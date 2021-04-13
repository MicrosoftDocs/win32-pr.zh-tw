---
title: 'IResultsViewer 介面 (WdsSharedIDL .h) '
description: 公開結果檢視的方法和屬性。
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- IResultsViewer 介面舊版 Windows 環境功能
- IResultsViewer 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508807"
---
# <a name="iresultsviewer-interface"></a><span data-ttu-id="0d072-105">IResultsViewer 介面</span><span class="sxs-lookup"><span data-stu-id="0d072-105">IResultsViewer interface</span></span>

> [!NOTE]
> <span data-ttu-id="0d072-106">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="0d072-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0d072-107">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d072-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0d072-108">公開結果檢視的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="0d072-108">Exposes methods and properties for the results view.</span></span>

## <a name="members"></a><span data-ttu-id="0d072-109">成員</span><span class="sxs-lookup"><span data-stu-id="0d072-109">Members</span></span>

<span data-ttu-id="0d072-110">**IResultsViewer** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="0d072-110">The **IResultsViewer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0d072-111">**IResultsViewer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0d072-111">**IResultsViewer** also has these types of members:</span></span>

-   [<span data-ttu-id="0d072-112">方法</span><span class="sxs-lookup"><span data-stu-id="0d072-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0d072-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0d072-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0d072-114">方法</span><span class="sxs-lookup"><span data-stu-id="0d072-114">Methods</span></span>

<span data-ttu-id="0d072-115">**IResultsViewer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0d072-115">The **IResultsViewer** interface has these methods.</span></span>



| <span data-ttu-id="0d072-116">方法</span><span class="sxs-lookup"><span data-stu-id="0d072-116">Method</span></span>                                                   | <span data-ttu-id="0d072-117">描述</span><span class="sxs-lookup"><span data-stu-id="0d072-117">Description</span></span>                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d072-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="0d072-118">**GoBack**</span></span>](-search-2x-iresultsviewer-goback.md)       | <span data-ttu-id="0d072-119">未實作。</span><span class="sxs-lookup"><span data-stu-id="0d072-119">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="0d072-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="0d072-120">**GoForward**</span></span>](-search-2x-iresultsviewer-goforward.md) | <span data-ttu-id="0d072-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="0d072-121">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="0d072-122">**重新整理**</span><span class="sxs-lookup"><span data-stu-id="0d072-122">**Refresh**</span></span>](-search-2x-iresultsviewer-refresh.md)     | <span data-ttu-id="0d072-123">未實作。</span><span class="sxs-lookup"><span data-stu-id="0d072-123">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="0d072-124">**停止**</span><span class="sxs-lookup"><span data-stu-id="0d072-124">**Stop**</span></span>](-search-2x-iresultsviewer-stop.md)           | <span data-ttu-id="0d072-125">未實作。</span><span class="sxs-lookup"><span data-stu-id="0d072-125">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="0d072-126">**更新**</span><span class="sxs-lookup"><span data-stu-id="0d072-126">**Update**</span></span>](-search-2x-iresultsviewer-update.md)       | <span data-ttu-id="0d072-127">套用任何查詢變更，並將視圖導覽至新的結果集。</span><span class="sxs-lookup"><span data-stu-id="0d072-127">Applies any query changes and navigates the view to the new set of results.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0d072-128">屬性</span><span class="sxs-lookup"><span data-stu-id="0d072-128">Properties</span></span>

<span data-ttu-id="0d072-129">**IResultsViewer** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0d072-129">The **IResultsViewer** interface has these properties.</span></span>



| <span data-ttu-id="0d072-130">屬性</span><span class="sxs-lookup"><span data-stu-id="0d072-130">Property</span></span>                                                                            | <span data-ttu-id="0d072-131">存取類型</span><span class="sxs-lookup"><span data-stu-id="0d072-131">Access type</span></span>           | <span data-ttu-id="0d072-132">Description</span><span class="sxs-lookup"><span data-stu-id="0d072-132">Description</span></span>                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d072-133">**目錄**</span><span class="sxs-lookup"><span data-stu-id="0d072-133">**Contents**</span></span>](-search-2x-iresultsviewer-contents.md)<br/>                   | <span data-ttu-id="0d072-134">唯寫</span><span class="sxs-lookup"><span data-stu-id="0d072-134">Write-only</span></span><br/> | <span data-ttu-id="0d072-135">這個屬性會追蹤顯示在結果檢視中的內容類型。</span><span class="sxs-lookup"><span data-stu-id="0d072-135">This property tracks the type of the content being displayed in the results view.</span></span> <br/>    |
| [<span data-ttu-id="0d072-136">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="0d072-136">**DisplayName**</span></span>](-search-2x-iresultsviewer-displayname.md)<br/>             | <span data-ttu-id="0d072-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="0d072-137">Read-only</span></span><br/>  | <span data-ttu-id="0d072-138">類型的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0d072-138">Localized display name of the type.</span></span><br/>                                                   |
| [<span data-ttu-id="0d072-139">**EnumSelectedItems**</span><span class="sxs-lookup"><span data-stu-id="0d072-139">**EnumSelectedItems**</span></span>](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | <span data-ttu-id="0d072-140">唯寫</span><span class="sxs-lookup"><span data-stu-id="0d072-140">Write-only</span></span><br/> | <span data-ttu-id="0d072-141">未實作。</span><span class="sxs-lookup"><span data-stu-id="0d072-141">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="0d072-142">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="0d072-142">**FilterType**</span></span>](-search-2x-iresultsviewer-filtertype.md)<br/>               | <span data-ttu-id="0d072-143">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0d072-143">Read/write</span></span><br/> | <span data-ttu-id="0d072-144">這個屬性會設定或傳回用來篩選結果的 preceived 類型名稱。</span><span class="sxs-lookup"><span data-stu-id="0d072-144">This property will set or return the name of the preceived type to filter results by.</span></span><br/> |
| [<span data-ttu-id="0d072-145">**HeaderStyle**</span><span class="sxs-lookup"><span data-stu-id="0d072-145">**HeaderStyle**</span></span>](-search-2x-iresultsviewer-headerstyle.md)<br/>             | <span data-ttu-id="0d072-146">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0d072-146">Read/write</span></span><br/> | <span data-ttu-id="0d072-147">顯示在視圖中的標頭樣式。</span><span class="sxs-lookup"><span data-stu-id="0d072-147">The style of header displayed in the view.</span></span><br/>                                            |
| [<span data-ttu-id="0d072-148">**IsUpdateNeeded**</span><span class="sxs-lookup"><span data-stu-id="0d072-148">**IsUpdateNeeded**</span></span>](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | <span data-ttu-id="0d072-149">唯寫</span><span class="sxs-lookup"><span data-stu-id="0d072-149">Write-only</span></span><br/> | <span data-ttu-id="0d072-150">如果 views 查詢已修改且需要更新，則會傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="0d072-150">This returns TRUE if the views query has been modified and needs updating.</span></span> <br/>           |
| [<span data-ttu-id="0d072-151">**ItemStore**</span><span class="sxs-lookup"><span data-stu-id="0d072-151">**ItemStore**</span></span>](-search-2x-iresultsviewer-itemstore.md)<br/>                 | <span data-ttu-id="0d072-152">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0d072-152">Read/write</span></span><br/> | <span data-ttu-id="0d072-153">這個屬性會設定或傳回用來篩選結果的存放區名稱。</span><span class="sxs-lookup"><span data-stu-id="0d072-153">This property will set or return the name of the store to filter results by.</span></span><br/>          |
| [<span data-ttu-id="0d072-154">**PreviewStyle**</span><span class="sxs-lookup"><span data-stu-id="0d072-154">**PreviewStyle**</span></span>](-search-2x-iresultsviewer-previewstyle.md)<br/>           | <span data-ttu-id="0d072-155">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0d072-155">Read/write</span></span><br/> | <span data-ttu-id="0d072-156">控制預覽窗格的顯示模式。</span><span class="sxs-lookup"><span data-stu-id="0d072-156">Controls the preview pane's display mode.</span></span><br/>                                             |
| [<span data-ttu-id="0d072-157">**PropertyFilters**</span><span class="sxs-lookup"><span data-stu-id="0d072-157">**PropertyFilters**</span></span>](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | <span data-ttu-id="0d072-158">唯寫</span><span class="sxs-lookup"><span data-stu-id="0d072-158">Write-only</span></span><br/> | <span data-ttu-id="0d072-159">呼叫屬性篩選集合時，會傳回下列內容：</span><span class="sxs-lookup"><span data-stu-id="0d072-159">When calling the property filter collection it will return the following:</span></span><br/>             |
| [<span data-ttu-id="0d072-160">**QueryText**</span><span class="sxs-lookup"><span data-stu-id="0d072-160">**QueryText**</span></span>](-search-2x-iresultsviewer-querytext.md)<br/>                 | <span data-ttu-id="0d072-161">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0d072-161">Read/write</span></span><br/> | <span data-ttu-id="0d072-162">取得或設定目前的查詢文字。</span><span class="sxs-lookup"><span data-stu-id="0d072-162">Gets or sets the current query text.</span></span><br/>                                                  |
| [<span data-ttu-id="0d072-163">**ResultsStyle**</span><span class="sxs-lookup"><span data-stu-id="0d072-163">**ResultsStyle**</span></span>](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | <span data-ttu-id="0d072-164">唯寫</span><span class="sxs-lookup"><span data-stu-id="0d072-164">Write-only</span></span><br/> | <span data-ttu-id="0d072-165">未實作。</span><span class="sxs-lookup"><span data-stu-id="0d072-165">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="0d072-166">**SortOrderProperty**</span><span class="sxs-lookup"><span data-stu-id="0d072-166">**SortOrderProperty**</span></span>](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | <span data-ttu-id="0d072-167">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0d072-167">Read/write</span></span><br/> | <span data-ttu-id="0d072-168">這個屬性會設定或傳回排序結果所依據的資料行順序。</span><span class="sxs-lookup"><span data-stu-id="0d072-168">This property will set or return the order of columns to sort results by.</span></span> <br/>            |
| [<span data-ttu-id="0d072-169">**SortProperty**</span><span class="sxs-lookup"><span data-stu-id="0d072-169">**SortProperty**</span></span>](-search-2x-iresultsviewer-sortproperty.md)<br/>           | <span data-ttu-id="0d072-170">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0d072-170">Read/write</span></span><br/> | <span data-ttu-id="0d072-171">這個屬性會設定或傳回用來排序結果的屬性（property）（IndexColumn）。</span><span class="sxs-lookup"><span data-stu-id="0d072-171">This property will set or return the IndexColumn of the property to sort results by.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d072-172">備註</span><span class="sxs-lookup"><span data-stu-id="0d072-172">Remarks</span></span>

<span data-ttu-id="0d072-173">這些方法和屬性會用來操作所查看的資訊。</span><span class="sxs-lookup"><span data-stu-id="0d072-173">These methods and properties are used to manipulate the information viewed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d072-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d072-174">Requirements</span></span>



| <span data-ttu-id="0d072-175">需求</span><span class="sxs-lookup"><span data-stu-id="0d072-175">Requirement</span></span> | <span data-ttu-id="0d072-176">值</span><span class="sxs-lookup"><span data-stu-id="0d072-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d072-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d072-177">Minimum supported client</span></span><br/> | <span data-ttu-id="0d072-178">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d072-178">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0d072-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d072-179">Minimum supported server</span></span><br/> | <span data-ttu-id="0d072-180">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d072-180">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0d072-181">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0d072-181">Redistributable</span></span><br/>          | <span data-ttu-id="0d072-182">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="0d072-182">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="0d072-183">標頭</span><span class="sxs-lookup"><span data-stu-id="0d072-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d072-184"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d072-184"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

