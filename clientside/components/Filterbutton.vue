<template>
    <b-dropdown id="dropdown-1" text="Filter by Category" class="shadow-sm float-right">
        <b-dropdown-item>All</b-dropdown-item>
        <b-dropdown-item>Vegitable</b-dropdown-item>
        <b-dropdown-item active>Fish</b-dropdown-item>
        <b-dropdown-item>Meat</b-dropdown-item>
    </b-dropdown>
</template>

<script>
export default {
    name: "filterdropdown"
}
</script>

<style scoped> 
.dropdown-menu.show {
    display: block;
    box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075) !important;
    border: none; 
}

</style>