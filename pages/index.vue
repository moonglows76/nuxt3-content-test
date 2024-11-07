
<template>
  <main>
    <h1>トップページ</h1>

    <ul>
      <li>
        <NuxtLink to="/">Top</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about">About</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/service">Service</NuxtLink>
      </li>
    </ul>

    <h2>Blog</h2>
    <ContentList path="/blog" v-slot="{ list }">
      <a :href="article._path" v-for="article in list" :key="article._path">
        <h3>{{ article.title }}</h3>
        <p>{{ article.description }}</p>
      </a>
    </ContentList>
    <h2>Staff Blog</h2>
    <ContentList path="/staff-blog" v-slot="{ list }">
      <a :href="article._path" v-for="article in list" :key="article._path">
        <h3>{{ article.title }}</h3>
        <p>{{ article.description }}</p>
      </a>
    </ContentList>
  </main>
</template>