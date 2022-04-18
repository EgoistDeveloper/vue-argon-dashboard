<template>
    <!-- Modal 1 -->
    <modal ref="modal1" v-model:show="isOpenModal1" modalClasses="modal-lg">
        <template v-slot:header>
            <h1>Lorem Title</h1>
        </template>

        <p>
            Aute adipisicing aliquip exercitation ad aute nostrud ut nisi duis labore aliquip nisi qui fugiat. Excepteur aute incididunt aliqua exercitation ex
            incididunt duis nulla. In incididunt aute laboris nulla duis ullamco aliqua id ea sint ea proident do proident. Consequat cupidatat dolor pariatur
            qui. Proident culpa ut cupidatat qui excepteur aliquip nulla. Esse eiusmod nulla aliqua veniam duis eu non laboris. Proident cupidatat sint eu
            commodo deserunt magna sint reprehenderit non nisi velit id cillum. Irure dolor irure consectetur laborum. Ea non magna deserunt nulla irure nostrud
            culpa aliqua aliquip Lorem eiusmod pariatur adipisicing. Sunt velit fugiat ipsum mollit veniam sit esse mollit do eu eu. Velit sunt dolore mollit
            veniam eiusmod deserunt sint do id do ipsum et mollit sint. Ipsum cillum qui labore aute labore enim. Officia sit magna est esse tempor dolor sit eu
            culpa labore quis duis qui. Aute adipisicing in ea laboris commodo reprehenderit occaecat occaecat ipsum voluptate pariatur dolor cillum.
            Adipisicing ipsum laborum eiusmod consectetur pariatur anim nostrud dolor labore culpa sit ullamco fugiat. Enim duis aliqua labore consequat
            excepteur commodo enim duis reprehenderit aliquip esse amet occaecat. Id id fugiat exercitation ea sit id velit velit reprehenderit officia
            voluptate dolore aliqua. Laboris aliquip cupidatat veniam nisi quis. Non mollit duis eiusmod dolore consectetur dolor qui esse cillum minim est
            laborum ad aute. Ad adipisicing esse incididunt excepteur. Laborum laborum excepteur laboris fugiat quis. Cupidatat consectetur irure qui non
            officia velit ullamco ex est laborum sit. Irure anim minim minim eu labore eiusmod ullamco occaecat amet eiusmod qui tempor enim. Duis aliquip
            deserunt aliquip qui reprehenderit. Et anim anim eu veniam laborum. Cupidatat minim occaecat duis incididunt aliquip enim enim. Aliquip do duis ut
            non. Sint dolor sint dolor duis nulla.
        </p>

        <template v-slot:footer>
            <div class="font-weight-bold">Story ends here</div>
        </template>
    </modal>

    <!-- Modal 2 -->
    <modal ref="modal2" v-model:show="isOpenModal2" modalClasses="modal-lg">
        <template v-slot:header>
            <h1>Register Form</h1>
        </template>

        <card shadow type="secondary">
            <template v-slot:header>
                <div class="bg-white border-0">
                    <div class="row align-items-center">
                        <div class="col-8">
                            <h3 class="mb-0">My account</h3>
                        </div>
                    </div>
                </div>
            </template>

            <form>
                <h6 class="heading-small text-muted mb-4">User information</h6>
                <div class="pl-lg-4">
                    <div class="row">
                        <div class="col-lg-6">
                            <base-input
                                alternative=""
                                label="Username"
                                placeholder="Username"
                                input-classes="form-control-alternative"
                                v-model="model.username"
                            />
                        </div>
                        <div class="col-lg-6">
                            <base-input
                                alternative=""
                                label="Email address"
                                placeholder="jesse@example.com"
                                input-classes="form-control-alternative"
                                v-model="model.email"
                            />
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-lg-6">
                            <base-input
                                alternative=""
                                label="First name"
                                placeholder="First name"
                                input-classes="form-control-alternative"
                                v-model="model.firstName"
                            />
                        </div>
                        <div class="col-lg-6">
                            <base-input
                                alternative=""
                                label="Last name"
                                placeholder="Last name"
                                input-classes="form-control-alternative"
                                v-model="model.lastName"
                            />
                        </div>
                    </div>
                </div>
                <hr class="my-4" />
                <!-- Address -->
                <h6 class="heading-small text-muted mb-4">Contact information</h6>
                <div class="pl-lg-4">
                    <div class="row">
                        <div class="col-md-12">
                            <base-input
                                alternative=""
                                label="Address"
                                placeholder="Home Address"
                                input-classes="form-control-alternative"
                                v-model="model.address"
                            />
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-lg-4">
                            <base-input alternative="" label="City" placeholder="City" input-classes="form-control-alternative" v-model="model.city" />
                        </div>
                        <div class="col-lg-4">
                            <base-input alternative="" label="Country" placeholder="Country" input-classes="form-control-alternative" v-model="model.country" />
                        </div>
                        <div class="col-lg-4">
                            <base-input
                                alternative=""
                                label="Postal code"
                                placeholder="Postal code"
                                input-classes="form-control-alternative"
                                v-model="model.zipCode"
                            />
                        </div>
                    </div>
                </div>

                <hr class="my-4" />

                <!-- Description -->
                <h6 class="heading-small text-muted mb-4">About me</h6>
                <div class="pl-lg-4">
                    <div class="form-group">
                        <base-input alternative="" label="About Me">
                            <textarea rows="4" class="form-control form-control-alternative" placeholder="A few words about you ...">
A beautiful Dashboard for Bootstrap 4. It is Free and Open Source.</textarea
                            >
                        </base-input>
                    </div>
                </div>

                <hr class="my-4" />

                <div class="row">
                    <div class="container">
                        <button class="btn btn-primary float-right">Save</button>
                    </div>
                </div>
            </form>
        </card>
    </modal>

    <!-- Modal 3 -->
    <modal ref="modal3" v-model:show="isOpenModal3">
        <template v-slot:header>
            <h1>Example Modal 3</h1>
        </template>

        <p>
            Aliquip tempor est deserunt minim qui nostrud. Lorem proident in ut amet. Ut irure magna nisi sit duis. Nulla fugiat et officia irure tempor eiusmod
            proident consequat fugiat velit nisi. Culpa ex culpa in magna veniam nisi aliqua. Fugiat irure culpa occaecat eiusmod amet est aliquip nisi veniam
            est esse veniam. Est ex mollit nisi mollit enim tempor. Eu velit laboris excepteur ad excepteur tempor. Veniam voluptate commodo deserunt amet ipsum
            Lorem sit dolore labore consequat ut commodo exercitation. Laborum non consequat exercitation ipsum enim elit anim in reprehenderit ea cillum anim
            id nulla. Velit nulla fugiat consectetur commodo culpa eu consectetur. Nostrud occaecat magna ex qui commodo sint est fugiat voluptate dolor velit
            deserunt. Nulla officia voluptate elit velit proident minim excepteur velit duis est consequat. Quis ex exercitation nulla ea adipisicing
            consectetur. Nostrud sit culpa labore occaecat deserunt aliqua proident sunt. Id officia magna eu nisi excepteur. Voluptate consectetur ipsum amet
            laboris sunt sunt veniam aute adipisicing. Nisi ea magna id qui. Irure nostrud esse eu dolor magna anim ea.
        </p>

        <template v-slot:footer>
            <div class="row">
                <div class="col">
                    <button class="btn btn-primary float-right" @click="isOpenModal3 = false">Close</button>
                </div>
            </div>
        </template>
    </modal>

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
                                <button class="btn btn-default" @click="showModal1()">Text Modal</button>
                            </div>

                            <div class="col-3">
                                <button class="btn btn-default" @click="showModal2()">Form Modal</button>
                            </div>

                            <div class="col-3">
                                <button class="btn btn-default" @click="showModal3()">Close Button Modal</button>
                            </div>
                        </div>
                    </card>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "modals-page",
    data() {
        return {
            model: {
                username: "",
                email: "",
                firstName: "",
                lastName: "",
                address: "",
                city: "",
                country: "",
                zipCode: "",
                about: "",
            },
            isOpenModal1: false,
            isOpenModal2: false,
            isOpenModal3: false,
        };
    },
    mounted() {},
    methods: {
        showModal1() {
            this.isOpenModal1 = !this.isOpenModal1;
        },

        showModal2() {
            this.isOpenModal2 = !this.isOpenModal2;
        },

        showModal3() {
            this.isOpenModal3 = !this.isOpenModal3;
        },
    },
};
</script>
<style></style>
