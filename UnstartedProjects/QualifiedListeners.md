# Project Summary

Qualified Listeners is looking for a database to track interactions with veterans they service and to track how many volunteers they've contacted. They already have a WordPress site, so I suspect the easiest way to do this would be to add this as a small WordPress plugin. Those details need not be fixed if a much different implementations strategy is favored.

# What is Qualified Listeners?

Qualified Listeners (QL) is a relatively young northern Colorado (and southern Wyoming) nonprofit which seeks to serve military veterans in the community by giving them a listening and interested ear. They also produce a virtual and print service directory for veterans (irrelevant to this project, but good to know exists).

# Relevant Project Details

* QL is already on a WordPress site. Using a few new database tables in the WordPress database (using `$wpdb`) is probably best way to tackle expedience and robustness. This way the data can be extracted from MySQL for analysis, and is not constrained by WordPress data-saving conventions. 
* QL is looking to track two core entities:
	- Listening Sessions: will likely include data fields like:
		* time of meeting
		* volunteer name
		* miles traveled by volunteer (for reimbursement)
	- Contacted Veterans
		* name
		* phone number
		* location
		* combat experience
* If the WordPress-centric model is used, making each voluteer/listener a WordPress user account, and giving them access to fill out the form on front-end or back-end page is probably the simplest structure.
* Only WP Admins should probably have access to reports, but interesting and valuable figures to report on are:
	- Listening sessions held over the last month/year
	- Total veterans contacted (overall and this year)
	- Miles traveled by each volunteer (used to reimburse them for milage)