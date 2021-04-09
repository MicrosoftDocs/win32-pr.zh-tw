---
description: 在 Windows Vista 中，Windows 映像取得 (WIA) 專案樹狀結構已大幅變更。
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: 關於 IWiaItem2 專案樹狀結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849360"
---
# <a name="about-the-iwiaitem2-item-tree"></a><span data-ttu-id="9950e-103">關於 IWiaItem2 專案樹狀結構</span><span class="sxs-lookup"><span data-stu-id="9950e-103">About the IWiaItem2 Item Tree</span></span>

<span data-ttu-id="9950e-104">在 Windows Vista 中，Windows 映像取得 (WIA) 專案樹狀結構已大幅變更。</span><span class="sxs-lookup"><span data-stu-id="9950e-104">With Windows Vista, the Windows Image Acquisition (WIA) item tree has changed significantly.</span></span> <span data-ttu-id="9950e-105">[**IWiaItem2**](-wia-iwiaitem2.md) 專案用來代表裝置屬性和裝置資料。</span><span class="sxs-lookup"><span data-stu-id="9950e-105">[**IWiaItem2**](-wia-iwiaitem2.md) items are used to represent device attributes and device data.</span></span> <span data-ttu-id="9950e-106">映射應用程式會看到 Windows 映像取得 (WIA) 2.0 裝置作為專案的階層式樹狀結構，其中包含代表裝置本身的根專案，以及代表可程式化資料來源、影像或包含影像之資料夾等專案的子專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-106">Imaging applications see a Windows Image Acquisition (WIA) 2.0 device as a hierarchical tree of items, with the root item representing the device itself and the child items representing things like programmable data sources, images, or folders that contain images.</span></span>

-   [<span data-ttu-id="9950e-107">應用程式專案</span><span class="sxs-lookup"><span data-stu-id="9950e-107">Application Items</span></span>](#application-items)
-   [<span data-ttu-id="9950e-108">專案旗標</span><span class="sxs-lookup"><span data-stu-id="9950e-108">Item Flags</span></span>](#item-flags)
-   [<span data-ttu-id="9950e-109">專案類別</span><span class="sxs-lookup"><span data-stu-id="9950e-109">Item Categories</span></span>](#item-categories)
-   [<span data-ttu-id="9950e-110">根專案</span><span class="sxs-lookup"><span data-stu-id="9950e-110">Root Item</span></span>](#root-item)
-   [<span data-ttu-id="9950e-111">資料項目</span><span class="sxs-lookup"><span data-stu-id="9950e-111">Data Item</span></span>](#data-item)
-   [<span data-ttu-id="9950e-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="9950e-112">Related topics</span></span>](#related-topics)

## <a name="application-items"></a><span data-ttu-id="9950e-113">應用程式專案</span><span class="sxs-lookup"><span data-stu-id="9950e-113">Application Items</span></span>

<span data-ttu-id="9950e-114">應用程式可以看到的 WIA 2.0 專案樹狀結構與 WIA 2.0 迷你驅動程式所建立和維護的樹狀結構不同。</span><span class="sxs-lookup"><span data-stu-id="9950e-114">The WIA 2.0 item tree that an application can see is separate from the tree created and maintained by a WIA 2.0 minidriver.</span></span> <span data-ttu-id="9950e-115">當迷你驅動程式建立樹狀結構時，WIA 2.0 服務會使用此 WIA 2.0 專案樹狀結構作為指南，以建立可供影像應用程式查看的樹狀結構複本。</span><span class="sxs-lookup"><span data-stu-id="9950e-115">When a minidriver creates a tree, the WIA 2.0 service uses this WIA 2.0 item tree as a guide to create a copy of the tree that can be viewed by imaging applications.</span></span> <span data-ttu-id="9950e-116">複製之樹狀結構中的專案稱為 *應用程式* 專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-116">Items in the copied tree are called *application* items.</span></span> <span data-ttu-id="9950e-117">迷你驅動程式所建立之樹狀結構中的專案稱為 *驅動程式* 專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-117">Items in the tree created by a minidriver are called *driver* items.</span></span>

<span data-ttu-id="9950e-118">WIA 專案可以代表掃描器的檔送紙器的可程式化資料來源，或是儲存在該裝置上的資料。</span><span class="sxs-lookup"><span data-stu-id="9950e-118">A WIA item can represent a programmable data source for a scanner's document feeder or the data stored on that device.</span></span> <span data-ttu-id="9950e-119">WIA 裝置應該分成個別的專案，以描述該裝置所產生的不同資料。</span><span class="sxs-lookup"><span data-stu-id="9950e-119">A WIA device should be divided into individual items that describe different data produced by that device.</span></span>

<span data-ttu-id="9950e-120">例如，支援平板掃描和檔送紙器掃描的 WIA 掃描器可能會分成兩個子專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-120">For example, a WIA scanner that supports both flatbed scanning and document feeder scanning might be divided into two child items.</span></span> <span data-ttu-id="9950e-121">其中一個代表平板掃描功能，另一個則代表檔送送掃描功能。</span><span class="sxs-lookup"><span data-stu-id="9950e-121">One represents the flatbed scanning functionality and the other represents the document feeder scanning functionality.</span></span>

<span data-ttu-id="9950e-122">在平台掃描器上配置並同時掃描的多個映射可以放在一個資料夾中。</span><span class="sxs-lookup"><span data-stu-id="9950e-122">Multiple images laid out on a flatbed scanner and scanned at the same time can be placed in one folder.</span></span> <span data-ttu-id="9950e-123">使用分割篩選 ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) 之後，每個影像或子領域都可以建立為資料夾的子專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-123">Using the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), each image or subregion can then be created as a child item of the folder.</span></span>

<span data-ttu-id="9950e-124">將相片儲存 ( 「電影」 ) 的相機裝置的 WIA 樹狀目錄可以分成代表資料夾、子資料夾和相片的專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-124">The WIA tree for a camera device that stores photos ("Film") can be divided into items that represent folders, subfolders, and photos.</span></span>

## <a name="item-flags"></a><span data-ttu-id="9950e-125">專案旗標</span><span class="sxs-lookup"><span data-stu-id="9950e-125">Item Flags</span></span>

<span data-ttu-id="9950e-126">WIA 專案旗標有助於分類特定 WIA 專案的內容或支援的行為。</span><span class="sxs-lookup"><span data-stu-id="9950e-126">WIA item flags help classify the content or supported behavior of a particular WIA item.</span></span> <span data-ttu-id="9950e-127">WIA 專案旗標分為兩個群組。</span><span class="sxs-lookup"><span data-stu-id="9950e-127">WIA item flags fall into two groups.</span></span>

1.  <span data-ttu-id="9950e-128">專案狀態旗標會報告 WIA 專案的目前狀態，例如 [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md)、 **WiaItemTypeDeleted** 等等。</span><span class="sxs-lookup"><span data-stu-id="9950e-128">Item status flags report the current state of the WIA item, for example, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, and so forth.</span></span>
2.  <span data-ttu-id="9950e-129">專案資料標記法/使用方式旗標會報告 WIA 專案代表的資料，或在傳送時可能產生的資料。</span><span class="sxs-lookup"><span data-stu-id="9950e-129">Item data representation/usage flags report the data that the WIA item represents or can produce if transferred.</span></span> <span data-ttu-id="9950e-130">例如， [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) 是一個資料表示旗標，會向應用程式指出與目前 WIA 專案相關聯的資料是影像資料，而且應該具有影像資料屬性。</span><span class="sxs-lookup"><span data-stu-id="9950e-130">For example, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) is a data representation flag that tells the application the data associated with the current WIA item is image data and should have image data properties.</span></span> <span data-ttu-id="9950e-131">**WIA \_IPA \_ 專案 \_ 旗標** 是一種專案使用方式旗標，會告知應用程式可設定 wia 專案，並遵循一組預先定義的設定規則（以 [**WIA \_ IPA \_ 專案 \_ 類別**](-wia-wiaitempropcommonitem.md) 為依據），而且設定可能會變更每個資料傳輸的結果。</span><span class="sxs-lookup"><span data-stu-id="9950e-131">**WIA\_IPA\_ITEM\_FLAGS** is an item usage flag that tells the application that the WIA item is configurable and follows a set of predefined configuration rules based on the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) and that the configuration can possibly change the result for each data transfer.</span></span> <span data-ttu-id="9950e-132"> (如需類別目錄定義的詳細資訊，請參閱 [專案類別](#item-categories) 目錄專案類別目錄。 ) </span><span class="sxs-lookup"><span data-stu-id="9950e-132">(For more information about category definitions, see [Item Categories](#item-categories) item categories.)</span></span>

<span data-ttu-id="9950e-133">下圖顯示 WIA 專案樹狀結構的範例，以及可能與每個專案相關聯的各種旗標。</span><span class="sxs-lookup"><span data-stu-id="9950e-133">The following graphic shows an example of a WIA item tree and the various flags that might be associated with each item.</span></span>

![樹狀目錄中專案的專案旗標範例](images/scannertree1.jpg)

## <a name="item-categories"></a><span data-ttu-id="9950e-135">專案類別</span><span class="sxs-lookup"><span data-stu-id="9950e-135">Item Categories</span></span>

<span data-ttu-id="9950e-136">使用 [**wia \_ IPA \_ 專案 \_ 類別目錄**](-wia-wiaitempropcommonitem.md) 屬性值，將 WIA 專案分組成類別目錄。</span><span class="sxs-lookup"><span data-stu-id="9950e-136">WIA items are grouped into categories using the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) property values.</span></span> <span data-ttu-id="9950e-137">這些類別定義要如何處理或使用 WIA 專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-137">These categories define how a WIA item is to be treated or used.</span></span> <span data-ttu-id="9950e-138">例如，如果專案代表已完成的檔案 (WIA \_ 類別目錄 \_ 已完成檔案 \_) ，則 wia 應用程式應該假設資料是靜態的，而且位於裝置上。</span><span class="sxs-lookup"><span data-stu-id="9950e-138">For example, if the item represents a finished file (WIA\_CATEGORY\_FINISHED\_FILE), a WIA application should assume that the data is static and located on the device.</span></span> <span data-ttu-id="9950e-139">如果專案代表送紙器 (WIA \_ 類別 \_ 送紙器) ，應用程式應該會預期它包含所需的檔送紙器內容，並如同檔送紙器般運作。</span><span class="sxs-lookup"><span data-stu-id="9950e-139">If the item represents a feeder (WIA\_CATEGORY\_FEEDER), the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span>

<span data-ttu-id="9950e-140">WIA 定義的類別如下：</span><span class="sxs-lookup"><span data-stu-id="9950e-140">The categories defined by WIA are:</span></span>

-   <span data-ttu-id="9950e-141">WIA \_ 類別 \_ AUTO</span><span class="sxs-lookup"><span data-stu-id="9950e-141">WIA\_CATEGORY\_AUTO</span></span>
-   <span data-ttu-id="9950e-142">WIA \_ 類別 \_ 送紙器</span><span class="sxs-lookup"><span data-stu-id="9950e-142">WIA\_CATEGORY\_FEEDER</span></span>
-   <span data-ttu-id="9950e-143">WIA \_ 類別 \_ 膠捲</span><span class="sxs-lookup"><span data-stu-id="9950e-143">WIA\_CATEGORY\_FILM</span></span>
-   <span data-ttu-id="9950e-144">WIA \_ 類別 \_ 已完成檔案 \_</span><span class="sxs-lookup"><span data-stu-id="9950e-144">WIA\_CATEGORY\_FINISHED\_FILE</span></span>
-   <span data-ttu-id="9950e-145">WIA \_ 類別的 \_ 平板</span><span class="sxs-lookup"><span data-stu-id="9950e-145">WIA\_CATEGORY\_FLATBED</span></span>

<span data-ttu-id="9950e-146">例如，掃描器的平板專案可能會將 [**wia \_ IPA \_ 專案 \_ 旗標**](-wia-wiaitempropcommonitem.md) 設為 [**WiaItemTypeImage**](-wia-wia-item-type-flags.md)、 **WiaItemTypeTransfer** 和 **WiaItemTypeProgrammableDataSource**，並將 [ **wia \_ IPA \_ 專案 \_ 類別目錄** ] 屬性設定為 [wia 類別] \_ \_ 平板。</span><span class="sxs-lookup"><span data-stu-id="9950e-146">For example, a scanner's flatbed item may have the [**WIA\_IPA\_ITEM\_FLAGS**](-wia-wiaitempropcommonitem.md) set to [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer**, and **WiaItemTypeProgrammableDataSource**, and the **WIA\_IPA\_ITEM\_CATEGORY** property set to WIA\_CATEGORY\_FLATBED.</span></span>

<span data-ttu-id="9950e-147">下表顯示具有專案旗標和 WIA 專案的 WIA 類別目錄群組。</span><span class="sxs-lookup"><span data-stu-id="9950e-147">The following table shows WIA category grouping with item flags and WIA items.</span></span> <span data-ttu-id="9950e-148">此資料表不包含由 WIA 定義之 WIA 專案旗標的完整清單。</span><span class="sxs-lookup"><span data-stu-id="9950e-148">This table does not include a full list of the WIA item flags defined by WIA.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9950e-149">WIA 分類</span><span class="sxs-lookup"><span data-stu-id="9950e-149">WIA Category</span></span></th>
<th><span data-ttu-id="9950e-150">有效的 WIA 專案旗標</span><span class="sxs-lookup"><span data-stu-id="9950e-150">Valid WIA Item Flags</span></span></th>
<th><span data-ttu-id="9950e-151">WIA 屬性集</span><span class="sxs-lookup"><span data-stu-id="9950e-151">WIA Property Set</span></span></th>
<th><span data-ttu-id="9950e-152">WIA 專案</span><span class="sxs-lookup"><span data-stu-id="9950e-152">WIA Items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9950e-153">WIA_CATEGORY_AUTO</span><span class="sxs-lookup"><span data-stu-id="9950e-153">WIA_CATEGORY_AUTO</span></span></td>
<td><ul>
<li><span data-ttu-id="9950e-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="9950e-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9950e-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="9950e-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="9950e-158">屬性集包含自動設定的掃描器屬性。</span><span class="sxs-lookup"><span data-stu-id="9950e-158">Property set includes auto-configured scanner properties.</span></span></td>
<td><span data-ttu-id="9950e-159">代表掃描器自動設定掃描設定的 WIA auto 專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-159">WIA auto item that represents the scanner's auto-configured scanning settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9950e-160">WIA_CATEGORY_FEEDER</span><span class="sxs-lookup"><span data-stu-id="9950e-160">WIA_CATEGORY_FEEDER</span></span></td>
<td><ul>
<li><span data-ttu-id="9950e-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="9950e-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9950e-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="9950e-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="9950e-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="9950e-166">屬性集包括送紙器掃描器控制項屬性， (通常是影像和檔專屬屬性集) 。</span><span class="sxs-lookup"><span data-stu-id="9950e-166">Property set includes feeder scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="9950e-167">WIA 送紙器專案，包括代表檔前端和上一頁頁面的子專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-167">WIA Feeder items, including child items that represent the front and back pages of a document.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9950e-168">WIA_CATEGORY_FILM</span><span class="sxs-lookup"><span data-stu-id="9950e-168">WIA_CATEGORY_FILM</span></span></td>
<td><ul>
<li><span data-ttu-id="9950e-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="9950e-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9950e-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="9950e-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="9950e-173">屬性集包含膠捲掃描器控制項屬性， (通常是影像和檔特定屬性集) 。</span><span class="sxs-lookup"><span data-stu-id="9950e-173">Property set includes film scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="9950e-174">WIA 膠捲專案，包括代表個別掃描畫面格的子專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-174">WIA Film items, including child items that represent the individual scanning frames.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9950e-175">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="9950e-175">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><ul>
<li><span data-ttu-id="9950e-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
<li><span data-ttu-id="9950e-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9950e-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span></span></li>
<li><span data-ttu-id="9950e-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span></span></li>
<li><span data-ttu-id="9950e-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="9950e-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="9950e-182">此專案上設定的屬性取決於所報告的專案類型。</span><span class="sxs-lookup"><span data-stu-id="9950e-182">The property set on this item depends on the item type reported.</span></span> <span data-ttu-id="9950e-183">例如， <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> 應該包含某些影像專案屬性，例如每圖元的位等等。</span><span class="sxs-lookup"><span data-stu-id="9950e-183">For example, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> should include some image item properties, like bits per pixel and so forth.</span></span></td>
<td><span data-ttu-id="9950e-184">WIA 儲存專案（包括代表已完成檔案內容的子專案） (資料檔案，例如 JPEG、HTML、TXT 等) 。</span><span class="sxs-lookup"><span data-stu-id="9950e-184">WIA storage items, including child items that represent finished file content (data files like JPEG, HTML, TXT, and so forth).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9950e-185">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="9950e-185">WIA_CATEGORY_FLATBED</span></span></td>
<td><ul>
<li><span data-ttu-id="9950e-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="9950e-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9950e-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="9950e-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="9950e-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="9950e-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>—如果掃描器支援多重專案掃描，可能會出現此情況。</span><span class="sxs-lookup"><span data-stu-id="9950e-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>—may be present if the scanner supports multi-item scanning.</span></span></li>
<li><span data-ttu-id="9950e-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>：如果應用程式在多專案掃描會話期間產生 WIA 專案，可能會出現此情況。</span><span class="sxs-lookup"><span data-stu-id="9950e-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>—may be present if the application generates a WIA item during a multi-item scanning session.</span></span></li>
</ul></td>
<td><span data-ttu-id="9950e-192">屬性集包含平台掃描器控制項屬性， (通常是影像和檔特定屬性集) 。</span><span class="sxs-lookup"><span data-stu-id="9950e-192">The property set includes flatbed scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="9950e-193">WIA 平板專案，包括代表掃描器平板玻璃上掃描之區域的子專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-193">WIA flatbed items, including child items that represent regions being scanned on the scanner's flatbed platen.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9950e-194">下圖顯示 WIA 專案樹狀結構的範例，以及可能與每個專案相關聯的各種類別。</span><span class="sxs-lookup"><span data-stu-id="9950e-194">The following graphic shows an example of a WIA item tree and the various categories that might be associated with each item.</span></span>

![樹狀目錄中專案的專案類別範例](images/scannertree2.jpg)

## <a name="root-item"></a><span data-ttu-id="9950e-196">根專案</span><span class="sxs-lookup"><span data-stu-id="9950e-196">Root Item</span></span>

<span data-ttu-id="9950e-197">WIA 根專案是以 [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) 和 **WiaItemTypeDevice** 旗標標記的資料夾專案，代表裝置本身。</span><span class="sxs-lookup"><span data-stu-id="9950e-197">A WIA root item is a folder item marked with [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) and **WiaItemTypeDevice** flags that represents the device itself.</span></span> <span data-ttu-id="9950e-198">它包含像是製造商、裝置名稱和驅動程式屬性的裝置屬性，例如驅動程式版本和使用者介面類別別識別碼 (CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="9950e-198">It contains device attributes like manufacturer, device name, and driver attributes like driver version and user interface class identifier (CLSID).</span></span> <span data-ttu-id="9950e-199">影像應用程式會藉由呼叫 [**IWiaDevMgr2：： CreateDevice**](-wia-iwiadevmgr2-createdevice.md) 方法，取得 WIA 專案樹狀結構的根。</span><span class="sxs-lookup"><span data-stu-id="9950e-199">Imaging applications get the root to the WIA item tree by calling [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) method.</span></span> <span data-ttu-id="9950e-200">應用程式會透過列舉樹狀結構，使用根項目來取得個別子 WIA 專案的存取權 (查看 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9950e-200">The application uses the root item to gain access to the individual child WIA items by enumerating the tree (see [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span></span>

## <a name="data-item"></a><span data-ttu-id="9950e-201">Data Item</span><span class="sxs-lookup"><span data-stu-id="9950e-201">Data Item</span></span>

<span data-ttu-id="9950e-202">任何可以用來傳送資料的專案都會被視為資料項目。</span><span class="sxs-lookup"><span data-stu-id="9950e-202">Any item that can be use to transfer data is considered a data item.</span></span> <span data-ttu-id="9950e-203">這包括以 [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) 旗標標記的專案。</span><span class="sxs-lookup"><span data-stu-id="9950e-203">This includes items marked with the [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) flag.</span></span>

<span data-ttu-id="9950e-204">資料夾專案和 nonfolder 專案可以藉由使用 [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) 旗標標記來公開傳輸資料的能力。</span><span class="sxs-lookup"><span data-stu-id="9950e-204">Folder items and nonfolder items can expose the ability to transfer data by being marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag.</span></span> <span data-ttu-id="9950e-205">具有此旗標設定的任何專案都必須提供下列 WIA 專案屬性：</span><span class="sxs-lookup"><span data-stu-id="9950e-205">Any item with this flag set has to provide the following WIA item properties:</span></span>

-   [<span data-ttu-id="9950e-206">**WIA \_ IPA \_ 訪問 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="9950e-206">**WIA\_IPA\_ACCESS\_RIGHTS**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9950e-207">**WIA \_ IPA \_ 專案 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="9950e-207">**WIA\_IPA\_ITEM\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9950e-208">**WIA \_ IPA \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="9950e-208">**WIA\_IPA\_BUFFER\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9950e-209">**WIA \_ IPA \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="9950e-209">**WIA\_IPA\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9950e-210">**WIA \_ IPA \_ 慣用 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="9950e-210">**WIA\_IPA\_PREFERRED\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9950e-211">**WIA \_ IPA \_ TYMED**</span><span class="sxs-lookup"><span data-stu-id="9950e-211">**WIA\_IPA\_TYMED**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9950e-212">**WIA \_ IPA \_ \_ 副檔名**</span><span class="sxs-lookup"><span data-stu-id="9950e-212">**WIA\_IPA\_FILENAME\_EXTENSION**</span></span>](-wia-wiaitempropcommonitem.md)

<span data-ttu-id="9950e-213">以 [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) 旗標標記的可程式化資料來源專案，也必須提供資料項目目必要屬性集。</span><span class="sxs-lookup"><span data-stu-id="9950e-213">Programmable data source items marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag must also supply the data item required property set.</span></span>

<span data-ttu-id="9950e-214">根據專案的旗標設定，WIA 資料項目可能會有其他屬性。</span><span class="sxs-lookup"><span data-stu-id="9950e-214">WIA data items may have additional properties depending on the item's flag settings.</span></span> <span data-ttu-id="9950e-215">例如，使用 [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) 旗標標記的 WIA 專案應該有影像特定的資訊屬性，例如 [**WIA \_ IPA \_ DEPTH**](-wia-wiaitempropcommonitem.md) 和 **wia \_ IPA \_ \_ \_ 行數**。</span><span class="sxs-lookup"><span data-stu-id="9950e-215">For example, WIA items marked with the [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) flag should have image specific information properties, like [**WIA\_IPA\_DEPTH**](-wia-wiaitempropcommonitem.md) and **WIA\_IPA\_NUMBER\_OF\_LINES**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9950e-216">相關主題</span><span class="sxs-lookup"><span data-stu-id="9950e-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9950e-217">**參考**</span><span class="sxs-lookup"><span data-stu-id="9950e-217">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9950e-218">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="9950e-218">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="9950e-219">**IEnumWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="9950e-219">**IEnumWiaItem2**</span></span>](-wia-ienumwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="9950e-220">**IWiaDevMgr2**</span><span class="sxs-lookup"><span data-stu-id="9950e-220">**IWiaDevMgr2**</span></span>](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



