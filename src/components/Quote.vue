<template>
    <div class="col-sm-6 col-md-3">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <q>
                    <slot></slot>
                </q>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style scoped>
.panel-body {
    padding: 15px;
    font-size: 14px;
    color: rgb(33, 71, 129);
    background-image: linear-gradient(to top left, rgb(233, 238, 255), rgb(184, 215, 255));
    border: 1px solid rgb(188, 213, 245);
    border-radius: 5px;;
}
.quote {
    cursor: pointer
}
.quote:hover {
    background-image: linear-gradient(to top left, rgb(255, 233, 233), rgb(185, 57, 57));
}
</style>