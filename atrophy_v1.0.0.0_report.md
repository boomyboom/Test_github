json 구조 명세
============================
# WholeBrain
```json
	{
			"AtrophyIndex": 0.915153013268881,
			"ADAtrophyIndex": 0.915153013268881,
			"BrainScore": 82,
			"BrainRank" : 18,
			"AsymmetricIndex": 0.55,
			"OutlierThk": [
				0.5764691079601576,
				0.323334790123374,
				0.7369965876769332,
				0.003968480889045792,
				0.363029811671182,
				0.34173231320382524
			],
			"OutlierVol": [
				1.7671294272314395,
				1.8721038171582514,
				0.6972560243773455,
				2.065834843713206,
				1.7395574895361363,
				0.978376784576825
			]
	}
```
* `AtrophyIndex` : 대뇌 피질 위축, %.2f, 1 page(Summary), 3 page(Atrophy(cortex)) Atrophy(Whole)에 출력
* `ADAtrophyIndex` : AD 취약 부분 위축, %.2f, 1 page(Summary)에 출력
* `BrainScore` : 연령대비 뇌 건강 점수, %.0f, 1 page(Summary)에 출력
* `BrainRank` : 등수, 1 page(Summary)에 출력
* `AsymmetricIndex` : 대뇌 비대칭 지수, %.2f, 1 page(Summary), 5 page(Cerebral Asymmetry) Asymmetry Index에 출력
* `OutlierThk` : 정상 범위 밖 두께, 1 page(Summary)에 출력
	* [전두엽, 두정엽, 측두엽, 후두엽, 뇌도, 대상회] 순으로 표시
	* 각 각 -1.0 미만이면 색으로 표시
	* -1.0 미만인 영역 개수 출력
* `OutlierVol` : 정상 범위 밖 부피, %.2f, 1 page(Summary)에 출력
	* [전뇌, 피질하, 회백질, 백질, 소뇌, 측뇌실] 순으로 표시
	* 각 각 -1.0 미만이면 색으로 표시
	* -1.0 미만인 영역 개수 출력

# Thickness
```json
	{
		"thickness": [
			"2.4887283",
			"2.4620497"
		],
		"FrontalLobe": [
			0.701844278081426,
			0.4525052581373462
		],
		"ParietalLobe": [
			0.4419009761401627,
			0.20846255737878075
		],
		"TemporalLobe": [
			0.8382466152547612,
			0.6350131534738003
		],
		"OccipitalLobe": [
			0.05811427880826611,
			-0.05346233014916611
		],
		"Cingulate": [
			0.42672956886236185,
			0.25097414418452474
		],
		"Insula": [
			0.391190708524644,
			0.33409988443213423
		]
	}
```

* `thickness` : 대뇌 피질 두께, %.2f, 1 page(Summary)에 출력
	* [좌뇌, 우뇌] 순으로 출력
* `FrontalLobe` : Frontal lobe, %.2f, 3page(Atrophy(cortex))에 출력
	* [좌, 우] 순으로 출력
* `ParietalLobe` : Parietal lobe, %.2f, 3page(Atrophy(cortex))에 출력
	* [좌, 우] 순으로 출력
* `TemporalLobe` : Temporal lobe, %.2f, 3page(Atrophy(cortex))에 출력
	* [좌, 우] 순으로 출력
* `OccipitalLobe` : Occipital lobe, %.2f, 3page(Atrophy(cortex))에 출력
	* [좌, 우] 순으로 출력
* `Cingulate` : Cingulate, %.2f, 3page(Atrophy(cortex))에 출력
	* [좌, 우] 순으로 출력
* `Insula` : Insula, %.2f, 3page(Atrophy(cortex))에 출력
	* [좌, 우] 순으로 출력

# Volume
```json
	{
		"TotalBrain": [
			1.7671294272314395
		],
		"GreyMatter": [
			0.6434859499656934,
			0.7439456257398903
		],
		"WhiteMatter": [
			2.0361712482241807,
			2.0838517010172155
		],
		"Cerebellum": [
			1.465751624815987,
			1.9645961176522355
		],
		"LateralVentricle": [
			-0.9389602268864258,
			-0.9677820355404364
		],
		"SubCortexGM": [
			1.9069823854347607,
			1.5993227987721792
		]
	}
```
* `TotalBrain` : Total brain volume, %.2f, 4 page(Atrophy(volume))에 출력
* `GreyMatter` : Grey matter, %.2f, 4 page(Atrophy(volume))에 출력
	* [좌, 우] 순으로 출력
* `WhiteMatter` : White matter, %.2f, 4 page(Atrophy(volume))에 출력
	* [좌, 우] 순으로 출력
* `Cerebellum` : Cerebellum, %.2f, 4 page(Atrophy(volume))에 출력
	* [좌, 우] 순으로 출력
* `LateralVentricle` : Lateral ventricle, %.2f, 4 page(Atrophy(volume))에 출력
	* [좌, 우] 순으로 출력
* `SubCortexGM` : Subcortical grey matter, %.2f, 4 page(Atrophy(volume))에 출력
	* [좌, 우] 순으로 출력

# AsymmetryIndex
```json
	{
		"FrontalLobe": 1.1014549842342882,
		"TempotalLobe": 2.47852498013305,
		"ParietalLobe": 1.0365911677319206,
		"OccipitalLobe": -0.6358749719311395,
		"CerebellumCortex": -0.02548411462562188,
		"Thalamus": -0.02885904342767538,
		"Caudate": -0.017965480732063947,
		"Putamen": 0.01348361428330469,
		"Pallidum": 0.09108200406345913,
		"Hippocampus": -0.017400893841778356,
		"Amygdala": 0.014091888429511468,
		"Accumbens": 0.0060702557468405045
	}
```
* `FrontalLobe` : Frontal lobe, %.2f, 5 page(Cerebral Asymmetry)에 출력
* `TemporalLobe` : Temporal lobe, %.2f, 5 page(Cerebral Asymmetry)에 출력
* `ParietalLobe` : Parietal lobe, %.2f, 5 page(Cerebral Asymmetry)에 출력
* `OccipitalLobe` : Occipital lobe, %.2f, 5 page(Cerebral Asymmetry)에 출력
* `CerebellumCortex` : Cerebellum-Cortex, %.2f, Deep Analysis - 4 page에 출력
* `Thalamus` : Thalamus-Proper, %.2f, Deep Analysis - 4 page에 출력
* `Caudate` : Caudate, %.2f, Deep Analysis - 4 page에 출력
* `Putamen` : Putamen, %.2f, Deep Analysis - 4 page에 출력
* `Pallidum` : Pallidum, %.2f, Deep Analysis - 4 page에 출력
* `Amygdala` : Amygdala, %.2f, Deep Analysis - 4 page에 출력
* `Accumbens` : Accumbens-area, %.2f, Deep Analysis - 4 page에 출력

