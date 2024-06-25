<script setup></script>
<template>
        <div class="pages">
            <a href="#" class="page_no"><</a>
            <a href="#" class="page_no">1</a>
            <a href="#" class="page_no">2</a>
            <a href="#" class="page_no">...</a>
            <a href="#" class="page_no">8</a>
            <a href="#" class="page_no">9</a>
            <a href="#" class="page_no">10</a>
            <a href="#" class="page_no">11</a>
            <a href="#" class="page_no">12</a>
            <a href="#" class="page_no">13</a>
            <a href="#" class="page_no">14</a>
            <a href="#" class="page_no">...</a>
            <a href="#" class="page_no">56</a>
            <a href="#" class="page_no">57</a>
            <a href="#" class="page_no">></a>
        </div>
</template>

<style scoped>
.pages
{
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    width: 100%;
    gap: 5px;
}

.pages .page_no 
{
    padding: 5px 10px;
    background-color: var(--light);
    border: 1px solid var(--light-gray);
    color: var(--dark);
    font-size: 12px;
    font-weight: 500;
}

.pages .page_no:hover 
{
    background-color: var(--red);
    color: var(--light);
}
</style>