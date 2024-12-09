---

title: 'Deployment View'
weight: 40

menu:
  main:
    name: "Deployments"
    identifier: "user-guide-cockpit-deployment-view"
    parent: "user-guide-cockpit"
    pre: "Inspect the process engine's repository, browsing deployments and resources"

---

{{< img src="../img/cockpit-deployments-page.png" title="Cockpit Deployment View" >}}

The deployment view of Cockpit shows an overview of all deployments, their resources and the content of these resources. It allows the deletion of existing deployments as well as redeployment of old resources and the creation of new deployments. The content of resources within deployments can be displayed. It is also possible to download single resources from this view.

# Search

Use the search field at the top of the list of deployments to find specific deployments. Similar to the search on the [cockpit dashboard]({{< ref "/manual/webapps/cockpit/dashboard.md#search" >}}) and in [tasklist]({{< ref "/manual/webapps/tasklist/dashboard.md#search-for-tasks" >}}), it is possible to search deployments using an array of available criteria.

Valid search criteria are unique ID, name (which does not need to be unique across all deployments), time of deployment and source. The deployment source can be provided when a deployment is created. A deployment that is created by the application during startup will have this property set to `process application`. You can also search for deployments that have no deployment source set using the `Source undefined` criterion.

Furthermore, you can copy a link to the current search query to your clipboard by clicking on the <button class="btn btn-xs"><i class="glyphicon glyphicon-link"></i></button> button and you can save search queries to your local browser storage by clicking on the <button class="btn btn-xs"><i class="glyphicon glyphicon-floppy-disk"></i></button> button and inserting a name in the drop down menu that appears. You can then retrieve the search query by clicking on the <button class="btn btn-xs"><i class="glyphicon glyphicon-floppy-disk"></i></button> button and selecting the chosen name in the drop down menu.

Independently of the search, ordering for the deployment list can be set using the sorting parameter above the search field. It is possible to order by ID, name and deployment time. Clicking on the arrow on the right side of the sorting criterion changes the ordering (ascending and descending).

# Delete

To delete a deployment, hover over the deployment  and click on the deletion icon {{< glyphicon name="trash" >}}. In the dialog that appears, you can choose to cascade the deletion (i.e., also delete running and historic process instances) and you can choose to skip custom listeners and I/O mappings. After you have completed this step, the deployment is deleted.

# Definition Resources

For resources that contain definitions (BPMN, DMN and CMMN files), a preview of the diagram or the table is displayed on the right side of the page as well as the version number of the definitions contained in this resource. At the bottom of the page, there is a list of definitions with a link to the respective definition pages.
