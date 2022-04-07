<template>
    <div>
        <base-header type="gradient-success" class="pb-6 pb-8 pt-5 pt-md-8">
            <!-- Card stats -->
            <div class="row">
                <div class="col-xl-3 col-lg-6">
                    <stats-card title="Total traffic" type="gradient-red" sub-title="350,897" icon="ni ni-active-40" class="mb-4 mb-xl-0">
                        <template v-slot:footer>
                            <span class="text-success mr-2"><i class="fa fa-arrow-up"></i> 3.48%</span>
                            <span class="text-nowrap">Since last month</span>
                        </template>
                    </stats-card>
                </div>
                <div class="col-xl-3 col-lg-6">
                    <stats-card title="Total traffic" type="gradient-orange" sub-title="2,356" icon="ni ni-chart-pie-35" class="mb-4 mb-xl-0">
                        <template v-slot:footer>
                            <span class="text-success mr-2"><i class="fa fa-arrow-up"></i> 12.18%</span>
                            <span class="text-nowrap">Since last month</span>
                        </template>
                    </stats-card>
                </div>
                <div class="col-xl-3 col-lg-6">
                    <stats-card title="Sales" type="gradient-green" sub-title="924" icon="ni ni-money-coins" class="mb-4 mb-xl-0">
                        <template v-slot:footer>
                            <span class="text-danger mr-2"><i class="fa fa-arrow-down"></i> 5.72%</span>
                            <span class="text-nowrap">Since last month</span>
                        </template>
                    </stats-card>
                </div>
                <div class="col-xl-3 col-lg-6">
                    <stats-card title="Performance" type="gradient-info" sub-title="49,65%" icon="ni ni-chart-bar-32" class="mb-4 mb-xl-0">
                        <template v-slot:footer>
                            <span class="text-success mr-2"><i class="fa fa-arrow-up"></i> 54.8%</span>
                            <span class="text-nowrap">Since last month</span>
                        </template>
                    </stats-card>
                </div>
            </div>
        </base-header>

        <div class="container-fluid mt--7">
            <div class="row mt-5">
                <div class="col">
                    <projects-table title="Light Table"></projects-table>
                </div>
            </div>

            <div class="row mt-5">
                <div class="col">
                    <projects-table type="dark" title="Dark Table"></projects-table>
                </div>
            </div>

            <div class="row mt-5">
                <div class="col">
                    <projects-pagination-table
                        title="Paginated Light Table Example"
                        :content="projectsPaginationTableData"
                        @changePage="loadPaginatedData"
                    ></projects-pagination-table>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import ProjectsTable from "./Tables/ProjectsTable";
import ProjectsPaginationTable from "./Tables/ProjectsPaginationTable";

export default {
    name: "tables",
    components: {
        ProjectsTable,
        ProjectsPaginationTable,
    },

    data() {
        return {
            projectsPaginationTableData: null,
        };
    },

    mounted() {
        this.loadPaginatedData();
    },

    methods: {
        loadPaginatedData(page = 1) {
            // first page data
            var data = [
                {
                    img: "img/theme/bootstrap.jpg",
                    title: "Argon Design System",
                    budget: "$2500 USD",
                    status: "pending",
                    statusType: "warning",
                    completion: 60,
                },
                {
                    img: "img/theme/angular.jpg",
                    title: "Angular Now UI Kit PRO",
                    budget: "$1800 USD",
                    status: "completed",
                    statusType: "success",
                    completion: 100,
                },
                {
                    img: "img/theme/sketch.jpg",
                    title: "Black Dashboard",
                    budget: "$3150 USD",
                    status: "delayed",
                    statusType: "danger",
                    completion: 72,
                },
            ];

            // presents to next page
            if (page > 1) {
                data = [
                    {
                        img: "img/theme/sketch.jpg",
                        title: "Black Dashboard",
                        budget: "$3150 USD",
                        status: "delayed",
                        statusType: "danger",
                        completion: 72,
                    },
                    {
                        img: "img/theme/react.jpg",
                        title: "React Material Dashboard",
                        budget: "$4400 USD",
                        status: "on schedule",
                        statusType: "info",
                        completion: 90,
                    },
                    {
                        img: "img/theme/vue.jpg",
                        title: "Vue Paper UI Kit PRO",
                        budget: "$2200 USD",
                        status: "completed",
                        statusType: "success",
                        completion: 100,
                    },
                ];
            }

            // dummy pagianted static data
            this.projectsPaginationTableData = {
                data: data,
                per_page: 3,
                current_page: page,
                last_page: 5,
            };
        },
    },
};
</script>

<style></style>
