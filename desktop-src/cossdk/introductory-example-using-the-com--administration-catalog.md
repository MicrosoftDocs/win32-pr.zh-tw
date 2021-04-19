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
# <a name="introductory-example-using-the-com-administration-catalog"></a><span data-ttu-id="e9211-103">使用 COM + 系統管理目錄的簡介範例</span><span class="sxs-lookup"><span data-stu-id="e9211-103">Introductory Example Using the COM+ Administration Catalog</span></span>

<span data-ttu-id="e9211-104">以程式設計方式使用 COM + 系統管理目錄時，您通常會執行下列一般步驟， (不會在這裡) 嚴格的順序：</span><span class="sxs-lookup"><span data-stu-id="e9211-104">When programmatically using the COM+ Administration catalog, you typically carry out the following general steps (not given in a strict order here):</span></span>

-   <span data-ttu-id="e9211-105">使用本機電腦上的 COM + 類別目錄開啟會話。</span><span class="sxs-lookup"><span data-stu-id="e9211-105">Open a session with the COM+ catalog on the local machine.</span></span> <span data-ttu-id="e9211-106">（選擇性）連接至遠端電腦上的 COM + 類別目錄。</span><span class="sxs-lookup"><span data-stu-id="e9211-106">Optionally, connect to the COM+ catalog on a remote machine.</span></span>
-   <span data-ttu-id="e9211-107">執行動作，例如啟動或停止服務，也就是與特定 COM + 應用程式無關的動作。</span><span class="sxs-lookup"><span data-stu-id="e9211-107">Perform actions such as starting or stopping services—actions that don't pertain to a particular COM+ application.</span></span>
-   <span data-ttu-id="e9211-108">執行動作，例如安裝或匯出 COM + 應用程式，或將元件安裝到應用程式中，這是與讀取或寫入檔案相關的動作。</span><span class="sxs-lookup"><span data-stu-id="e9211-108">Perform actions such as installing or exporting COM+ applications, or installing components into applications—actions that pertain to reading from or writing to files.</span></span>
-   <span data-ttu-id="e9211-109">將新專案加入至集合，例如，藉由將新的專案加入至「應用程式」集合來建立新的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="e9211-109">Add new items to collections, such as creating a new COM+ application by adding a new item to the "Applications" collection.</span></span>
-   <span data-ttu-id="e9211-110">設定或取得集合中專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="e9211-110">Set or get properties on an item in a collection.</span></span>
-   <span data-ttu-id="e9211-111">儲存或捨棄目錄的暫止變更。</span><span class="sxs-lookup"><span data-stu-id="e9211-111">Save or discard pending changes to the catalog.</span></span>
-   <span data-ttu-id="e9211-112">處理可能發生的任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="e9211-112">Handle any errors that might occur.</span></span>

<span data-ttu-id="e9211-113">若要在使用 COMAdmin 物件時顯示這些步驟的外觀，請參閱下面的 Microsoft Visual Basic 範例。</span><span class="sxs-lookup"><span data-stu-id="e9211-113">To show what these steps look like when you use the COMAdmin objects, a Microsoft Visual Basic example is provided below.</span></span> <span data-ttu-id="e9211-114">它會簡要說明上面所述的一些典型步驟，例如尋找集合、列舉集合以抓取專案，以及設定該專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="e9211-114">It briefly illustrates some of the typical steps described above, such as locating collections, enumerating through a collection to retrieve an item, and setting properties on that item.</span></span>

<span data-ttu-id="e9211-115">在下列範例中，您將執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e9211-115">In the example below you will perform the following actions:</span></span>

1.  <span data-ttu-id="e9211-116">建立新的 COM + 應用程式 "MyHomeZoo"。</span><span class="sxs-lookup"><span data-stu-id="e9211-116">Create a new COM+ application, "MyHomeZoo".</span></span>
2.  <span data-ttu-id="e9211-117">將部分元件（貓和狗）安裝到應用程式中。</span><span class="sxs-lookup"><span data-stu-id="e9211-117">Install some components, Cat and Dog, into the application.</span></span> <span data-ttu-id="e9211-118">這兩個元件都包含在必須已經存在的單一 DLL 中： MyZoo.dll。</span><span class="sxs-lookup"><span data-stu-id="e9211-118">Both components are contained in a single DLL that must already exist: MyZoo.dll.</span></span>
3.  <span data-ttu-id="e9211-119">藉由定義兩個角色來設定應用程式的角色型安全性： ZooKeeper 和 AllergicToCats。</span><span class="sxs-lookup"><span data-stu-id="e9211-119">Configure role-based security for the application by defining two roles: ZooKeeper and AllergicToCats.</span></span>
4.  <span data-ttu-id="e9211-120">將整個應用程式的存取權指派給 ZooKeeper 角色。</span><span class="sxs-lookup"><span data-stu-id="e9211-120">Assign the ZooKeeper role access to the entire application.</span></span>
5.  <span data-ttu-id="e9211-121">將 AllergicToCats 角色存取權指派給狗元件。</span><span class="sxs-lookup"><span data-stu-id="e9211-121">Assign the AllergicToCats role access to only the Dog component.</span></span>
6.  <span data-ttu-id="e9211-122">開啟安全性屬性，讓應用程式能夠執行角色檢查。</span><span class="sxs-lookup"><span data-stu-id="e9211-122">Turn on security properties so that role checking will be enforced for the application.</span></span>
7.  <span data-ttu-id="e9211-123">將 MyHomeZoo 應用程式匯出到檔案，使其可以安裝在其他電腦上。</span><span class="sxs-lookup"><span data-stu-id="e9211-123">Export the MyHomeZoo application to a file so that it can be installed on other computers.</span></span>

<span data-ttu-id="e9211-124">若要從 Visual Basic 使用此範例，請將參考新增至 COM + 系統管理員類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="e9211-124">To use this example from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e9211-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9211-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9211-126">交易內的 COM + 管理作業</span><span class="sxs-lookup"><span data-stu-id="e9211-126">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="e9211-127">處理 COM + 管理錯誤</span><span class="sxs-lookup"><span data-stu-id="e9211-127">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="e9211-128">COMAdmin 物件的總覽</span><span class="sxs-lookup"><span data-stu-id="e9211-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="e9211-129">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="e9211-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="e9211-130">設定屬性並將變更儲存至 COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="e9211-130">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



