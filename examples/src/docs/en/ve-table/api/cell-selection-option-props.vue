<template>
    <div>
        <tpl
            :desc="desc"
            :anchor="anchor"
            :table-data="db.cellSelectionOption.data"
            :columns="db.cellSelectionOption.columns"
        />
    </div>
</template>
<script>
import tpl from "@/comp/api-tpl";
import { db } from "./db";
export default {
    components: { tpl },
    props: {
        anchor: {
            type: String,
            default: "Cell selection configuration",
        },
        desc: {
            type: String,
            default: "cellSelectionOption",
        },
    },
    data() {
        return {
            db: db,
        };
    },
};
</script>
