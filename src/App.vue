<template>
  <div id="app">
    <ui-button>
      Кнопка
    </ui-button>
    <ui-button variant="danger">
      Кнопка
    </ui-button>
    <ui-button variant="minor">
      Кнопка
    </ui-button>
    <ui-button variant="minor" flat>
      Очень очень длинная кнопка кек
    </ui-button>
    <ui-button flat>
      Кнопка
    </ui-button>
    <ui-button variant="danger" flat>
      Кнопка
    </ui-button>
    <ui-button variant="minor" flat>
      Кнопка
    </ui-button>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  :root {
    --transition-bg-duration: .25s;

    --button-primary-bg-color: #18A0FB;
    --button-danger-bg-color: #FF3E1D;
    --button-minor-bg-color: #F6F6F6;

    --button-primary-font-color: #FFFFFF;
    --button-danger-font-color: #FFFFFF;
    --button-minor-font-color: #878787;

    --button-flat-bg-color: #FFFFFF;


    --button-primary-bg-color_hover: #1896f0;
    --button-danger-bg-color_hover: #f03d1d;
    --button-minor-bg-color_hover: #f0f0f0;

    --button-primary-bg-color_active: #187cd7;
    --button-danger-bg-color_active: #d7331b;
    --button-minor-bg-color_active: #d7d7d7;

  }
</style>
