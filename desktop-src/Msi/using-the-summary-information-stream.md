---
description: 本節說明 Windows Installer API 中哪些函數可以呼叫摘要資訊資料流程屬性。 如需摘要資訊資料流程及其如何與資料庫搭配運作的詳細資訊，請參閱關於摘要資訊資料流程。
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: 使用摘要資訊資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de3ece9ad336b1a88d343b859fd3881b23246c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944294"
---
# <a name="using-the-summary-information-stream"></a><span data-ttu-id="fb0f9-104">使用摘要資訊資料流程</span><span class="sxs-lookup"><span data-stu-id="fb0f9-104">Using the Summary Information Stream</span></span>

<span data-ttu-id="fb0f9-105">本節說明 Windows Installer API 中哪些函數可以呼叫摘要資訊資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-105">This section describes which functions in the Windows Installer API can call the summary information stream properties.</span></span> <span data-ttu-id="fb0f9-106">如需摘要資訊資料流程及其如何與資料庫搭配運作的詳細資訊，請參閱 [關於摘要資訊資料流程](about-the-summary-information-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-106">For more information on the summary information stream and how it works with databases, see [About the Summary Information Stream](about-the-summary-information-stream.md).</span></span>

-   <span data-ttu-id="fb0f9-107">請務必記住，安裝套裝程式含不同類型的資料庫，而摘要資訊資料流程的某些屬性在不同的資料庫中有不同的意義。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-107">It is important to remember that the installer contains different types of databases, and some properties of the summary information stream have different meanings with different databases.</span></span> <span data-ttu-id="fb0f9-108">如需詳細資訊，請參閱 [摘要屬性描述](summary-property-descriptions.md)。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-108">For more information, see [Summary Property Descriptions](summary-property-descriptions.md).</span></span>
-   <span data-ttu-id="fb0f9-109">當資料庫開啟為另一個資料庫的輸出時，輸出資料庫的摘要資訊資料流程實際上是原始資料庫的唯讀鏡像，因此無法變更。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-109">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="fb0f9-110">此外，它也不會保存在資料庫中。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-110">Additionally, it will not be persisted with the database.</span></span> <span data-ttu-id="fb0f9-111">若要建立或修改輸出資料庫的摘要資訊，必須將其關閉並重新開啟。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-111">To create or modify the summary information for the output database it must be closed and re-opened.</span></span>

<span data-ttu-id="fb0f9-112">下列步驟說明如何使用摘要資訊資料流程函數：</span><span class="sxs-lookup"><span data-stu-id="fb0f9-112">The following steps describe how to use the summary information stream functions:</span></span>

<span data-ttu-id="fb0f9-113">**使用摘要資訊資料流程屬性**</span><span class="sxs-lookup"><span data-stu-id="fb0f9-113">**To use the summary information stream properties**</span></span>

1.  <span data-ttu-id="fb0f9-114">藉由呼叫 [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) 函式，取得包含摘要資訊資料流程之資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-114">Obtain a handle to the database containing the summary information stream by calling the [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) function.</span></span>
2.  <span data-ttu-id="fb0f9-115">呼叫 [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) 函數來取得現有屬性的數目。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-115">Call the [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) function to obtain the number of existing properties.</span></span>
3.  <span data-ttu-id="fb0f9-116">呼叫 [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) 函數來查看單一摘要資訊屬性。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-116">Call the [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) function to view a single summary information property.</span></span>
4.  <span data-ttu-id="fb0f9-117">呼叫 [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) 函數來設定單一屬性</span><span class="sxs-lookup"><span data-stu-id="fb0f9-117">Call the [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) function to set a single property</span></span>
5.  <span data-ttu-id="fb0f9-118">呼叫 [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) 函數來儲存摘要資訊屬性。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-118">Call the [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) function to save the summary information property.</span></span>
6.  <span data-ttu-id="fb0f9-119">呼叫 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) 函數，以建立現有轉換的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-119">Call the [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) function to create the summary information for an existing transform.</span></span>

<span data-ttu-id="fb0f9-120">[Orca.exe](orca-exe.md) 和 [Msiinfo.exe](msiinfo-exe.md) 是可用於編輯或顯示資料庫之摘要資訊資料流程的工具。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-120">[Orca.exe](orca-exe.md) and [Msiinfo.exe](msiinfo-exe.md) are tools that can be used to edit or display the summary information stream of a database.</span></span> <span data-ttu-id="fb0f9-121">這些工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-121">These tools are only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="fb0f9-122">您也可以使用 Windows Installer [Automation 介面](automation-interface.md)的下列方法和屬性來存取摘要資訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-122">The summary information stream can also be accessed using the following methods and properties of the Windows Installer [Automation Interface](automation-interface.md).</span></span>

-   [<span data-ttu-id="fb0f9-123">**SummaryInfo。屬性**</span><span class="sxs-lookup"><span data-stu-id="fb0f9-123">**SummaryInfo.Property**</span></span>](summaryinfo-summaryinfo.md)
-   [<span data-ttu-id="fb0f9-124">**SummaryInfo.PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="fb0f9-124">**SummaryInfo.PropertyCount**</span></span>](summaryinfo-propertycount.md)
-   [<span data-ttu-id="fb0f9-125">**SummaryInfo。保存**</span><span class="sxs-lookup"><span data-stu-id="fb0f9-125">**SummaryInfo.Persist**</span></span>](summaryinfo-persist.md)
-   [<span data-ttu-id="fb0f9-126">**SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="fb0f9-126">**Installer.SummaryInformation**</span></span>](installer-summaryinformation.md)
-   [<span data-ttu-id="fb0f9-127">**SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="fb0f9-127">**Database.SummaryInformation**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="fb0f9-128">**CreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="fb0f9-128">**Database.CreateTransformSummaryInfo**</span></span>](database-createtransformsummaryinfo.md)

<span data-ttu-id="fb0f9-129">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiSumInf.vbs。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-129">The VBScript file WiSumInf.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="fb0f9-130">此範例腳本可用來管理 Windows Installer 封裝的摘要資訊串流。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-130">This sample script can be used to manage the summary information stream of a Windows Installer package.</span></span> <span data-ttu-id="fb0f9-131">如需 WiSumInf.vbs 的詳細資訊，請參閱 [管理摘要資訊](manage-summary-information.md)。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-131">For more information about WiSumInf.vbs, see [Manage Summary Information](manage-summary-information.md).</span></span>

 

 



