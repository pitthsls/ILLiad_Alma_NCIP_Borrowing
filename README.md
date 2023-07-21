# ILLiad Alma NCIP Borrowing V3.2

Hello and Welcome!

This is the official GitHub repository containing the latest updates for the ILLiad Alma NCIP Borrowing System Addon.   The latest version of this Addon submitted to Atlas Systems can be found at the [ILLiad Addons Directory](https://atlas-sys.atlassian.net/wiki/spaces/ILLiadAddons/pages/3149522/ILLiad+ALMA+NCIP+Borrowing+Client+System+Addon).  

This is a System Addon for [ILLiad](https://www.atlas-sys.com/illiad) allowing for the creation of items with brief records in Alma from ILLiad via NCIP, using barcodes produced from data within a selectable ILLiad transaction field.

This System Addon needs to be installed in the same directory as your regular Addons in its own folder.  If you make changes to your Addon configurations through the [config.xml](https://github.com/Hypolymer/ILLiad_Alma_NCIP_Borrowing) file while your ILLiad Client is open, you will need to close and reopen your ILLiad Client for the configuration changes to take effect.  You may also make changes to your configuration values through the ILLiad Client, under System > Manage Addons.

If you run into problems and want to see the error log, please check these instructions:  https://github.com/Hypolymer/AddonsLibrary/wiki/Enabling-ILLiad-Client-and-Server-Logs

This System Addon is typically used in conjunction with the [ILLiad Alma NCIP Lending Addon](https://github.com/Hypolymer/ILLiad_Alma_NCIP_Lending)  and the [ILLiad Alma NCIP Borrowing Renewals V2 Addon](https://github.com/Hypolymer/ILLiad_Alma_NCIP_Borrowing_Renewals_V2).

Description of Addon Configuration Settings ([config.xml](https://github.com/Hypolymer/ILLiad_Alma_NCIP_Borrowing/blob/main/config.xml))

| Configuration Value        | Description |
|:------------- | :-----|
| NCIP_Responder_URL |  The URL used to connect to your Alma NCIP responder. Replace "xxx" with your institution's three letter Alma code. If SUNY, replace "xxx" with "suny-zzz", and replace zzz with your institution's three letter Alma code.|
| ILLiad_field_to_get_external_identifier | This ILLiad field will be used as the External Identifier in Alma (the transaction number will be used if this field is empty).|
| ILLiad_field_to_get_barcode |This field will be used as the item barcode in Alma (the transaction number will be used if this field is empty).|
|acceptItem_from_uniqueAgency_value| Your institution's Alma code.  This could be a three-letter code, or a hyphenated code like "SUNY_GEN"|
|ApplicationProfileType|Input the Resource Sharing Partner code used in Alma.  Possible values might be "ILL" or "ILLiad".|
|BorrowingAcceptItemFailQueue|This designates the name of the queue a Borrowing Transaction will be moved to if the BorrowingAcceptItem function fails. Queue names that do not currently exist will be created automatically.|
|BorrowingCheckInItemFailQueue|This designates the name of the queue a Borrowing Transaction will be moved to if the BorrowingCheckInItem function fails. Queue names that do not currently exist will be created automatically.|
|EnablePatronBorrowingReturns|Possible values:  True or False.  When this setting is enabled, patron returns will go through ILLiad and a message is sent to Alma.  When this setting is disabled, patron returns will update ILLiad and exteral ILL systems like Worldshare but item will need to also be returned in Alma.|
|Use_Prefixes|Determines whether or not you want to change prefixes of a transaction based on specific criteria (below). NOTE: Using these will disable the abilty to scan a barcode in Alma.|
|Prefix_for_LibraryUseOnly|This setting allows you to change the prefix of a transaction that is marked LibraryUseOnly Yes.|
|Prefix_for_RenewablesAllowed|This setting allows you to change the prefix of a transaction that is marked RenewalsAllowed Yes.|
|Prefix_for_LibraryUseOnly_and_RenewablesAllowed|This setting allows you to change the prefix of a transaction that is marked both LibraryUseOnly and RenewalsAllowed Yes.|
