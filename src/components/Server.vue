<template>
  <div>
    <div v-if="loaded">
      <div v-for="part of parts">
        <p>
          <b>
            URL:
          </b>
          &nbsp;
          <span>
              {{this[part + 'Url']}}
          </span>
        </p>

        <p>
          <b>
            Response:
          </b>
          &nbsp;
          <span>
              {{this[part]}}
          </span>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
  import { get, post, put, del } from '@/utils/api';

  export default {
    name: 'Server',
    props: {
      endpoint: ''
    },
    data () {
      return {
        get: '',
        post: '',
        put: '',
        delete: '',
        loaded: false
      };
    },
    async mounted() {
      const getResponse = await get(this.getUrl);
      this.get = getResponse.data;

      const postResponse = await post(this.postUrl, this.payload);
      this.post = postResponse.data;

      const putResponse = await put(this.putUrl, this.payload);
      this.put = putResponse.data;

      const deleteResponse = await del(this.deleteUrl);
      this.delete = deleteResponse.data;

      this.loaded = true;
    },
    computed: {
      parts: () => ['get', 'post', 'put', 'delete'],
      getUrl () {
        return this.endpoint + '/api?input=abc';
      },
      postUrl () {
        return this.endpoint + '/api';
      },
      putUrl () {
        return this.endpoint + '/api';
      },
      deleteUrl () {
        return this.endpoint + '/api';
      },
      payload: () => ({ a: 'A', b: 'B'})
    }
  }
</script>