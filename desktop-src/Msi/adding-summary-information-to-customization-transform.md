---
description: 若要在產品安裝期間套用自訂轉換，您必須將摘要資訊資料流程新增至產生自訂轉換時產生的轉換檔 MNPtrans。
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: 將摘要資訊加入自訂轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974241"
---
# <a name="adding-summary-information-to-customization-transform"></a><span data-ttu-id="d24ed-103">將摘要資訊加入自訂轉換</span><span class="sxs-lookup"><span data-stu-id="d24ed-103">Adding Summary Information to Customization Transform</span></span>

<span data-ttu-id="d24ed-104">若要在產品安裝期間套用自訂轉換，您必須將 [摘要資訊資料流程](summary-information-stream.md) 新增至產生 [自訂轉換](generating-a-customization-transform.md)時產生的轉換檔 MNPtrans。</span><span class="sxs-lookup"><span data-stu-id="d24ed-104">To apply the customization transform during an installation of the product, you must add a [Summary Information Stream](summary-information-stream.md) to the transform file MNPtrans.mst generated in [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

<span data-ttu-id="d24ed-105">您可以使用 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) 或 [**CreateTransformSummaryInfo 方法**](database-createtransformsummaryinfo.md)來產生轉換的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="d24ed-105">You may generate summary information for a transform using [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) or the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md).</span></span> <span data-ttu-id="d24ed-106">下列程式碼片段（Sum.vbs）說明 [**CreateTransformSummaryInfo 方法**](database-createtransformsummaryinfo.md) ，並可用於 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="d24ed-106">The following snippet, Sum.vbs, illustrates the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md) and is for use with Windows Script Host.</span></span> <span data-ttu-id="d24ed-107">請注意，此範例不會執行任何驗證，也不會隱藏任何錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="d24ed-107">Note that this example performs no validation and suppresses no error conditions.</span></span>


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



<span data-ttu-id="d24ed-108">若要建立摘要資訊，並將其新增至您在 [產生自訂轉換](generating-a-customization-transform.md)時建立的轉換檔案 MNPtrans，請將目錄變更為包含 Gen.vbs、原始資料庫、更新的資料庫和轉換的資料夾，然後輸入下列命令列。</span><span class="sxs-lookup"><span data-stu-id="d24ed-108">To create and add summary information to the transform file MNPtrans.mst you created in [Generating a Customization Transform](generating-a-customization-transform.md), change directories to the folder containing Gen.vbs, the original database, the updated database, and the transform, and enter the following command line.</span></span>

<span data-ttu-id="d24ed-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans**</span><span class="sxs-lookup"><span data-stu-id="d24ed-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**</span></span>

<span data-ttu-id="d24ed-110">按一下 MNP2000.msi 圖示以啟動安裝，或使用下列命令列。</span><span class="sxs-lookup"><span data-stu-id="d24ed-110">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="d24ed-111">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="d24ed-111">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="d24ed-112">這會在沒有自訂專案的情況下安裝產品。</span><span class="sxs-lookup"><span data-stu-id="d24ed-112">This installs the product without the customizations.</span></span> <span data-ttu-id="d24ed-113">若要使用自訂安裝，請輸入下列命令列。</span><span class="sxs-lookup"><span data-stu-id="d24ed-113">To install with the customization, enter the following command line.</span></span> <span data-ttu-id="d24ed-114">請注意，[ [**轉換**](transforms.md) ] 屬性的值是指位於來源的轉換檔案。</span><span class="sxs-lookup"><span data-stu-id="d24ed-114">Note that the value of the [**TRANSFORMS**](transforms.md) Property refers to transform file located at the source.</span></span>

<span data-ttu-id="d24ed-115">**msiexec/i MNP2000.msi 轉換 = MNPtrans .mst**</span><span class="sxs-lookup"><span data-stu-id="d24ed-115">**msiexec /i MNP2000.msi TRANSFORMS=MNPtrans.mst**</span></span>

<span data-ttu-id="d24ed-116">閘道功能不會出現在功能選取樹狀目錄中，而且即使在使用者介面中選取了完整的安裝類型，也不會安裝閘道功能的元件。</span><span class="sxs-lookup"><span data-stu-id="d24ed-116">The Gate feature does not appear in the feature selection tree and the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

[<span data-ttu-id="d24ed-117">繼續</span><span class="sxs-lookup"><span data-stu-id="d24ed-117">Continue</span></span>](embedding-customization-transforms-as-substorage.md)

 

 



