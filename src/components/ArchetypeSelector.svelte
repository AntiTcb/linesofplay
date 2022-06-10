<script>
    import { MultiSelect } from 'carbon-components-svelte';
    import supabase from '$utils/db';
    import { onMount } from 'svelte';

    let archetypes = [];

    export let selectedArchetypes = [];

    const getArchetypes = async () => {
        const { data, error } = await supabase.from('tags').select('id,name').eq('type', 'archetype');
        if (!error)
            archetypes = data.map(a => ({ id: a.id, text: a.name }));

    };

    onMount(async () => {
        await getArchetypes();
    });
</script>

<MultiSelect filterable titleText="Select archetype(s)" items={archetypes} />
