<template>
  <div class="projects">
    <v-container>
      <div class="projectsHeader">Projects</div>
      <v-row>
        <v-col v-for="project in projects" :key="project.title" :cols="project.flex">
          <v-card>
            <v-img :src="project.src" class="white--text align-end" height="200px"></v-img>
            <v-card-title v-text="project.title"></v-card-title>
            <v-card-text v-text="project.desc"></v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'Projects',
  data () {
    return {
      projects: [
        { title: 'Risk AI (MCTS)', src: require('../assets/risk.png'), flex: 6, desc: 'For our integration project at school, a friend of mine and I were able to build, in 6 weeks, the base of a Monte Carlo Tree Search algorithm to play the Risk Boardgame. Because the game was written in Java, we wrote the algorithm in Java as well to reuse the functionality.' },
        { title: 'Painters Classifier', src: require('../assets/painters.jpg'), flex: 6, desc: 'During the course Artificial Intelligence 1, I build a classifier to classify the paintings of 4 different painters. The model was build upon the ResNet50 model in Keras, I added layers and retrained the new layers to specialize the model on our data.' },
        { title: 'Reinforcement Learning Library', src: require('../assets/rl.png'), flex: 6, desc: 'In Artificial Intelligence 2, we build a base library from scratch on the OpenAI Gym with different Reinforcement Learning algorithms (like NQ-learn, Value Iteration and Deep Q).' },
        { title: 'EEG Visualization', src: require('../assets/brain.png'), flex: 6, desc: 'For Data Science 3, we build a visualization for given EEG data, we build a preprocess algorithm and visualized the data in Plotly.' },
        { title: 'Speaker Diarization Internship', src: require('../assets/waveform.jpg'), flex: 6, desc: 'During my internship, I did research and build an application to implement Speaker Diariziation in combination with Speech-to-text. We used a PyTorch libary to diarize different files and implemented a video conference tool where the conference would the transcribed.' },
        { title: 'Twitter Sentiment Analyser (WIP)', src: require('../assets/twitter.jpg'), flex: 6, desc: 'I build a dashboard to analyse the sentiment of a keyword on Twitter. The dashboard was build in Plotly and the sentiment was calculated with Vader SentimentIntensityAnalyzer.' },
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
.projects {
  padding-top: 3%;
  height: 100%;
  width: 100%;
  background: #272727;
}

.projectsHeader {
  font-family: "Comfortaa", cursive;
  font-size: 4rem;
  font-weight: 600;
  padding-bottom: 2%;
}
</style>