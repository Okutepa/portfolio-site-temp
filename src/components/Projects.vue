<template>
         <section class="projects" id="projects">
            <div class="grid-con">
                <div class="projects-content col-span-full">   
                    <div class="projects-heading">
                        <h2 class="heading-h2">Featured Works</h2>
                        <div class="divisor"></div>
                     </div>


                <!-- dynamic projects -->

                <div class="showcase col-span-full" v-for="(project, index) in projects" :key="project.id" :class="{ 'reverse': index % 2 !== 0 }">
                    <div class="showcase-item">
                        <div class="showcase-image">
                            <img :src="project.Image" :alt="project.title" />
                            <div class="pagination">
                                <div class="pagination-number">{{ index + 1 }}/{{ projects.length }}</div>
                                <div class="pagination-buttons"></div>
                            </div>
                        </div>

                        <div class="showcase-text">
                            <div class="showcase-title">
                                <h3 class="heading-h3">{{ project.title }}</h3>
                                <p class="body-text-bold category">
                                    {{ project.category }}
                                </p>
                                <p class="body-text-light year">
                                    {{ project.year }}
                                </p>
                            </div>

                            <div class="showcase-description">
                                    <p class="body-text-light" v-for="paragraph in project.description" :key="paragraph">
                                        {{ paragraph }}
                                    </p>
                            </div>  
                        </div>                      
                    </div>
                </div>
                </div>

            </div>
        </section>
</template>

<script>
import { projectData } from '../data/projectData.js'

export default {
  name: 'Projects',
  data() {
    return {
        projects: projectData
    }
  }
}
</script>