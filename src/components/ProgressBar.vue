<template>
    <progress-bar
        :options="{
                text: {
                    color: '#000000',
                    shadowEnable: true,
                    shadowColor: '#000000',
                    fontSize: 15,
                    fontFamily: 'Helvetica',
                    dynamicPosition: false,
                    hideText: false
                },
                progress: {
                    color: '#2dbd2d',
                    backgroundColor: '#C0C0C0'
                },
                layout: {
                    height: 35,
                    width: 500,
                    verticalTextAlign: 61,
                    horizontalTextAlign: 43,
                    zeroOffset: 50,
                    strokeWidth: 30,
                    progressPadding: 5,
                    type: 'line'
                }
            }"
        :value="percent"
    />
</template>

<script>
import ProgressBar from 'vuejs-progress-bar'

export default {
    components: {
        ProgressBar
    },
    props: {
        options: {

        }
    },
    data: function() {
        return {
            percent: 0
        };
    },
    created: function() {
        let self = this
        setInterval(function() {
            self.percent = self.percent + 1
            if(self.percent > 100) {
                self.percent = 0
            }
        }, 2000)
    }
}


</script>

<style>
</style>