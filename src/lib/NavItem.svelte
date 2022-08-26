<script>
    import { getContext } from 'svelte';
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
    
    export let segment = null;
    const current = getContext('nav');
    
    function setSegment(){
        current.set(segment);
    }
    
    
    
    </script>
    
    <li on:click={setSegment} class:active="{$current === segment}"><a style="text-decoration: none; color:white; text-shadow:black 0px 0px 2px" href={segment}><slot></slot></a></li>
    
    