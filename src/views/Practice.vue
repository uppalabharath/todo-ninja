<template>
  <div class="practice">
    <!-- Text and color -->
    <!-- red is backgorund color white--text is the text color-->
    <p
      class="red white--text"
    >Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat laborum ipsum deleniti fugit quibusdam vitae repellendus ex iure officiis optio sit sint fuga sunt iste at harum, et, quod dignissimos?</p>
    <!-- lighten and darken are used to tweak the intensity of the color. Values can range from 1 to 4 -->
    <p
      class="pink lighten-4 red--text text--darken-4"
    >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugit minima ex fugiat vitae? Necessitatibus fugit perferendis repellat ad impedit exercitationem, distinctio aperiam, tempore consequuntur laborum esse nulla ex eius. Omnis?</p>
    <!-- font -->
    <h1 class="headline">Heading</h1>
    <h1 class="subheading">Sub heading</h1>
    <h1 class="caption">Caption</h1>
    <!-- buttons and Icons -->
    <v-btn class="indigo white--text">Button 1</v-btn>
    <!-- color can be applied using color class -->
    <v-btn color="indigo" class="white--text">Button 2</v-btn>
    <!-- using dark to make the text white -->
    <v-btn color="indigo" dark>Button 3</v-btn>
    <!-- making button look like already clicked. When depressed prop is used shadow is removed -->
    <v-btn depressed dark color="indigo">Button 4</v-btn>
    <!-- When flat prop is used backgorund gets transparent and color controls the text and hover -->
    <v-btn flat dark color="indigo">Button 4</v-btn>
    <!-- vuetify uses material icons by default -->
    <v-btn depressed dark color="indigo">
      <v-icon>email</v-icon>
    </v-btn>
    <!-- By default buttons are created with default size. these can be controlled using small and large props -->
    <v-btn depressed dark color="indigo">
      <!-- left prop moves the icon left -->
      <v-icon left>home</v-icon>
      <span>Home</span>
    </v-btn>
    <v-btn depressed large dark color="indigo">
      <v-icon left large>search</v-icon>
      <span>Search</span>
    </v-btn>
    <v-btn depressed small color="indigo" class="white--text">
      <v-icon left small>alarm</v-icon>
      <span>Remind</span>
    </v-btn>
    <!-- Making a round icon use fab prop-->
    <v-btn fab depressed color="indigo" class="white--text">
      <v-icon>favorite</v-icon>
    </v-btn>
    <!-- viewport breakpoints are used for responsive design and would come into action when screen resizes-->
    <v-btn class="hidden-md-and-down">Only Large and above</v-btn>
    <v-btn class="hidden-lg-and-up">Only medium and below</v-btn>
    <v-btn class="hidden-sm-only">Hide Only in Small</v-btn>
  </div>
</template>