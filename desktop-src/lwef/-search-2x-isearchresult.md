---
title: 'ISearchResult 介面 (WdsSharedIDL .h) '
description: 公開有關結果集的資訊和屬性。
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- ISearchResult 介面舊版 Windows 環境功能
- ISearchResult 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89387ebe02c87ca6a5c5ac663a67ea060bd78948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686110"
---
# <a name="isearchresult-interface"></a><span data-ttu-id="034f7-105">ISearchResult 介面</span><span class="sxs-lookup"><span data-stu-id="034f7-105">ISearchResult interface</span></span>

> [!NOTE]
> <span data-ttu-id="034f7-106">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="034f7-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="034f7-107">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="034f7-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="034f7-108">公開有關結果集的資訊和屬性。</span><span class="sxs-lookup"><span data-stu-id="034f7-108">Exposes information and properties regarding the result set.</span></span>

## <a name="members"></a><span data-ttu-id="034f7-109">成員</span><span class="sxs-lookup"><span data-stu-id="034f7-109">Members</span></span>

<span data-ttu-id="034f7-110">**ISearchResult** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="034f7-110">The **ISearchResult** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="034f7-111">**ISearchResult** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="034f7-111">**ISearchResult** also has these types of members:</span></span>

-   [<span data-ttu-id="034f7-112">方法</span><span class="sxs-lookup"><span data-stu-id="034f7-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="034f7-113">方法</span><span class="sxs-lookup"><span data-stu-id="034f7-113">Methods</span></span>

<span data-ttu-id="034f7-114">**ISearchResult** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="034f7-114">The **ISearchResult** interface has these methods.</span></span>



| <span data-ttu-id="034f7-115">方法</span><span class="sxs-lookup"><span data-stu-id="034f7-115">Method</span></span>                                                            | <span data-ttu-id="034f7-116">描述</span><span class="sxs-lookup"><span data-stu-id="034f7-116">Description</span></span>                 |
|:------------------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="034f7-117">**可用性**</span><span class="sxs-lookup"><span data-stu-id="034f7-117">**Availability**</span></span>](-search-2x-isearchresult-availability.md)     | <span data-ttu-id="034f7-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-118">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-119">**DoVerb**</span><span class="sxs-lookup"><span data-stu-id="034f7-119">**DoVerb**</span></span>](-search-2x-isearchresult-doverb.md)                 | <span data-ttu-id="034f7-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-120">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-121">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="034f7-121">**GetIcon**</span></span>](-search-2x-isearchresult-geticon.md)               | <span data-ttu-id="034f7-122">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-122">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-123">**GetThumbnail**</span><span class="sxs-lookup"><span data-stu-id="034f7-123">**GetThumbnail**</span></span>](-search-2x-isearchresult-getthumbnail.md)     | <span data-ttu-id="034f7-124">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-124">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-125">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="034f7-125">**GetValue**</span></span>](-search-2x-isearchresult-getvalue.md)             | <span data-ttu-id="034f7-126">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-126">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-127">**GetVerb**</span><span class="sxs-lookup"><span data-stu-id="034f7-127">**GetVerb**</span></span>](-search-2x-isearchresult-getverb.md)               | <span data-ttu-id="034f7-128">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-128">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-129">**IconCount**</span><span class="sxs-lookup"><span data-stu-id="034f7-129">**IconCount**</span></span>](-search-2x-isearchresult-iconcount.md)           | <span data-ttu-id="034f7-130">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-130">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-131">**索引**</span><span class="sxs-lookup"><span data-stu-id="034f7-131">**Index**</span></span>](-search-2x-isearchresult-index.md)                   | <span data-ttu-id="034f7-132">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-132">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-133">**LoadState**</span><span class="sxs-lookup"><span data-stu-id="034f7-133">**LoadState**</span></span>](-search-2x-isearchresult-loadstate.md)           | <span data-ttu-id="034f7-134">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-134">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-135">**預覽程式**</span><span class="sxs-lookup"><span data-stu-id="034f7-135">**Previewer**</span></span>](-search-2x-isearchresult-previewer.md)           | <span data-ttu-id="034f7-136">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-136">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-137">**PutValue**</span><span class="sxs-lookup"><span data-stu-id="034f7-137">**PutValue**</span></span>](-search-2x-isearchresult-putvalue.md)             | <span data-ttu-id="034f7-138">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-138">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-139">**ThumbnailState**</span><span class="sxs-lookup"><span data-stu-id="034f7-139">**ThumbnailState**</span></span>](-search-2x-isearchresult-thumbnailstate.md) | <span data-ttu-id="034f7-140">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-140">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-141">**類型**</span><span class="sxs-lookup"><span data-stu-id="034f7-141">**Type**</span></span>](-search-2x-isearchresult-type.md)                     | <span data-ttu-id="034f7-142">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-142">Not implemented.</span></span><br/> |
| [<span data-ttu-id="034f7-143">**VerbCount**</span><span class="sxs-lookup"><span data-stu-id="034f7-143">**VerbCount**</span></span>](-search-2x-isearchresult-verbcount.md)           | <span data-ttu-id="034f7-144">未實作。</span><span class="sxs-lookup"><span data-stu-id="034f7-144">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="034f7-145">備註</span><span class="sxs-lookup"><span data-stu-id="034f7-145">Remarks</span></span>

<span data-ttu-id="034f7-146">這些方法會公開適用于結果集的屬性和動作。</span><span class="sxs-lookup"><span data-stu-id="034f7-146">These methods expose properties and actions applicable to the result set.</span></span>

## <a name="requirements"></a><span data-ttu-id="034f7-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="034f7-147">Requirements</span></span>



| <span data-ttu-id="034f7-148">需求</span><span class="sxs-lookup"><span data-stu-id="034f7-148">Requirement</span></span> | <span data-ttu-id="034f7-149">值</span><span class="sxs-lookup"><span data-stu-id="034f7-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="034f7-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="034f7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="034f7-151">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="034f7-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="034f7-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="034f7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="034f7-153">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="034f7-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="034f7-154">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="034f7-154">Redistributable</span></span><br/>          | <span data-ttu-id="034f7-155">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="034f7-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="034f7-156">標頭</span><span class="sxs-lookup"><span data-stu-id="034f7-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="034f7-157"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="034f7-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

