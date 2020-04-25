<template>
    <div>
        <table border='1'>
            <thead>
                <td v-for="(item, index) in columns" :key='index'>
                    {{item.title}}
                </td>
            </thead>
            <tbody>
                <tr v-for="(item, index) in data" :key="index">
                    <td v-for="(citem, cindex) in columns" :key='cindex'>
                        {{item[citem.key]}}
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
    export default {
        props: ['columns', 'data']
    }
</script>

<style lang="scss" scoped>

</style>