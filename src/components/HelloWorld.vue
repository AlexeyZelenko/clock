<template>
	<div>
		<Vue3CountdownClock/>
		<p>11</p>
	</div>
</template>

<script>
    import { defineComponent, ref, provide } from '@vue/composition-api'
    import Vue3CountdownClock from 'vue3-countdown-clock'

    export default defineComponent({
        name: 'HelloWorld',
        components: {
            Vue3CountdownClock
        },
        setup () {
            const deadLine = ref('2021/12/06 10:00:00 GMT-0200')
            provide('deadline', deadLine)

            const Title = ref('Online service will be honored through:')
            provide('title', Title)

            const timerStyle = ref({
                'text-align': 'center',
                'font-family': 'sans-serif',
                'font-weight': 100
            })
            provide('timerStyle', timerStyle)

            const h1Style = ref({
                color: '#396',
                'font-weight': 100,
                'font-size': '40px',
                margin: '40px 0px 20px'
            })
            provide('h1Style', h1Style)

            const clockdiv = ref({
                'font-family': 'sans-serif',
                color: '#fff',
                display: 'inline-block',
                'font-weight': 100,
                'text-align': 'center',
                'font-size': '30px'
            })
            provide('clockdiv', clockdiv)

            const clockdivDiv = ref({
                padding: '10px',
                'border-radius': '3px',
                background: '#00BF96',
                display: 'inline-block',
                margin: '1px'
            })
            provide('clockdivDiv', clockdivDiv)

            const clockdivDivSpan = ref({
                padding: '15px',
                'border-radius': '3px',
                background: '#00816A',
                display: 'inline-block'
            })
            provide('clockdivDivSpan', clockdivDivSpan)

            const styleEndTime = ref({
                color: '#fff'
            })
            provide('styleEndTime', styleEndTime)

            const smalltext = ref({
                'padding-top': '5px',
                'font-size': '16px'
            })
            provide('smalltext', smalltext)

            const titleDays = ref('Days')
            provide('titleDays', titleDays)

            const titleHours = ref('Hours')
            provide('titleHours', titleHours)

            const titleMinutes = ref('Minutes')
            provide('titleMinutes', titleMinutes)

            const titleSeconds = ref('Seconds')
            provide('titleSeconds', titleSeconds)

            const titleEndTime = ref('End Time!')
            provide('titleEndTime', titleEndTime)
        }
    })
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
