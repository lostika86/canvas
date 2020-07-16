<template>
    <div class="shadow">
        <div class="col-xl-10 offset-xl-1 px-xl-5 col-md-12">
            <nav class="navbar justify-content-between flex-nowrap flex-row py-2 px-0">
                <a class="back-logo" :href="customRoutes.home"><svg style="width:32px;" version="1.1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 470 470" xmlns:xlink="http://www.w3.org/1999/xlink" enable-background="new 0 0 470 470">
                    <g>
                        <path d="M430.809,30h-40.491c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5,7.5,7.5h13.952c-2.827,4.673-4.457,10.148-4.457,15.997v354.509   c0,4.142,3.357,7.5,7.5,7.5s7.5-3.358,7.5-7.5V60.997c0-8.821,7.176-15.997,15.996-15.997c8.821,0,15.998,7.176,15.998,15.997   v354.509c0,21.777-17.717,39.494-39.494,39.494s-39.494-17.717-39.494-39.494V7.5c0-4.142-3.357-7.5-7.5-7.5H15.693   c-4.143,0-7.5,3.358-7.5,7.5v408.006C8.193,445.554,32.64,470,62.688,470h344.625c30.048,0,54.494-24.446,54.494-54.494V60.997   C461.807,43.905,447.901,30,430.809,30z M62.688,455c-21.777,0-39.494-17.717-39.494-39.494V15h329.625v400.506   c0,15.526,6.529,29.559,16.983,39.494H62.688z"/>
                        <path d="m320.318,40h-264.625c-4.143,0-7.5,3.358-7.5,7.5v75c0,4.142 3.357,7.5 7.5,7.5h264.625c4.143,0 7.5-3.358 7.5-7.5v-75c0-4.142-3.357-7.5-7.5-7.5zm-7.5,75h-249.625v-60h249.625v60z"/>
                        <path d="m320.318,145h-264.625c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5h264.625c4.143,0 7.5-3.358 7.5-7.5s-3.357-7.5-7.5-7.5z"/>
                        <path d="m320.318,205h-117.312c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5h117.313c4.143,0 7.5-3.358 7.5-7.5s-3.358-7.5-7.501-7.5z"/>
                        <path d="m173.006,205h-117.313c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5h117.313c4.143,0 7.5-3.358 7.5-7.5s-3.358-7.5-7.5-7.5z"/>
                        <path d="m320.318,235h-117.312c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5h117.313c4.143,0 7.5-3.358 7.5-7.5s-3.358-7.5-7.501-7.5z"/>
                        <path d="m173.006,235h-117.313c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5h117.313c4.143,0 7.5-3.358 7.5-7.5s-3.358-7.5-7.5-7.5z"/>
                        <path d="m320.318,265h-117.312c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5h117.313c4.143,0 7.5-3.358 7.5-7.5s-3.358-7.5-7.501-7.5z"/>
                        <path d="m320.318,295h-117.312c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5h117.313c4.143,0 7.5-3.358 7.5-7.5s-3.358-7.5-7.501-7.5z"/>
                        <path d="m203.006,340h77.313c4.143,0 7.5-3.358 7.5-7.5s-3.357-7.5-7.5-7.5h-77.313c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5z"/>
                        <path d="m280.318,415h-77.313c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5h77.313c4.143,0 7.5-3.358 7.5-7.5s-3.357-7.5-7.5-7.5z"/>
                        <path d="m320.318,385h-117.312c-4.143,0-7.5,3.358-7.5,7.5s3.357,7.5 7.5,7.5h117.313c4.143,0 7.5-3.358 7.5-7.5s-3.358-7.5-7.501-7.5z"/>
                        <path d="m173.006,265h-117.313c-4.143,0-7.5,3.358-7.5,7.5v150c0,4.142 3.357,7.5 7.5,7.5h117.313c4.143,0 7.5-3.358 7.5-7.5v-150c0-4.142-3.358-7.5-7.5-7.5zm-7.5,150h-102.313v-135h102.313v135z"/>
                    </g>
                </svg>
                    ADMIN
                </a>

                <ul class="navbar-nav mr-auto flex-row float-right">
                    <li class="text-muted font-weight-bold">
                        <slot name="status" />
                    </li>
                </ul>

                <div class="my-auto ml-auto d-flex align-items-end align-middle">
                    <slot name="action" />
                </div>

                <slot name="menu" />

                <div class="dropdown ml-3" v-cloak>
                    <a href="#" id="navbarDropdown" class="nav-link px-0 text-secondary" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                        <svg version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
                             viewBox="0 0 394.971 394.971" style="enable-background:new 0 0 394.971 394.971; width: 32px" xml:space="preserve">
                        <g>
                            <g>
                                <g>
                                    <path d="M56.424,146.286c-28.277,0-51.2,22.923-51.2,51.2s22.923,51.2,51.2,51.2s51.2-22.923,51.2-51.2
                                        S84.701,146.286,56.424,146.286z M56.424,227.788L56.424,227.788c-16.735,0-30.302-13.567-30.302-30.302
                                        s13.567-30.302,30.302-30.302c16.735,0,30.302,13.567,30.302,30.302S73.16,227.788,56.424,227.788z"/>
                                    <path d="M379.298,187.037H143.151c-5.771,0-10.449,4.678-10.449,10.449s4.678,10.449,10.449,10.449h236.147
                                        c5.771,0,10.449-4.678,10.449-10.449S385.069,187.037,379.298,187.037z"/>
                                    <path d="M56.424,0c-28.277,0-51.2,22.923-51.2,51.2s22.923,51.2,51.2,51.2s51.2-22.923,51.2-51.2S84.701,0,56.424,0z
                                         M56.424,81.502c-16.735,0-30.302-13.567-30.302-30.302s13.567-30.302,30.302-30.302S86.726,34.465,86.726,51.2
                                        S73.16,81.502,56.424,81.502z"/>
                                    <path d="M143.151,61.649h236.147c5.771,0,10.449-4.678,10.449-10.449s-4.678-10.449-10.449-10.449H143.151
                                        c-5.771,0-10.449,4.678-10.449,10.449S137.38,61.649,143.151,61.649z"/>
                                    <path d="M56.424,292.571c-28.277,0-51.2,22.923-51.2,51.2c0,28.277,22.923,51.2,51.2,51.2s51.2-22.923,51.2-51.2
                                        C107.624,315.494,84.701,292.571,56.424,292.571z M86.726,343.771c0,16.735-13.567,30.302-30.302,30.302v0
                                        c-16.735,0-30.302-13.567-30.302-30.302c0-16.735,13.567-30.302,30.302-30.302S86.726,327.036,86.726,343.771L86.726,343.771z"/>
                                    <path d="M379.298,333.322H143.151c-5.771,0-10.449,4.678-10.449,10.449s4.678,10.449,10.449,10.449h236.147
                                        c5.771,0,10.449-4.678,10.449-10.449S385.069,333.322,379.298,333.322z"/>
                                </g>
                            </g>
                        </g>
                        </svg>
                    </a>
                    <div class="dropdown-menu dropdown-menu-right" aria-labelledby="dropdownMenuButton">
                        <h6 class="dropdown-header">
                            <strong>{{ user.name }}</strong>
                            <br/>
                            {{ user.email }}
                        </h6>
                        <div class="dropdown-divider"></div>

                        <router-link to="/posts" class="dropdown-item">
                            <span>{{ trans.app.posts_simple }}</span>
                        </router-link>
                        <router-link to="/tags" class="dropdown-item">
                            <span>{{ trans.app.tags }}</span>
                        </router-link>
<!--                        <router-link to="/topics" class="dropdown-item">-->
<!--                            <span>{{ trans.app.topics }}</span>-->
<!--                        </router-link>-->
                        <router-link to="/stats" class="dropdown-item">
                            <span>{{ trans.app.stats }}</span>
                        </router-link>
<!--                        <div class="dropdown-divider"></div>-->
<!--                        <router-link to="/settings" class="dropdown-item">-->
<!--                            <span>{{ trans.app.settings }}</span>-->
<!--                        </router-link>-->
<!--                        <a href="" class="dropdown-item" @click.prevent="sessionLogout">-->
<!--                            {{ trans.app.sign_out }}-->
<!--                        </a>-->
                    </div>
                </div>
            </nav>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'page-header',

        data() {
            return {
                user: Canvas.user,
                avatar: this.$root.avatar,
                token: this.getToken(),
                trans: JSON.parse(Canvas.lang),
                customRoutes: {
                    home : Canvas.customRoutes.home
                }
            }
        },

        watch: {
            '$root.avatar': function(url){
                this.avatar = url
            }
        },

        methods: {
            sessionLogout() {
                this.logout()
            },
        },
    }
</script>
