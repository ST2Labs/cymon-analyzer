# Cymon - Cortex Analyzers

> cortex-analyzer to search information into cymon.io "Open Threat Intelligence" and obtain IP reputation info.

[[@SVTCloud]] [[SSIC - SVT Security Intelligence & Operations Center Team]] [[@st2labs]]

__Author__: Julian J. Gonzalez Caracuel - Twitter: @rhodius | @seguriadxato2 | @st2labs | @svtcloud
__Vesion__: 0.1


## Abstracts

  Cymon-Analyzer is a [Cortex Analyzers](https://github.com/CERT-BDF/Cortex-Analyzers) to obtain information about "Threats" checking cymon.io services.
  This **analyzer** help to Security Analyst what are investigate a Security Incident Case in theHive-project.org who could obtain información about observables in 1-click. 
  

__Depedencies__:

	1. python requests lib
		
		$> pip install requests
	
	2. python Cortex Utils lib
	
		$> pip install cortexutils
	
### Install Analyzers

Path to install "cortex-analyzer" could change, popular path it `/opt/Cortex-Analyzer/analyzers/` 

	1. Files what you need:
	
		- requirements.txt
		- Cymon_Check_IP.json [config file to add new analyzer in TheHive GUI]
		- config.json [config file to add Token API cymon.io]
		- cymon_analyzer.py [this is the core of analyzer]
		- cymon [folder][API Wrapper para cymon.io]
		- template [foler][ have a report template file]
		
	2. Reports Templates [Report Template Management]
		- Short template report
		- Long template report

### Testing in Cortex Server

One you have install "analyzer" you could run it and test it. You must to restart Cortex Service and access to GUI de Cortex [Cortex Engine](http://your_ip_server:9001), or you can run it from CLI/Shell like this:

	python cymon_analyzer.py <<< ' { "dataType":"ip", "data":"92.185.113.25", "config":{} }'

## License Info

	This is free software; you can redistribute it and/or modify
	it under the terms of the GNU General Public License as published by
	the Free Software Foundation version 2 of the License.
	
	This is distributed in the hope that it will be useful,
	but WITHOUT ANY WARRANTY; without even the implied warranty of
	MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
	GNU General Public License for more details.
	
	You should have received a copy of the GNU General Public License
	along it; if not, write to the Free Software
	Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA