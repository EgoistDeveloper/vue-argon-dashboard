<template>
    <div>
        <base-header
            class="header pb-8 pt-5 pt-lg-8 d-flex align-items-center"
            style="min-height: 600px; background-image: url(img/theme/covers/warehouse.jpg); background-size: cover; background-position: center top"
        >
            <!-- Mask -->
            <span class="mask bg-gradient-success opacity-8"></span>
            <!-- Header container -->
            <div class="container-fluid d-flex align-items-center">
                <div class="row">
                    <div class="col-lg-7 col-md-10">
                        <h1 class="display-2 text-white">Modals</h1>

                        <p class="text-white mt-0 mb-5">Modal examples</p>
                    </div>
                </div>
            </div>
        </base-header>

        <div class="container-fluid mt--7">
            <div class="row">
                <div class="col-xl-12 order-xl-1">
                    <card shadow type="secondary">
                        <template v-slot:header>
                            <div class="bg-white border-0">
                                <div class="row align-items-center">
                                    <div class="col-8">
                                        <h3 class="mb-0">Modal Exmaples</h3>
                                    </div>
                                </div>
                            </div>
                        </template>

                        <div class="row">
                            <div class="col-3">
                                <button class="btn btn-success" @click="showSuccessNotification()">Success Notification</button>
                            </div>

                            <div class="col-3">
                                <button class="btn btn-danger" @click="showErrorNotification()">Error Notification</button>
                            </div>

                            <div class="col-3">
                                <button class="btn btn-info" @click="showInfoNotification()">Info Notification</button>
                            </div>
                        </div>
                    </card>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import NotificationService from "@/services/NotificationService";

export default {
    name: "notifications-page",
    data() {
        return {};
    },

    mounted() {},

    methods: {
        showSuccessNotification() {
            NotificationService.success("Success Notification");
        },

        showErrorNotification() {
            NotificationService.error("Error Notification");
        },

        showInfoNotification() {
            NotificationService.info("Info Notification");
        },
    },
};
</script>

<style></style>
