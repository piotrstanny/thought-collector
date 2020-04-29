<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style scoped>
.panel-body {
    font-size: 14px;
    color: rgb(33, 71, 129);
    background-image: linear-gradient(to top left, rgb(233, 238, 255), rgb(184, 215, 255));
}
.quote {
    cursor: pointer
}
.quote:hover {
    background-image: linear-gradient(to top left, rgb(255, 233, 233), rgb(185, 57, 57));
}
</style>