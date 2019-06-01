<template>
    <div class="page">
        <div v-if="$route.params.page === 'grounds'" class="about">
            <p>
                In the shadow of ‘Peak Soil’, fertile soils are becoming more and more scarce leading to an escalating
                competition worldwide around this undervalued, but precious resource. The crucial role of healthy soil for the
                planet’s ecosystem has been, so far, the main focus of past attempts to face global soil loss. As various discourses
                and conflicts around the ownership of soil are rising worldwide, it is urgent to address soil in a more complex and nuanced
                manner – not just as an ecological problem but as a cultural, social and political issue.
            </p>
            <p>
                In order to provoke change, we need to seek new ways of engaging and thinking about what is under our feet,
                building an alternative soil culture within local and global scales. Unconventional approaches such as soil
                transplants and the inclusion of indigenous knowledge are considered as potential answers while challenging
                societal frameworks, namely the accessibility and ownership of resources. By combining a mythological and an analytical layer,
                this thesis confronts the imagery of the Garden of Eden, a utopian vision of fertility, with scientific, artistic and theoretical
                resources of past and present perspectives. Providing the grounds to speculate about the intertwined politics of soil, land and people,
                it encourages us to reconsider our relation to a material fundamental to our human existence – as individuals, societies and species.
            </p>
        </div>
        <div v-if="$route.params.page === 'soil'" class="about">
            <p>
                Global soil loss is not only an ecological problem but rather a cultural, social and political issue.
                Soils in Residency is a reaction to this current threat of ‘Peak Soil’ and seeks to materialize a new
                culture of soils within local and global scales. The project explores the transplantation of soils as a potential
                approach for reviving and altering soils for specific produce without artificial influence, while challenging societal
                frameworks, such as the ownership of resources.
            </p>
            <p>
                Whereas chromatography, a soil imaging method, is mainly used by farmers of the Global South, and soil transplants are
                only tested behind closed laboratory doors, this projects combines them in a physical intervention introducing them to
                our surroundings. Soils of different origins and agricultural treatments are inoculated in a test plot that is designed
                as a biogeographical map. Mirrored and monitored through soil chroma images, the results build up to an analogue and virtual
                archive of knowledge, displaying the soils’ potential and interactivity of a specific zone.
            </p>
            <p>
                By fusing art and science, the project challenges conventional ways of engaging and interacting with soil. It creates a
                transdisciplinary platform facilitating the exchange of knowledge and the sharing of the resource of soil. Seeking to create
                future visions of how to face the impoverishment of our grounds, Soils in Residency is understood as a pilot project with the
                ambition to scale its impact by establishing further test plots across the world.
            </p>
        </div>
    </div>
</template>
<style scoped>
    .about {
        text-align: left;
        width: 50%;
    }
</style>