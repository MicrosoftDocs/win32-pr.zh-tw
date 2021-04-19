---
description: 您可以將自訂轉換儲存在 Windows Installer 套件的儲存體中，以保證當安裝套件可用時，一律可使用轉換。
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: 將自訂轉換內嵌為 Substorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993188"
---
# <a name="embedding-customization-transforms-as-substorage"></a><span data-ttu-id="b01cb-103">將自訂轉換內嵌為 Substorage</span><span class="sxs-lookup"><span data-stu-id="b01cb-103">Embedding Customization Transforms as Substorage</span></span>

<span data-ttu-id="b01cb-104">您可以將自訂轉換儲存在 Windows Installer 套件的儲存體中，以保證當安裝套件可用時，一律可使用轉換。</span><span class="sxs-lookup"><span data-stu-id="b01cb-104">You may store the customization transform in a storage of the Windows Installer package to guarantee that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="b01cb-105">請參閱 [內嵌轉換](embedded-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="b01cb-105">See [Embedded Transforms](embedded-transforms.md).</span></span> <span data-ttu-id="b01cb-106">Windows Installer SDK 中提供的範例是公用程式 WiSubStg.vbs。</span><span class="sxs-lookup"><span data-stu-id="b01cb-106">An example of this is provided in the Windows Installer SDK as the utility WiSubStg.vbs.</span></span> <span data-ttu-id="b01cb-107">下列程式碼片段 Emb.vbs，也會說明如何使用 [ [儲存體] 資料表](-storages-table.md) 來新增內嵌的轉換，並可用於 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="b01cb-107">The following snippet, Emb.vbs, also illustrates the use of the [Storages table](-storages-table.md) to add an embedded transform and is for use with Windows Script Host.</span></span>


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



<span data-ttu-id="b01cb-108">若要將名為 MNPtrans1 的儲存體新增至 MNP2000.msi，並包含您在 [將摘要資訊新增至自訂轉換](adding-summary-information-to-customization-transform.md)時所建立的轉換，請將目錄變更為包含 Emb.vbs、原始資料庫和轉換檔案的資料夾，然後輸入下列命令列。</span><span class="sxs-lookup"><span data-stu-id="b01cb-108">To add a storage named MNPtrans1 to MNP2000.msi, and containing the transform you created in [Adding Summary Information to Customization Transform](adding-summary-information-to-customization-transform.md), change directories to the folder containing Emb.vbs, the original database, and the transform file, then enter the following command line.</span></span>

<span data-ttu-id="b01cb-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans .mst MNPtrans1**</span><span class="sxs-lookup"><span data-stu-id="b01cb-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**</span></span>

<span data-ttu-id="b01cb-110">這樣就完成了自訂轉換範例。</span><span class="sxs-lookup"><span data-stu-id="b01cb-110">This completes the customization transform example.</span></span> <span data-ttu-id="b01cb-111">在 MNPtrans 中內嵌轉換之後，安裝套件一律會提供轉換。</span><span class="sxs-lookup"><span data-stu-id="b01cb-111">After embedding the transform in MNPtrans.mst, the transform is always available with the installation package.</span></span> <span data-ttu-id="b01cb-112">MNPtrans 檔案不需要位於來源，以套用轉換。</span><span class="sxs-lookup"><span data-stu-id="b01cb-112">The file MNPtrans.mst does not need to be located at the source to apply the transform.</span></span>

<span data-ttu-id="b01cb-113">從包含範例安裝套件的資料夾中移除 MNPtrans。</span><span class="sxs-lookup"><span data-stu-id="b01cb-113">Remove MNPtrans.mst from the folder containing the sample installation package.</span></span> <span data-ttu-id="b01cb-114">按一下 MNP2000.msi 圖示以啟動安裝，或使用下列命令列。</span><span class="sxs-lookup"><span data-stu-id="b01cb-114">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="b01cb-115">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="b01cb-115">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="b01cb-116">請注意，這會在沒有自訂專案的情況下安裝產品。</span><span class="sxs-lookup"><span data-stu-id="b01cb-116">Note that this installs the product without the customizations.</span></span> <span data-ttu-id="b01cb-117">若要使用自訂安裝，請輸入下列命令列。</span><span class="sxs-lookup"><span data-stu-id="b01cb-117">To install with the customizations, enter the following command line.</span></span> <span data-ttu-id="b01cb-118">您可以使用冒號來指出 [ [**轉換**](transforms.md) ] 屬性的值是指內嵌的轉換。</span><span class="sxs-lookup"><span data-stu-id="b01cb-118">Use a colon to indicate that the value of the [**TRANSFORMS**](transforms.md) Property refers to an embedded transform.</span></span>

<span data-ttu-id="b01cb-119">msiexec/i MNP2000.msi 轉換 =： MNPtrans1</span><span class="sxs-lookup"><span data-stu-id="b01cb-119">msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1</span></span>

<span data-ttu-id="b01cb-120">請注意，[閘道] 功能不會出現在功能選取樹狀目錄中，而且即使在使用者介面中選取了完整的安裝類型，也不會安裝閘道功能的元件。</span><span class="sxs-lookup"><span data-stu-id="b01cb-120">Note that the Gate feature does not appear in the feature selection tree and that the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

## <a name="next-example"></a><span data-ttu-id="b01cb-121">下一個範例</span><span class="sxs-lookup"><span data-stu-id="b01cb-121">Next example</span></span>

[<span data-ttu-id="b01cb-122">小型更新修補範例</span><span class="sxs-lookup"><span data-stu-id="b01cb-122">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

 

 



