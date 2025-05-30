<template>
    
    <div>
        <header>
            <slot name="header">
              <!-- <h2>The Default</h2> -->
            </slot>
        </header>
     <!--    you dont need to name all slots but you can only have 
        one unnamed slot which would be a default slot -->
      <slot></slot>
    </div>

</template>

<script>
export default{

}

</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

div {
  margin: 2rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
}

</style>