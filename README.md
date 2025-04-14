# Task-no.-5
Extract insights using visual and statistical exploration.
#	Titanic	Dataset:	Exploratory	Data	Analysis	Report
##	Introduction This	report	presents	the	findings	from	an	exploratory	data	analysis	(EDA)	of	the	Titanic	dataset,	which	contains	information	about	the	passengers	aboard	the	RMS	Titanic,	including	whether	they	survived	the	sinking	of	the	ship	on	April	15,	1912.	The	analysis	explores	patterns	and	relationships	in	the	data	to	better	understand	factors	that	influenced	passenger	survival.
##	Dataset	Overview The	Titanic	dataset	contains	891	records	with	12	variables: -	**PassengerId**:	Unique	identifier	for	each	passenger -	**Survived**:	Survival	status	(0	=	No,	1	=	Yes) -	**Pclass**:	Passenger	class	(1	=	1st	class,	2	=	2nd	class,	3	=	3rd	class) -	**Name**:	Passenger	name -	**Sex**:	Gender	of	passenger -	**Age**:	Age	of	passenger	(some	values	missing) -	**SibSp**:	Number	of	siblings/spouses	aboard -	**Parch**:	Number	of	parents/children	aboard -	**Ticket**:	Ticket	number -	**Fare**:	Passenger	fare -	**Cabin**:	Cabin	number	(many	missing	values) -	**Embarked**:	Port	of	embarkation	(C	=	Cherbourg,	Q	=	Queenstown,	S	=	Southampton)
##	Key	Findings
###	1.	Missing	Data -	**Age**:	19.9%	missing	values -	**Cabin**:	77.1%	missing	values -	**Embarked**:	0.2%	missing	values	(2	records)
The	high	percentage	of	missing	cabin	data	limits	analysis	of	this	feature,	while	the	missing	age	data	was	handled	appropriately	in	age-related	analyses.
###	2.	Demographic	Distribution -	**Gender**:	64.8%	male,	35.2%	female -	**Class**:	55.1%	in	3rd	class,	24.2%	in	1st	class,	20.7%	in	2nd	class -	**Age**:	Mean	age	of	29.7	years,	with	most	passengers	between	20-40	years -	**Embarkation**:	72.4%	from	Southampton,	18.9%	from	Cherbourg,	8.6%	from	Queenstown
###	3.	Survival	Patterns
####	Overall	Survival	Rate -	38.4%	(342	out	of	891)	passengers	survived	the	disaster
####	Survival	by	Gender -	**Female**:	74.2%	survival	rate -	**Male**:	18.9%	survival	rate
This	dramatic	difference	confirms	the	"women	first"	evacuation	policy	was	largely	followed.
####	Survival	by	Passenger	Class -	**1st	Class**:	62.9%	survival	rate -	**2nd	Class**:	47.3%	survival	rate -	**3rd	Class**:	24.2%	survival	rate
The	significant	gradient	in	survival	rates	across	classes	suggests	that	socioeconomic	status	played	a	major	role	in	determining	who	survived.
####	Survival	by	Age -	**Children	(0-12)**:	Higher	survival	rates,	especially	for	boys -	**Elderly	(60+)**:	Lower	survival	rates	for	men	in	this	group -	**Age	Groups	by	Gender**:	Females	in	all	age	groups	had	considerably	higher	survival	rates	than	males
####	Survival	by	Family	Size -	Passengers	in	small	family	groups	(2-4	members)	had	better	survival	rates	(around	50%) -	Passengers	traveling	alone	had	a	lower	survival	rate	(about	30%) -	Passengers	in	large	families	(5+	members)	had	the	lowest	survival	rates	(below	20%)
####	Survival	by	Embarkation	Port -	**Cherbourg**:	55.4%	survival	rate -	**Queenstown**:	38.9%	survival	rate -	**Southampton**:	33.7%	survival	rate
The	higher	survival	rate	for	Cherbourg	passengers	is	likely	related	to	passenger	class	distribution,	as	more	1st	class	passengers	embarked	there.
###	4.	Correlation	Analysis -	Strong	negative	correlation	between	passenger	class	and	survival	(-0.34) -	Moderate	positive	correlation	between	fare	and	survival	(0.26)
-	Strong	negative	correlation	between	being	male	and	survival	(-0.54) -	Moderate	correlation	between	family	size	and	survival,	with	small	families	having	positive	correlation	and	large	families	having	negative	correlation
##	Visualizations	Insights
###	Gender	and	Class	Interaction The	combination	of	gender	and	passenger	class	revealed	particularly	stark	survival	disparities: -	**1st	Class	Women**:	96.8%	survival	rate -	**2nd	Class	Women**:	92.1%	survival	rate -	**3rd	Class	Women**:	50.0%	survival	rate -	**1st	Class	Men**:	36.9%	survival	rate -	**2nd	Class	Men**:	15.7%	survival	rate -	**3rd	Class	Men**:	13.5%	survival	rate
This	pattern	shows	a	clear	hierarchy	in	evacuation	priority,	with	women	from	higher	classes	having	near-certain	survival	while	men	from	lower	classes	had	the	lowest	chances.
###	Age,	Gender,	and	Class	Interaction The	three-way	interaction	between	age,	gender,	and	class	revealed: -	Female	children	in	1st	and	2nd	class	had	100%	survival	rate -	Male	children	in	1st	and	2nd	class	had	higher	survival	rates	than	adult	males -	Adult	females	in	3rd	class	had	significantly	lower	survival	rates	than	those	in	1st	and	2nd	class -	Male	survival	rates	were	consistently	low	across	all	age	groups	in	3rd	class
###	Fare	Distribution	and	Survival -	Passengers	who	paid	higher	fares	had	better	survival	rates -	The	fare	distribution	was	highly	skewed,	with	most	passengers	paying	less	than	Â£50 -	Within	each	class,	survivors	generally	paid	higher	fares	than	non-survivors
##	Conclusions
This	exploratory	data	analysis	of	the	Titanic	dataset	reveals	several	important	insights	about	the	factors	that	influenced	passenger	survival:
1.	**Social	Hierarchy**:	The	strong	influence	of	passenger	class	on	survival	rates	reflects	the	social	stratification	of	the	early	20th	century.	First-class	passengers	had	access	to	better	information,	were	likely	closer	to	lifeboats,	and	may	have	received	preferential	treatment	during	evacuation.
2.	**Gender	Norms**:	The	"women	and	children	first"	maritime	disaster	protocol	is	clearly	reflected	in	the	data,	with	women	having	dramatically	higher	survival	rates	across	all	classes.	This	demonstrates	how	gender	norms	of	the	era	played	a	critical	role	in	determining	survival	outcomes.
3.	**Family	Dynamics**:	The	curvilinear	relationship	between	family	size	and	survival	suggests	that	traveling	with	a	small	family	was	optimal	for	survival.	Small	families	could	stay	together	and	help	each	other	during	evacuation,	while	very	large	families	may	have	found	it	difficult	to	stay	together	in	the	chaos.
4.	**Age	Considerations**:	Age	influenced	survival	mainly	in	interaction	with	gender	and	class.	Children	generally	had	better	chances,	especially	in	higher	classes,	reflecting	both	the	"women	and	children	first"	policy	and	the	social	hierarchy.
5.	**Economic	Factors**:	The	correlation	between	fare	and	survival	rate,	even	within	the	same	passenger	class,	suggests	that	economic	resources	played	a	role	beyond	the	broad	class	categories,	possibly	influencing	cabin	location	and	access	to	information	during	the	emergency.
This	analysis	provides	a	data-driven	glimpse	into	the	human	and	social	dynamics	at	play	during	one	of	history's	most	famous	maritime	disasters,	showing	how	survival	was	influenced	by	a	complex	interplay	of	demographic,	economic,	and	social	factors.	
