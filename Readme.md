<!-- default file list -->
*Files to look at*:

* [BO.cs](./CS/WinWebSolution.Module/BO.cs) (VB: [BO.vb](./VB/WinWebSolution.Module/BO.vb))
* **[Model.DesignedDiffs.xafml](./CS/WinWebSolution.Module/Model.DesignedDiffs.xafml) (VB: [Model.DesignedDiffs.xafml](./VB/WinWebSolution.Module/Model.DesignedDiffs.xafml))**
<!-- default file list end -->
# How to Show different views for the same object, based on the source view


<p><strong>Scenario:</strong><br>I have two business classes representing a producer and a consumer of an transaction, and a transaction class that have references to both producer and consumer. I want to be able to open (or create) a transaction from the producer's transactions list, and do not show the producer property in the detail view (it is obvious). The same behavior I want for the consumer object.</p>
<p><strong>Solution:</strong><br>To accomplish the task, create additional detail views for the transaction class, with a different layout for each case (Transaction_DetailView_FromConsumer and Transaction_DetailView_FromProducer). Then, customize the nested list view models (Consumer_Transactions_ListView and Producer_Transactions_ListView) by specifying the custom detail view in the <a href="https://documentation.devexpress.com/eXpressAppFramework/DevExpress.ExpressApp.Model.IModelListView.DetailView.property">IModelListView.DetailView</a> property.</p>
<p><strong>See Also:<br></strong><a href="https://www.devexpress.com/Support/Center/p/E274">How to provide a specific View layout for users of certain security roles</a><br><a href="https://www.devexpress.com/Support/Center/p/S35797">Core - Provide an easy way to specify a different DetailView depending on whether a new object is created, shown from the ListView or on other conditions</a></p>


<h3>Description</h3>

This solution is based on the model customization only.

<br/>


