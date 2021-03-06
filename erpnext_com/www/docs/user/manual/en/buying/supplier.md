<!-- add-breadcrumbs -->
# Supplier

Suppliers are companies or individuals who provide you with products or services.

### 1. How to create a Supplier
1. You can create a new Supplier from:
**Buying > Supplier > Supplier > New**
2. Enter a name for the supplier.
4. Select the supplier group whether Pharmaceutical, Hardware etc.
5. Save.
<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-master.png">

### 2. Features

In the Supplier master you can add all regular information related to the supplier as well like Tax ID, Billing Currency, Price List and Payment Terms. So that in all future transactions, these default values will populate in the forms.  

You can also choose a default Supplier Type and add a new type if you want to. 

Each Supplier can have a default price list so that every time when you buy a new item from the supplier, the supplier price list would be updated as well. 


#### 2.1 Contacts and Addresses

Contacts and Addresses in ERPNext are stored separately so that you can create multiple Contacts and Addresses for a Supplier. Once Supplier is saved, you will find the option to create Contact and Address for that Supplier.

<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-new-address-contact.png">

> Tip: When you select a Supplier in any transaction, Contact for which "Is Primary" field id checked, it will auto-fetch with the Supplier details.

#### 2.2 Integration with Accounts

For all the Supplier, "Creditor" account is set as default payable Account. When Purchase Invoice is created, payable towards the supplier is booked against "Creditors" account.

If you want to customize payable account for the Supplier, you should first add a payable Account in the Chart of Account, and then select that Payable Account in the Supplier master.

<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-payable-account.png">

If you don't want to customize payable account, and proceed with default payable account "Creditor", then do not update any value in the Default Supplier Account's table.

> Advanced Tip: Default Payable Account is set in the Company master. If you want to set another account as Account as default for payable instead of Creditors Account, go to Company master, and set that account as "Default Payable Account".

You can add multiple companies in your ERPNext instance, and one Supplier can be used across multiple companies. In this case, you should define Companywise Payable Account for the Supplier in the "Default Payable Accounts" table.

<div>
    <div class='embed-container'>
        <iframe src='https://www.youtube.com/embed//zsrrVDk6VBs?start=213' frameborder='0' allowfullscreen>
        </iframe>
    </div>
</div>

#### 2.3 Place Supplier On Hold
In the Supplier form, check the "Block Supplier" checkbox. Next, choose the "Hold Type".

The hold types are as follows:
- Invoices: ERPNext will not allow Purchase Invoices or Purchase Orders to be created for the supplier
- Payments: ERPNext will not allow Payment Entries to be created for the Supplier
- All: ERPNext will apply both hold types above

After selecting the hold type, you can optionally set a release date in the "Release Date" field.

Take note of the following:
- If you do not select a hold type, ERPNext will set it to "All"
- If you do not set a release date, ERPNext will hold the Supplier indefinitely 

#### 3. Related Topics
1. [Supplier Quotation](/docs/user/manual/en/buying/supplier-quotation)
1. [Supplier Scorecard](/docs/user/manual/en/buying/supplier-scorecard)
1. [Maintaining Supplier's Item Code In the Item Master](/docs/user/manual/en/buying/articles/maintaining-suppliers-part-no-in-item)
1. [Pull Items In Purchase Order Based On Supplier](/docs/user/manual/en/buying/articles/pull-items-in-purchase-order-based-on-supplier)