---

title: 'Dashboard'
weight: 10

menu:
  main:
    identifier: "user-guide-cockpit-dashboard"
    parent: "user-guide-cockpit"
    pre: "Entry Point to Cockpit, provides overview of cockpit sections"

---

{{< img src="../img/dashboard.png" title="Cockpit Dashboard" >}}

The dashboard of Cockpit provides a quick overview of running and historic operations as well as details about deployments.

At the top of the dashboard you can see a plugin with pie charts that display the amount of running process instances, open incidents and open human tasks.
By clicking on the number or a section of the pie chart, you are forwarded to the respective search with preselected query parameters.

On the right hand side, you see an overview of deployed process definitions, decision definitions, case definitions and the total number of deployments.

Additional [plugins]({{< ref "/manual/webapps/cockpit/extend/plugins.md" >}}) can be added to the dashboard.

# Multi Engine

{{< img src="../img/cockpit-multi-engine.png" title="Multiple Engines" >}}

If you are working with more than one engine, you can select the desired engine via a dropdown selection. Cockpit provides all information of the selected engine.
