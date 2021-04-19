---
description: 使用 COM + 系統管理目錄的簡介範例
ms.assetid: e9ce25aa-4fb1-4357-9f4e-5bf649e29447
title: 使用 COM + 系統管理目錄的簡介範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db24f3985538b7189534c9fef3ef279ed240e3a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971973"
---
# <a name="introductory-example-using-the-com-administration-catalog"></a>使用 COM + 系統管理目錄的簡介範例

以程式設計方式使用 COM + 系統管理目錄時，您通常會執行下列一般步驟， (不會在這裡) 嚴格的順序：

-   使用本機電腦上的 COM + 類別目錄開啟會話。 （選擇性）連接至遠端電腦上的 COM + 類別目錄。
-   執行動作，例如啟動或停止服務，也就是與特定 COM + 應用程式無關的動作。
-   執行動作，例如安裝或匯出 COM + 應用程式，或將元件安裝到應用程式中，這是與讀取或寫入檔案相關的動作。
-   將新專案加入至集合，例如，藉由將新的專案加入至「應用程式」集合來建立新的 COM + 應用程式。
-   設定或取得集合中專案的屬性。
-   儲存或捨棄目錄的暫止變更。
-   處理可能發生的任何錯誤。

若要在使用 COMAdmin 物件時顯示這些步驟的外觀，請參閱下面的 Microsoft Visual Basic 範例。 它會簡要說明上面所述的一些典型步驟，例如尋找集合、列舉集合以抓取專案，以及設定該專案的屬性。

在下列範例中，您將執行下列動作：

1.  建立新的 COM + 應用程式 "MyHomeZoo"。
2.  將部分元件（貓和狗）安裝到應用程式中。 這兩個元件都包含在必須已經存在的單一 DLL 中： MyZoo.dll。
3.  藉由定義兩個角色來設定應用程式的角色型安全性： ZooKeeper 和 AllergicToCats。
4.  將整個應用程式的存取權指派給 ZooKeeper 角色。
5.  將 AllergicToCats 角色存取權指派給狗元件。
6.  開啟安全性屬性，讓應用程式能夠執行角色檢查。
7.  將 MyHomeZoo 應用程式匯出到檔案，使其可以安裝在其他電腦上。

若要從 Visual Basic 使用此範例，請將參考新增至 COM + 系統管理員類型程式庫。


```VB
Function SetupMyZoo() As Boolean  ' Return False if any errors occur.

    '  Initialize error handling for this function.
    SetupMyZoo = False 
    On Error GoTo My_Error_Handler

    '  Open a session with the catalog.
    '  Instantiate a COMAdminCatalog object. 
    Dim objCatalog As COMAdminCatalog
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")

    '  Create a new COM+ application.
    '  First get the "Applications" collection from the catalog.
    Dim objApplicationsColl As COMAdminCatalogCollection
    Set objApplicationsColl = objCatalog.GetCollection("Applications")

    '  Add a new item to this collection. 
    Dim objZooApp As COMAdminCatalogObject
    Set objZooApp = objApplicationsColl.Add

    '  The "Applications" collection determines the available properties.
    '  Set the "Name" property of the new application item. 
    objZooApp.Value("Name") = "MyHomeZoo"

    '  Set the "Description" property of the new application item. 
    objZooApp.Value("Description") = "My pets at home"

    '  Save changes made to the "Applications" collection. 
    objApplicationsColl.SaveChanges

    '  Install components into the application.
    '  Use the InstallComponent method on COMAdminCatalog. 
    '  In this case, the last two parameters are passed as empty strings.
    objCatalog.InstallComponent "MyHomeZoo","MyZoo.DLL","","" 

    '  Define the roles ZooKeeper and AllergicToCats 
    '  by adding them to the "Roles" collection related to MyHomeZoo. 
    '  First get the "Roles" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Roles", 
    '  and the Key property value of objZooApp.   
    '  The Key property uniquely identifies the object, serving
    '  here to distinguish the "Roles" collection related 
    '  to MyHomeZoo from that of any other application. 
    Dim objRolesColl As COMAdminCatalogCollection
    Set objRolesColl = objApplicationsColl.GetCollection("Roles", objZooApp.Key)

    '  Add new items to this "Roles" collection. 
    Dim objZooKeeperRole As COMAdminCatalogObject
    Dim objAllergicToCatsRole As COMAdminCatalogObject
    Set objZooKeeperRole = objRolesColl.Add
    Set objAllergicToCatsRole = objRolesColl.Add

    '  Set the "Name" for the new items.
    objZooKeeperRole.Value("Name") = "ZooKeeper" 
    objAllergicToCatsRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to any items in this "Roles" collection. 
    objRolesColl.SaveChanges

    '  Assign the AllergicToCats role to the Dog component to 
    '  restrict its scope of access. (The ZooKeeper role, if assigned
    '  only at the application level, can access the whole application.)
    '  First get the "Components" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Components", and
    '  the Key property value of objZooApp. 
    Dim objZooComponentsColl As COMAdminCatalogCollection
    Set objZooComponentsColl = objApplicationsColl.GetCollection("Components", objZooApp.Key) 

    '  Find the Dog component item in this "Components" collection.
    '  First Populate the collection to read in data for all its items. 
    objZooComponentsColl.Populate

    '  Enumerate through the "Components" collection 
    '  until the Dog component item is located. 
    Dim objDog As COMAdminCatalogObject 
    For Each objDog in objZooComponentsColl
        If objDog.Name = "Dog" Then 
            Exit For
        End If
    Next 
    '  Set the role checking property at the component level for Dog.
        objDog.Value("ComponentAccessChecksEnabled") = True 

    '  Save these changes.
        objZooComponentsColl.SaveChanges
    '  Get the "RolesForComponent" collection related to the 
    '  Dog component, using the Key property of objDog. 
    Dim objRolesForDogColl As COMAdminCatalogCollection 
    Set objRolesForDogColl = objZooComponentsColl.GetCollection("RolesForComponent", objDog.Key) 

    '  Add a new item to this "RolesForComponent" collection. 
    Dim objCatSneezerRole As COMAdminCatalogObject
    Set objCatSneezerRole = objRolesForDogColl.Add

    '  Set the "Name" of the new item to be "AllergicToCats". 
    objCatSneezerRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to this "RolesForComponent" collection. 
    objRolesForDogColl.SaveChanges

    '  Now set properties to enforce role-based security. 
    '  First set role-based security at the application level.
    objZooApp.Value("ApplicationAccessChecksEnabled") = True 
    objZooApp.Value("AccessChecksLevel") = COMAdminAccessChecksApplicationComponentLevel 

    '  Save these changes.
    objApplicationsColl.SaveChanges

    '  Finally, export the new configured MyHomeZoo application to an 
    '  MSI file, used to install the application on other machines.
    '  Use the ExportApplication method on COMAdminCatalogObject.
    objCatalog.ExportApplication "MyHomeZoo", "c:\Program Files\COM applications\MyHomeZoo.MSI", 4

    '  Exit the function gracefully.
    SetupMyZoo = True

My_Error_Handler:
    If Not SetupMyZoo Then
        MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) & ")" & vbNewLine & Err.Description
    End If
    objCatSneezerRole = Nothing
    objRolesForDogColl = Nothing
    objDog = Nothing
    objZooComponentsColl = Nothing
    objAllergicToCatsRole = Nothing
    objZooKeeperRole = Nothing
    objRolesColl = Nothing
    objZooApp = Nothing
    objApplicationsColl = Nothing
    objCatalog = Nothing
Exit Function
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[交易內的 COM + 管理作業](com--administration-operations-within-transactions.md)
</dt> <dt>

[處理 COM + 管理錯誤](handling-com--administration-errors.md)
</dt> <dt>

[COMAdmin 物件的總覽](overview-of-the-comadmin-objects.md)
</dt> <dt>

[在 COM + 類別目錄上取出集合](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[設定屬性並將變更儲存至 COM + 類別目錄](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



