<template>
	<ion-grid class="shortcuts">
		<ion-row class="ion-justify-content-center">
			<ion-list class="shortcuts__list" lines="none">
				<ion-item v-for="shortcut in shortcuts" :key="shortcut.letter">
					<ion-label><Keycode :letter="shortcut.letter" :label="shortcut.label" /></ion-label>
				</ion-item>
			</ion-list>
		</ion-row>
	</ion-grid>
</template>

<script>
import {
	IonList,
	IonItem,
	IonLabel,
	IonGrid,
	IonRow
} from '@ionic/vue'

import Keycode from './Keycode.vue'

export default {
	components: {
		IonList,
		IonItem,
		IonLabel,
		IonGrid,
		IonRow,
		Keycode
	},

	data() {
		return {
			shortcuts: [
				{
					letter: '<=',
					label: 'Decrement energy'
				},
				{
					letter: '=>',
					label: 'Increment energy'
				},
				{
					letter: 'up',
					label: 'Next round'
				},
				{
					letter: 'bar',
					label: 'Reset energy'
				},
			]
		}
	}
}
</script>
