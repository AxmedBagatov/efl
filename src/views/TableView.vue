<template>
	<div class="ptable">
		<h1 class="headin">Турнирная таблица</h1>
		<table class="resultTable">
			<tr class="col">
				<th>#</th>
				<th class="pros">Команда</th>
				<th>Игр</th>
				<th>В</th>
				<th>П</th>
				<th>Н</th>
				<th>Раз</th>
				<th>Очки</th>
			</tr>
			<tr v-for="(result, index) in sortedPoints" :key="result.Points" class="wpos">
				<td>{{ index + 1}}</td>
				<td class="pros">{{ result.team }}</td>
				<td>{{ result.games }}</td>
				<td>{{ result.win }}</td>
				<td>{{ result.loss }}</td>
				<td>{{ result.draw }}</td>
				<td>{{ result.goalDifferense }}</td>
				<td>{{ result.Points }}</td>
			</tr>
		</table>
		<div class="top">
			<table class="toptable">
				<th>ТОП</th>
				<tr class="trtop"><td>1</td><img src="../assets/EFL-2.png"></tr>
				<tr><td>1</td>2</tr>
				<tr><td>1</td>3</tr>
				<tr><td>1</td>4</tr>
				<tr><td>1</td>5</tr>
				<tr><td>1</td>6</tr>
			</table>
			<table class="toptable">
				<th>ТОП</th>
				<tr class="trtop"><td>1</td><img src="../assets/EFL-2.png"></tr>
				<tr><td>1</td>2</tr>
				<tr><td>1</td>3</tr>
				<tr><td>1</td>4</tr>
				<tr><td>1</td>5</tr>
				<tr><td>1</td>6</tr>
			</table>
			<table class="toptable">
				<th>ТОП</th>
				<tr class="trtop"><td>1</td><img src="../assets/EFL-2.png"></tr>
				<tr><td>1</td>2</tr>
				<tr><td>1</td>3</tr>
				<tr><td>1</td>4</tr>
				<tr><td>1</td>5</tr>
				<tr><td>1</td>6</tr>
			</table>

		</div>
	</div>
</template>

<script>

export default {
	name: 'table',
	data() {
		return {
			teamResult: [
				{

					team: 'Туран',
					games: 14,
					win: 12,
					draw: 0,
					loss: 2,
					goalDifferense: 68,
					Points: 36,
				},
				{
					team: 'Братсво',
					games: 16,
					win: 13,
					draw: 0,
					loss: 3,
					goalDifferense: 56,
					Points: 39,
				},
				{

					team: 'Бейрут',
					games: 14,
					win: 12,
					draw: 0,
					loss: 2,
					goalDifferense: 56,
					Points: 36,
				},
				{

					team: 'Ханиф',
					games: 15,
					win: 10,
					draw: 1,
					loss: 4,
					goalDifferense: 28,
					Points: 31,
				},
				{

					team: 'Завод аул',
					games: 16,
					win: 4,
					draw: 2,
					loss: 10,
					goalDifferense: -35,
					Points: 14,
				},
				{

					team: 'Легион',
					games: 15,
					win: 7,
					draw: 0,
					loss: 8,
					goalDifferense: -9,
					Points: 21,
				},
				{

					team: 'Бирлик',
					games: 15,
					win: 6,
					draw: 1,
					loss: 8,
					goalDifferense: -3,
					Points: 19,
				},
				{

					team: 'Эндери',
					games: 15,
					win: 6,
					draw: 1,
					loss: 8,
					goalDifferense: -16,
					Points: 19,
				},
				{

					team: 'Риджаль',
					games: 15,
					win: 3,
					draw: 3,
					loss: 9,
					goalDifferense: -25,
					Points: 12,
				},
				{

					team: 'Оьр Аул',
					games: 16,
					win: 4,
					draw: 0,
					loss: 12,
					goalDifferense: -41,
					Points: 12,
				},
				{

					team: 'Солтан мут',
					games: 15,
					win: 1,
					draw: 2,
					loss: 12,
					goalDifferense: -79,
					Points: 5,
				},],
			currentSort: 'Points',
			currentSortDir: 'desc'
		}
	},
	methods: {
		sort: function (s) {
			//if s == current sort, reverse
			if (s === this.currentSort) {
				this.currentSortDir = this.currentSortDir === 'asc' ? 'desc' : 'asc';
			}
			this.currentSort = s;
		}
	},
	computed: {
		sortedPoints: function () {
			return this.teamResult.sort((a, b) => {
				let modifier = 1;
				if (this.currentSortDir === 'desc') modifier = -1;
				if (a[this.currentSort] < b[this.currentSort]) return -1 * modifier;
				if (a[this.currentSort] > b[this.currentSort]) return 1 * modifier;
				return 0;
			});
		}
	},
}
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Fjalla+One");

* {
	font-family: Fjalla One;
	margin: 0;
	border: 0;
	padding: 0;
	color: white;
}

html{
	height: 100%;
}



@keyframes color-change-2x {
	0% {
		background: #000000;
	}

	100% {
		background: #011708;
	}
}

.top {
	margin-block-start: 10%;
	display: flex;	
	justify-content: end;
}

.toptable {
	text-align: center;
	margin-left: auto;
    margin-right: auto;
	vertical-align: middle;
}

td{
	
}

trtop{
	height: 50px;
}

.ptable table {
	margin: auto;
	border-collapse: collapse;
	animation-name: color-change-2x;
}

.ptable {
	margin: 0px 0% 30px 0%;
	width: 100%;
	background: rgb(0, 0, 0);
	height: 100%;
		
}

.pros {
	text-align: left;
	margin: 0;
}

th,
td {
	padding: 10px;
}

th {
	/* background-color: black; */
	color: #ffe221;
}

.headin {
	text-align: center;
	text-decoration: none;
	color: #ffe221;
	margin: 30px;
	margin-block-start: 0px;
	display: block;
}

.wpos {
	text-align: center;
}

.routPoint {
	color: #77ff21;
	text-decoration: none;
	display: block;
	color: rgb(240, 20, 20);
}

.routPoint:hover {
	cursor: pointer;
	color: #000000;
}

.wpos td {
	color: #77ff21;
}

.pos {
	text-align: center;
}

.pos td {
	color: #ff7b21;
}


p {
	color: white;
}



table .col {
	border-bottom: 1px solid #FFFFFF;
}

.resultTable{
	width: 80%;
}

.resultTable tr:hover:nth-child(n+5) {
	background-color: #ff7b21;
}

.resultTable tr:hover:nth-child(n+11) {
	background-color: #ff0000;
}

.wpos:hover {
	background-color: #77ff21;
}

.wpos:hover td {
	color: #000000;
}
</style>