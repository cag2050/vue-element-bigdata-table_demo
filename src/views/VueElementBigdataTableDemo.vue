<template>
    <div>
        <el-bigdata-table :data="tableData" height="500" :rowHeight="44">
            <el-table-column type="selection" width="55"></el-table-column>
            <el-table-column prop="ip" label="IP"></el-table-column>
        </el-bigdata-table>
    </div>
</template>

<script>
import ElBigdataTable from "vue-elementui-bigdata-table";

export default {
    components: {
        ElBigdataTable
    },
    data() {
        return {
            tableData: []
        };
    },
    mounted() {
        for (let i = 0; i < 500; i++) {
            this.tableData.push({
                ip: "111.222.333." + String(i + 1)
            });
        }
    },
    methods: {}
};
</script>

<style scoped></style>
