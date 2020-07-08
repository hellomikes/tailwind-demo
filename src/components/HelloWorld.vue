<template>
  <div class="container">
    <div class="bg-category-alpha md:bg-brand-light lg:bg-category-beta w-10 md:w-20 lg:w-100 h-10 md:h-20 lg:h-100">
      I should change colours with every breakpoint
    </div>

    <a
      href="/link-to-page"
      class="c-category-link w-full md:w-1/3 md:px-2 mb-2 md:mb-4"
      ><div class="c-category-link__container md:bg-category-alpha">
        <div class="c-category-link__container__img border-category-alpha">
          <img
            src="http://placehold.it/300x190"
            alt="See items in Fencing category"
          />
        </div>
        <div class="c-category-link__content">
          <h4 class="c-category-link__container__title">
            Fencing
          </h4>
          <div class="c-category-link__icon md:mt-4 md:bg-category-alpha">
            <span>View Products</span>
            <svg version="1.1" viewBox="0 0 9 14" class="svg-icon svg-fill">
              <path
                pid="0"
                d="M1 1l6 6-6 6"
                _stroke="#7B5901"
                stroke-width="2"
              ></path>
            </svg>
          </div>
        </div>
      </div>
      <!----></a
    >
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

</style>

<style lang="css">
.c-category-link {
  @apply bg-brand-dark flex text-white uppercase tracking-sm text-lg-button font-bold transition-all items-center justify-between;
}
.c-category-link.no-image {
  @apply p-4 w-full bg-brand-medium;
}

.c-category-link.no-image .c-category-link__content {
  @apply w-full;
}
.c-category-link:hover {
  /* @apply pr-1; */
}

.c-category-link__container {
  box-shadow: 0 2px 9px rgba(0,0,0,0.13);
  @apply flex flex-row items-center h-full;
}

.c-category-link__content {
  @apply flex flex-row justify-between w-3/4;
}

.c-category-link__container__title {
  @apply block text-left text-h5 uppercase leading-small tracking-sm font-body;
}
.c-category-link.no-image .c-category-link__container__title {
  @apply w-full;
}
.c-category-link__container__img {
  @apply border-r-4 inline mr-2 inline-flex w-1/4;
}
.c-category-link__container__img img {
  @apply w-full h-16 object-cover;
}
.c-category-link__icon svg {
  @apply self-center stroke-current fill-transparent ml-1 h-3 mr-3;
}

.c-category-link__icon {
  @apply inline-flex;
}

.c-category-link__icon span {
  @apply hidden;
}

@screen md {
  .c-category-link {
    @apply normal-case;
  }
  .c-category-link.no-image {
    @apply p-0;
  }
  .c-category-link.no-image .c-category-link__content {
    height: 100%;
  }

  .c-category-link__content {
    @apply flex-col w-full py-10 px-2 justify-center;
  }

  .c-category-link {
    @apply inline-flex flex-col normal-case bg-transparent justify-start;
  }

  .c-category-link:hover {
    /* transform: scale(1.02); */
  }

  .c-category-link__container {
    box-shadow: none;
    @apply flex-col;
  }
  .c-category-link__container,
  .c-category-link__container__title,
  .c-category-link__container__img {
    @apply block w-full mr-0 border-r-0;
  }
  .c-category-link__container__title {
    font-size: 1.8125rem;
    @apply text-center leading-h1 font-black normal-case tracking-normal;
  }

  .c-category-link__container__img {
    @apply border-t-4;
  }

  .c-category-link__container__img img {
    @apply w-full h-auto;
  }
  .c-category-link__icon {
    @apply flex w-full content-center justify-center;
  }
  .c-category-link__icon svg {
    @apply mr-0;
  }
  .c-category-link__icon span {
    @apply block uppercase;
  }
  .c-category-link:hover {
    /* @apply pr-2; */
  }

  .c-category-link.no-image {
    /* @apply py-0; */
  }
  .c-category-link.no-image .c-category-link__container {
    @apply h-full justify-center inline-flex;
  }

  .c-category-link.is-category-page .c-category-link__container__title {
    @apply text-lg-h4 font-bold;
  }
}
</style>

