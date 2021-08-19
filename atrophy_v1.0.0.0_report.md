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

# 심화분석 - Cerebral cortex
```json
	"FrontalLobeScore": {
		"caudalmiddlefrontal": [
			0.30066167788032516,
			0.0628642569278635
		],
		"lateralorbitofrontal": [
			0.8290832108646571,
			1.0583153179384372
		],
		"medialorbitofrontal": [
			1.219031386500153,
			0.7172061505625238
		],
		"paracentral": [
			-0.031650587789300876,
			-0.24072072964783844
		],
		"parsopercularis": [
			0.6844743651864266,
			0.14686055578458165
		],
		"parsorbitalis": [
			0.9129498609894134,
			1.0638700012660816
		],
		"parstriangularis": [
			0.01698547590808796,
			0.9050975178875137
		],
		"precentral": [
			0.26133940238143677,
			0.06928442148290888
		],
		"rostralmiddlefrontal": [
			1.0278239820006514,
			0.7687524836005405
		],
		"superiorfrontal": [
			1.1644034810730914,
			0.5664532436339064
		]
	}
```
* `caudalmiddlefrontal` : Frontal Lobe - caudalmiddlefrontal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `lateralorbitofrontal` : Frontal Lobe - lateralorbitofrontal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `medialorbitofrontal` : Frontal Lobe - medialorbitofrontal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `paracentral` : Frontal Lobe - paracentral, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `parsopercularis` : Frontal Lobe - parsopercularis, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `parsorbitalis` : Frontal Lobe - parsorbitalis, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력 
* `parstriangularis` : Frontal Lobe - parstriangularis, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력 
* `precentral` : Frontal Lobe - precentral, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력 
* `rostralmiddlefrontal` : Frontal Lobe - rostralmiddlefrontal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력 
* `superiorfrontal` : Frontal Lobe - superiorfrontal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력

```json
	"ParietalLobeScore": {
		"inferiorparietal": [
			0.2912457029772609,
			0.4594985540867406
		],
		"precuneus": [
			0.6346931615452372,
			0.21346190724708836
		],
		"superiorparietal": [
			0.25400498500190355,
			0.03909119158978016
		],
		"supramarginal": [
			0.8805509610745997,
			0.27225024585221863
		],
		"postcentral": [
			0.2285521975951892,
			0.07085589516502211
		]
	}
```
* `inferiorparietal` : Parietal Lobe - inferiorparietal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `precuneus` : Parietal Lobe - precuneus, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `superiorparietal` : Parietal Lobe - superiorparietal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `supramarginal` : Parietal Lobe - supramarginal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `postcentral` : Parietal Lobe - postcentral, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력

```json
	"TemporalLobeScore": {
		"inferiortemporal": [
			-0.14104406411629208,
			1.8175500328420555
		],
		"middletemporal": [
			0.8019610039229765,
			0.1504795598074567
		],
		"superiortemporal": [
			0.6113995175907659,
			0.6164833930784768
		],
		"transversetemporal": [
			0.7935749102316455,
			0.2935962766900145
		],
		"entorhinal": [
			0.7621553129427626,
			0.7630919066160398
		],
		"parahippocampal": [
			1.4143054576775038,
			1.0769437302564755
		],
		"fusiform": [
			1.0256746902830667,
			1.1430227378488664
		]
	}
```
* `inferiortemporal` : Temporal Lobe - inferiortemporal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `middletemporal` : Temporal Lobe - middletemporal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `superiortemporal` : Temporal Lobe - superiortemporal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `transversetemporal` : Temporal Lobe - transversetemporal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `entorhinal` : Temporal Lobe - entorhinal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `parahippocampal` : Temporal Lobe - parahippocampal, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력
* `fusiform` : Temporal Lobe - fusiform, %.2f, Deep Analysis - 1 page에 출력
	* [좌, 우] 순으로 출력

```json
	"OccipitalLobeScore": {
		"cuneus": [
			0.35910277550798236,
			0.273711927356238
		],
		"lateraloccipital": [
			-0.430090735828203,
			-0.17658081898097108
		],
		"lingual": [
			0.6602994605390397,
			0.0731023462955118
		],
		"paricalcarine": [
			0.10594892816370322,
			-0.21506339156736395
		]
	}
```
* `cuneus` : Occipital Lobe - cuneus, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력
* `lateraloccipital` : Occipital Lobe - lateraloccipital, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력
* `lingual` : Occipital Lobe - lingual, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력
* `paricalcarine` : Occipital Lobe - paricalcarine, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력

```json
	"Cingulate": {
		"caudalanteriorcingulate": [
			0.2530831861921902,
			0.41500881374352827
		],
		"isthmuscingulate": [
			0.06191395555651499,
			-0.07152716582692843
		],
		"posteriorcingulate": [
			0.6959042323426833,
			0.26760937980379546
		],
		"rostralanteriorcingulate": [
			0.6445821696125439,
			0.6853789816844066
		]
	}
```
* `caudalanteriorcingulate` : Cingulate - caudalanteriorcingulate, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력
* `isthmuscingulate` : Cingulate - isthmuscingulate, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력
* `posteriorcingulate` : Cingulate - posteriorcingulate, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력
* `rostralanteriorcingulate` : Cingulate - rostralanteriorcingulate, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력

```json
	"insula": {
		"insula": [
			0.391190708524644,
			0.33409988443213423
		]
	}
```
* `insula` : Insula - insula, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력

```json
	"Subcortex": {
		"cerebellum-cortex": [
			57799.6,
			0.03609548223360642,
			0.048360298430287475,
			61047.4,
			0.03812371265731709,
			0.051077697464915535
		],
		"Thalamus": [
			7679.2,
			0.004795611512334176,
			0.006425103352027758,
			8135.6,
			0.0050806304067801235,
			0.0068069682819508585
		],
		"Caudate": [
			2921.7,
			0.0018245830497430411,
			0.00244455470148186,
			3028.6,
			0.0018913414191914892,
			0.0025339967720532435
		],
		"Putamen": [
			5107.4,
			0.0031895387850421355,
			0.004273306185559247,
			4971.5,
			0.003104670100214782,
			0.004159600129519481
		],
		"Pallidum": [
			2524.0,
			0.0015762219315985336,
			0.0021118034249033835,
			2102.6,
			0.001313060314334024,
			0.001759222615373159
		],
		"Hippocampus": [
			4232.3,
			0.002643044406142819,
			0.003541119506821945,
			4382.2,
			0.0027366560018427474,
			0.003666539211018861
		],
		"Amygdala": [
			1741.5,
			0.001087555663184963,
			0.0014570941618340895,
			1693.1,
			0.0010573301713112033,
			0.0014165984067765127
		],
		"Accumbens": [
			505.5,
			0.0003156815318633355,
			0.0004229463673885342,
			499.4,
			0.0003118721206974278,
			0.00041784256354863297
		]
	}
```
* `cerebellum-cortex` : Subcortex - cerebellum-cortex, %.2f, Deep Analysis - 2 page에 출력
	* [좌, 우] 순으로 출력
