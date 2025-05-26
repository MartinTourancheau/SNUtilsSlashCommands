# Slashcommand Archive
  This repo serves as my personal archive of slashcommand that I can't live without since I'm often switching client remote desktops and laptops and wanted a easy place to go to import them all at once. There is a [slashcommands.json](slashcommands.json) file that you can use to import the commands in bulk, and I've written a quick GitHub action to list them out one by one below so they can be grabbed a la cart. 












## Wiki

### /us

*Filter Update Set <name>*

Search for Update set by name.

<pre><code>sys_update_set_list.do?sysparm_query=nameLIKE$1^ORDERBYDESCsys_updated_on</code></pre>

---

### /sc

*Filter Cat Item <name>*

Search for Catalog Item by name.

<pre><code>sc_cat_item_list.do?sysparm_query=nameLIKE$0</code></pre>

---

### /r

*Filter Roles <search>*

Search for roles by name.

<pre><code>sys_user_role_list.do?sysparm_query=nameLIKE$0</code></pre>

---

### /g

*Filter Groups <search>*

Search for user groups by name.

<pre><code>sys_user_group_list.do?sysparm_query=nameLIKE$0</code></pre>

---

### /notif

*Filter Notification <search>*

Search for notifications by name.

<pre><code>sysevent_email_action_list.do?sysparm_query=nameLIKE$0</code></pre>

---

### /ds

*Filter Data Source <name>*

Search for data sources by name.

<pre><code>sys_data_source_list.do?sysparm_query=nameLIKE$0</code></pre>

---

### /dico

*Dico Search <search>*

Search dictionary by name or element.

<pre><code>sys_dictionary_list.do?sysparm_query=nameLIKE$0^ORelementLIKE$0</code></pre>

---

### /exec

*Flow engine contexts of current record*

Flow engine contexts of current record.

<pre><code>sys_flow_context_list.do?sysparm_query=source_record=$sysid</code></pre>

---

### /lognow

*Search log*

Search logs from the last 15 minutes.

<pre><code>syslog_list.do?sysparm_query=sys_created_onONLast%2015%20minutes@javascript:gs.beginningOfLast15Minutes()@javascript:gs.endOfLast15Minutes()^messageLIKE$0^ORsourceLIKE$0</code></pre>

---

### /nus

*New Update set*

Open a new update set.

<pre><code>sys_update_set.do?sys_id=-1</code></pre>

---

### /cus

*Current update set*

Open current update set.

<pre><code>sys_update_set.do?sys_id=javascript:gs.getPreference('sys_update_set')</code></pre>

---

### /duplicate

*Dupliquer la page*

Duplicate the current page.

<pre><code>//env</code></pre>

---

### /try

*Try cat item in portal*

Open catalog item in portal.

<pre><code>/$0?id=sc_cat_item&sys_id=$sysid</code></pre>

---

### /en

*switch to english*

Switch language to English.

<pre><code>//lang en</code></pre>

---

### /fr

*Basculer en français*

Switch language to French.

<pre><code>//lang fr</code></pre>

---

### /msg

*Traduction de message*

Search message translations.

<pre><code>sys_ui_message_list.do?sysparm_query=messageLIKE$0%5EORkeyLIKE$0</code></pre>

---

### /bgd

*Prompt pour dupliquer le record courant*

Duplicate current record script.

<pre><code>/sys.scripts.do?content=var%20current%20%3D%20new%20GlideRecord%28%22$table%22%29%3B%0Aif%20%28current.get%28%22$sysid%22%29%29%7B%0A%20%20%20%20gs.info%28current.getDisplayValue%28%29%29%3B%0A%2F%2Fstuff%0A%2F%2Fcurrent.number%20%3D%20new%20NumberManager%28%22$table%22%29.getNextObjNumberPadded%28%29%3B%0A%0A%2F%2Fcurrent.insert%28%29%3B%0A%7D</code></pre>

---

### /w

*Widgets <name or id>*

Search for widgets by name or ID.

<pre><code>sp_widget_list.do?sysparm_query=nameLIKE$0^ORidLIKE$0^ORDERBYDESCsys_updated_on</code></pre>

---

### /stats

*Stats.do*

Open instance stats.

<pre><code>/stats.do</code></pre>

---

### /sla

*SLA Definitions <name>*

Search SLA definitions.

<pre><code>contract_sla_list.do?sysparm_query=nameLIKE$0^ORDERBYDESCname</code></pre>

---

### /retrieve

*Remote Instances <search>*

Retrieve update set sources.

<pre><code>sys_update_set_source_list.do?sysparm_query=^ORDERBYname</code></pre>

---

### /sj

*Scheduled Jobs <name>*

Search scheduled jobs.

<pre><code>sysauto_list.do?sysparm_query=nameLIKE$0^ORDERBYname</code></pre>

---

### /fix

*Fix Scripts <name>*

Search fix scripts.

<pre><code>sys_script_fix_list.do?sysparm_query=nameLIKE$0^ORDERBYname</code></pre>

---

### /upa

*UI Policy Actions <field>*

Search UI policy actions.

<pre><code>sys_ui_policy_action_list.do?sysparm_query=fieldLIKE$0^ORDERBYfield</code></pre>

---

### /case

*Filter Cases <number>*

Search Customer Service cases.

<pre><code>sn_customerservice_case_list.do?sysparm_query=numberLIKE$0</code></pre>

---

### /incident

*Filter Incidents <number>*

Search incidents.

<pre><code>incident_list.do?sysparm_query=numberLIKE$0</code></pre>

---

### /req

*Filter Requests <number>*

Search service requests.

<pre><code>sc_request_list.do?sysparm_query=numberLIKE$0</code></pre>

---

### /ritm

*Filter RITM <number>*

Search RITM records.

<pre><code>sc_req_item_list.do?sysparm_query=numberLIKE$0</code></pre>

---

### /sctask

*Filter SC Task <number>*

Search Service Catalog Tasks.

<pre><code>sc_task_list.do?sysparm_query=numberLIKE$0</code></pre>

---

### /wo

*Filter WO <number>*

Search Work Orders.

<pre><code>wm_order_list.do?sysparm_query=numberLIKE$0</code></pre>

---

### /wot

*Filter WOT <number>*

Search Work Order Tasks.

<pre><code>wm_task_list.do?sysparm_query=numberLIKE$0</code></pre>

---

