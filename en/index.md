---
title: Cash book and cash orders for Microsoft Dynamics 365 Business Central
owner: FTS Bulgaria
redirect_from:
  - /
---

[Terms of use](../FTS Standard Agreement.pdf)<br/>
[Full Version on PDF](../FTS Cash Book_ENU.pdf)<br/>
[Ръководство на български](../bg/index.html)  

# **Table of Contents**

[1. Summary](#summary)\
[2. Cash Report and cash orders](#cash-report-and-cash-orders)\
[2.1. Cash report](#cash-report)\
[2.2. Cash receipt / Cash withdrawal](#cash-receipt-cash-withdrawal)

# Summary

The Cash Report package is an addition to the Microsoft Dynamics 365
Business Central product. It was developed by FTS for the needs of users
and companies operating in Bulgaria and using D365 Business Central.

The Cash Report package complies with the requirements of the
legislation in the country and covers the necessary regulatory
requirements.

# Cash Report and cash orders

## Cash report

The cash book is accessible both through the Search button in the
Navigation Bar and through the Cash Desk:

![A screenshot of a computer Description automatically
generated](.\/media/image1.png)

From the cash desk a new cash book is created by pressing Cash Reports
button:

![A screenshot of a computer Description automatically
generated](.\/media/image2.png)

The following data could be populated in Cash Report:

Tab **General**

> • **Cashier No.** - code of the cashier, to which a cash report is
> created;
>
> • **No** - the system automatically gives a cash report number,
> according to the number series that is set in the cashier card;
>
> • **Currency code** -- the currency code is copied from the cashier
> card;
>
> • **Opening Date** - the system fills in the working date with which
> the user works;
>
> • **Starting balance** -- shows the balance at the cash desk at the
> time of opening the cash report in the relevant currency of the
> cashier. The field is locked for editing;

-   **Net Change/Net Change (LCY)** -- indicates daily cashier turnover
    while the report was open. Fields are locked for editing;

-   **Ending Balance** -- the field shows the final balance (sum of the
    opening balance and net changes) in the cashier. The field is locked
    for editing;

-   **Amount Denomination** - the user enters a denomination of the
    amount by clicking the Denomination button in the menu. The aim is
    to specify the physical quantity of coins and banknotes that were
    present in the cashier at the time of closing the cash report. The
    system displays a page with the monetary denominators, which are
    filled in for this currency code. The user fills in the quantities
    by automatically recalculating them. After the user clicks OK, the
    system updates the Amount Denomination field on the cash statement
    card;

**\*IMPORTANT** -- The system will check the Ending Balance and the
Denominated Amount and will display a discrepancy message in case of
incomparison.

Tab **Cash Report Lines** -- rows cannot be edited.

Cash statement lines are filled in depending on the posting level setup
from the cashier card :

> • Cash Order Posting Level -- the system fills the cash statement
> lines with title information of the Posted Cash Orders;
>
> • Cash statement posting level -- the system fills the cash report
> lines with header information of the Issued Cash Orders;

Closing the cash report at the end of each business day is done by
selecting the **Close** button from the menu. Depending on the posting
level, different actions will be applied when closing a Cash Report:

-   Cash posting level Cash order -- the system changes the status of
    the Cash Report and locks it for editing. No further action is
    needed as cash orders have already been posted;

-   Cash posting level Cash Desk Report -- the system publishes all
    issued cash orders that appear as Cash Desk Report lines and then
    changes the status of Cash Desk Report and locks it for editing;

If a correction is needed to be made to the already closed cash report,
the user can reopen it by selecting the **Reopen** button. This will
allow the user to publish additional cash orders for that day.

NOTE: Since there can only be one cash report open for the respective
cashier, reopening can happen, but only if there is no next cash report
open for that cashier.

The Cash report could be printed using the **Print** button.

## Cash receipt / Cash withdrawal

From the list with the Cash Desk accounts user should choose the one for
the transactions:

![A screenshot of a computer Description automatically
generated](.\/media/image3.png)

There is an opportunity to create a new cash book for the day, if one
has not already been created. After the creation of the cash book, the
creation of Cash Receipt and Cash Withdrawal is started, which is done
from the cashier card

![A screenshot of a computer Description automatically
generated](.\/media/image4.png)

a)  **Cash Withdrawal** -- The system loads a number from the number
    series, which is selected in Cash Desk Card. Cash withdrawal card
    can be created for payment on an invoice to a supplier, account
    expense, transfer of funds to a bank, cashier, accountable person,
    etc.

![A screenshot of a computer Description automatically
generated](.\/media/image5.png)

b)  **Cash Receipt**

![A screenshot of a computer Description automatically
generated](.\/media/image6.png)

Tab **General (The fields are similar between the two types of
documents)**

-   **Cash desk No** - code of the cashier to which the cash order is
    created;

-   **No** - the system automatically assigns an order number (Cash
    Withdrawal or Cash Receipt), according to the number series that is
    set in the cashier card (bank account);

-   **Pay-to / Receive-from Name** -- the user enters the name of the
    person/company from whom cash is received or paid;

-   **Description** - the user enters a short description;

-   **Currency code** - the currency code is copied from the cashier
    card;

-   **Posting date** - the system fills in the working date with which
    the user works;

-   **Correction** - the user checks this box to mark this cash order as
    a correction. This setting will result in reverse posting on the
    posted amount;

-   **Status** -- shows the status of this order

-   **Cash Report No** - the user can leave this field blank if the
    Required Report option at the checkout in the GL setting is turned
    off. Otherwise, the system will require to have an open cash report
    for this cash desk before creating new cash orders. The system will
    automatically fill in the open Cash Report No.

Tab **Cash Receipt Subform**

The fields are identical for both types of order and are as follows:

-   **Document Type** -- one of the standard types of documents is
    filled in: Blank, Payment or Refunded;

-   **Account Type/Account No** -- the user selects one of the available
    standard account types:

    -   GL account -- the user can enter one or multiple lines
        containing G/L accounts.

    -   Customer -- the user can enter only one line for a cash order
        containing an account type Customer. In the Account No. field,
        the user must select a customer number from which they will
        receive cash;

    -   Vendor -- the user can enter only one cash order line containing
        a Vendor account type. In the Account No. field, the user must
        select a vendor number to which they will pay in cash;

    -   Bank account -- the user must enter an account type Bank account
        to transfer of funds from a cash desk account to a cash desk
        account / From a cash desk account to a bank account / From a
        bank account to a cash desk account

-   **Applies-to Doc.Type/Applies-to Doc. No** -- the user can use these
    two fields to perform the standard record linking functionality if
    the account type is set to Customer/Vendor. The user can also link
    multiple records for a customer/vendor by selecting Functions --
    Apply Entries and using the standard functionality to link multiple
    records.

-   **Amount/Amount (LCY)** -- The amount is filled in automatically
    when you apply an entry (entries) or is entered manually.

-   **Dimensions** -- The user can display on the lines, through
    Personalization, all the dimensions included in the General Ledger
    Setup.

After filling in the header and lines, the user should post this order.

This is done by selecting the **Post**/**Post and Print** button. The
system requests confirmation for posting this cash order by making the
necessary checks for set checkout limits, minimum and maximum balances.

-   **Print before Posting** -- If the Print option is selected before
    the order is posted, the system will change its status to Issued and
    then print it. Orders in Issued status are not subject to change
    and/or deletion. If you still want to make changes to the Order, you
    need to change the status of the order. This is done through the
    Reopen button.

![A screenshot of a computer Description automatically
generated](.\/media/image7.png)

-   **Open and Issued orders --** The system supports two independent
    lists of unposted Orders:

> o Open
>
> o Issued

![A screenshot of a computer Description automatically
generated](.\/media/image8.png)

-   **Posted Orders** -- Posted orders could be seen through the Search
    button and Posted Cash Receipts (or Posted Cash Withdrawal) or from
    the Cash Desk Card*:*

![A screenshot of a computer Description automatically
generated](.\/media/image9.png)
