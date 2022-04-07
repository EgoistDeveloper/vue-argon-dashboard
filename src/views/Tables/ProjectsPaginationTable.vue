<template>
    <div class="card shadow" :class="type === 'dark' ? 'bg-default' : ''">
        <div class="card-header border-0" :class="type === 'dark' ? 'bg-transparent' : ''">
            <div class="row align-items-center">
                <div class="col">
                    <h3 class="mb-0" :class="type === 'dark' ? 'text-white' : ''">
                        {{ title }}
                    </h3>
                </div>

                <div class="col">
                    <base-pagination
                        class="float-right"
                        v-if="content && content.data"
                        :pageCount="content.last_page"
                        :perPage="content.per_page"
                        :value="content.current_page"
                        @input="changePage"
                    ></base-pagination>
                </div>
            </div>
        </div>

        <div v-if="content && content.data" class="table-responsive">
            <base-table
                class="table align-items-center table-flush"
                :class="type === 'dark' ? 'table-dark' : ''"
                :thead-classes="type === 'dark' ? 'thead-dark' : 'thead-light'"
                tbody-classes="list"
                :data="content.data"
            >
                <template v-slot:columns>
                    <th>Project</th>
                    <th>Budget</th>
                    <th>Status</th>
                    <th>Users</th>
                    <th>Completion</th>
                    <th></th>
                </template>

                <template v-slot:default="row">
                    <th scope="row">
                        <div class="media align-items-center">
                            <a href="#" class="avatar rounded-circle mr-3">
                                <img alt="Image placeholder" :src="row.item.img" />
                            </a>
                            <div class="media-body">
                                <span class="name mb-0 text-sm">{{ row.item.title }}</span>
                            </div>
                        </div>
                    </th>
                    <td class="budget">
                        {{ row.item.budget }}
                    </td>
                    <td>
                        <badge class="badge-dot mr-4" :type="row.item.statusType">
                            <i :class="`bg-${row.item.statusType}`"></i>
                            <span class="status">{{ row.item.status }}</span>
                        </badge>
                    </td>
                    <td>
                        <div class="avatar-group">
                            <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip" data-original-title="Ryan Tompson">
                                <img alt="Image placeholder" src="img/theme/team-1-800x800.jpg" />
                            </a>

                            <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip" data-original-title="Romina Hadid">
                                <img alt="Image placeholder" src="img/theme/team-2-800x800.jpg" />
                            </a>

                            <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip" data-original-title="Alexander Smith">
                                <img alt="Image placeholder" src="img/theme/team-3-800x800.jpg" />
                            </a>

                            <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip" data-original-title="Jessica Doe">
                                <img alt="Image placeholder" src="img/theme/team-4-800x800.jpg" />
                            </a>
                        </div>
                    </td>

                    <td>
                        <div class="d-flex align-items-center">
                            <span class="completion mr-2">{{ row.item.completion }}%</span>

                            <div>
                                <base-progress :type="row.item.statusType" :show-percentage="false" class="pt-0" :value="row.item.completion" />
                            </div>
                        </div>
                    </td>

                    <td class="text-right">
                        <base-dropdown class="dropdown" position="right">
                            <template v-slot:title>
                                <a class="btn btn-sm btn-icon-only text-light" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                    <i class="fas fa-ellipsis-v"></i>
                                </a>
                            </template>

                            <li class="dropdown-item">Action</li>

                            <li class="dropdown-item">Another action</li>

                            <li class="dropdown-item">Something else here</li>
                        </base-dropdown>
                    </td>
                </template>
            </base-table>
        </div>

        <h3 v-if="!content || !content.data" class="text-center my-4">There is no data to display</h3>

        <div class="card-footer d-flex justify-content-end" :class="type === 'dark' ? 'bg-transparent' : ''">
            <base-pagination
                class="float-right"
                v-if="content && content.data"
                :pageCount="content.last_page"
                :perPage="content.per_page"
                :value="content.current_page"
                @input="changePage"
            ></base-pagination>
        </div>
    </div>
</template>
<script>
export default {
    name: "projects-pagination-table",
    props: {
        type: {
            type: String,
        },
        title: String,

        content: null,
    },

    data() {
        return {};
    },

    methods: {
        changePage(page) {
            this.$emit("change-page", page);
        },
    },
};
</script>
<style></style>
