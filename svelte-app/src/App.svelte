<script>
  import './styles.scss';
  import { Router, Link, Route } from 'svelte-routing';
  import About from './About.svelte';
  import Products from './products/Products.svelte';
  import MFA from './authenticated/MFA.svelte';

  import { HeaderBar, NavBar, PageNotFound, Redirect } from './components';

  export let url = '';
</script>

<HeaderBar />
<div class="section columns">
  <Router {url}>
    <NavBar />
    <main class="column">
      <div>
        <!-- <Route path="/">
          <Redirect path="/authenticated/MFA" />
        </Route> -->
        <Route path="/authenticated/MFA" component={MFA} />
      </div>
    </main>
  </Router>
</div>
