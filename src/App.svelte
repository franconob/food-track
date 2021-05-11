<script lang="ts">
    import { Router, Link, Route } from "svelte-routing";
    import New from '@pages/new.svelte';
    import List from '@pages/List.svelte';

    function handleSubmit(submitEvent) {
       console.log(submitEvent.target.name.value);
    }
</script>

<Router>
   <Route path="new" component={New} />
   <Route path="/"><List /></Route>
</Router>
