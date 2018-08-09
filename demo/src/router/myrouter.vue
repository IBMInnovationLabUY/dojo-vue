<script>
import PageHome from '../components/Home';
import PageAbout from '../components/About';

const router = new VueRouter({
  routes: [
    {
      path: '/',
      component: PageHome
    },
    {
      path: '/about',
      component: PageAbout
    }
  ]
});
</script>
