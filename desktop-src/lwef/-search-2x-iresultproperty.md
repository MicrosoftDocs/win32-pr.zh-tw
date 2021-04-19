---
title: 'IResultProperty 介面 (WdsSharedIDL .h) '
description: 公開結果屬性。
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- IResultProperty 介面舊版 Windows 環境功能
- IResultProperty 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966129"
---
# <a name="iresultproperty-interface"></a><span data-ttu-id="8f133-105">IResultProperty 介面</span><span class="sxs-lookup"><span data-stu-id="8f133-105">IResultProperty interface</span></span>

> [!NOTE]
> <span data-ttu-id="8f133-106">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="8f133-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8f133-107">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="8f133-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8f133-108">公開結果屬性。</span><span class="sxs-lookup"><span data-stu-id="8f133-108">Exposes result properties.</span></span>

## <a name="members"></a><span data-ttu-id="8f133-109">成員</span><span class="sxs-lookup"><span data-stu-id="8f133-109">Members</span></span>

<span data-ttu-id="8f133-110">**IResultProperty** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="8f133-110">The **IResultProperty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8f133-111">**IResultProperty** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8f133-111">**IResultProperty** also has these types of members:</span></span>

-   [<span data-ttu-id="8f133-112">方法</span><span class="sxs-lookup"><span data-stu-id="8f133-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f133-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8f133-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f133-114">方法</span><span class="sxs-lookup"><span data-stu-id="8f133-114">Methods</span></span>

<span data-ttu-id="8f133-115">**IResultProperty** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8f133-115">The **IResultProperty** interface has these methods.</span></span>



| <span data-ttu-id="8f133-116">方法</span><span class="sxs-lookup"><span data-stu-id="8f133-116">Method</span></span>                                                    | <span data-ttu-id="8f133-117">描述</span><span class="sxs-lookup"><span data-stu-id="8f133-117">Description</span></span>                 |
|:----------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="8f133-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="8f133-118">**GoBack**</span></span>](-search-2x-iresultproperty-goback.md)       | <span data-ttu-id="8f133-119">未實作。</span><span class="sxs-lookup"><span data-stu-id="8f133-119">Not implemented.</span></span><br/> |
| [<span data-ttu-id="8f133-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="8f133-120">**GoForward**</span></span>](-search-2x-iresultproperty-goforward.md) | <span data-ttu-id="8f133-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="8f133-121">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8f133-122">屬性</span><span class="sxs-lookup"><span data-stu-id="8f133-122">Properties</span></span>

<span data-ttu-id="8f133-123">**IResultProperty** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8f133-123">The **IResultProperty** interface has these properties.</span></span>



| <span data-ttu-id="8f133-124">屬性</span><span class="sxs-lookup"><span data-stu-id="8f133-124">Property</span></span>                                                                   | <span data-ttu-id="8f133-125">存取類型</span><span class="sxs-lookup"><span data-stu-id="8f133-125">Access type</span></span>          | <span data-ttu-id="8f133-126">Description</span><span class="sxs-lookup"><span data-stu-id="8f133-126">Description</span></span>                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [<span data-ttu-id="8f133-127">**資料類型**</span><span class="sxs-lookup"><span data-stu-id="8f133-127">**DataType**</span></span>](-search-2x-iresultproperty-datatype.md)<br/>         | <span data-ttu-id="8f133-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="8f133-128">Read-only</span></span><br/> | <span data-ttu-id="8f133-129">屬性資料類型。</span><span class="sxs-lookup"><span data-stu-id="8f133-129">A properties data type.</span></span> <br/>                   |
| [<span data-ttu-id="8f133-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="8f133-130">**DisplayName**</span></span>](-search-2x-iresultproperty-displayname.md)<br/>   | <span data-ttu-id="8f133-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="8f133-131">Read-only</span></span><br/> | <span data-ttu-id="8f133-132">屬性的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8f133-132">Localized display name of the property.</span></span> <br/>   |
| [<span data-ttu-id="8f133-133">**DisplayState**</span><span class="sxs-lookup"><span data-stu-id="8f133-133">**DisplayState**</span></span>](-search-2x-iresultproperty-displaystate.md)<br/> | <span data-ttu-id="8f133-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="8f133-134">Read-only</span></span><br/> | <span data-ttu-id="8f133-135">屬性的 Visability。</span><span class="sxs-lookup"><span data-stu-id="8f133-135">Visability of the property.</span></span> <br/>               |
| [<span data-ttu-id="8f133-136">**提示**</span><span class="sxs-lookup"><span data-stu-id="8f133-136">**Hint**</span></span>](-search-2x-iresultproperty-hint.md)<br/>                 | <span data-ttu-id="8f133-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="8f133-137">Read-only</span></span><br/> | <span data-ttu-id="8f133-138">用來協助資料抓取的特殊值。</span><span class="sxs-lookup"><span data-stu-id="8f133-138">Special value used to aid data retrieval.</span></span> <br/> |
| [<span data-ttu-id="8f133-139">**IndexColumn**</span><span class="sxs-lookup"><span data-stu-id="8f133-139">**IndexColumn**</span></span>](-search-2x-iresultproperty-indexcolumn.md)<br/>   | <span data-ttu-id="8f133-140">唯讀</span><span class="sxs-lookup"><span data-stu-id="8f133-140">Read-only</span></span><br/> | <span data-ttu-id="8f133-141">索引中的屬性資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="8f133-141">Properties column name in the index.</span></span> <br/>      |
| [<span data-ttu-id="8f133-142">**UID**</span><span class="sxs-lookup"><span data-stu-id="8f133-142">**UID**</span></span>](-search-2x-iresultproperty-uid.md)<br/>                   | <span data-ttu-id="8f133-143">唯讀</span><span class="sxs-lookup"><span data-stu-id="8f133-143">Read-only</span></span><br/> | <span data-ttu-id="8f133-144">屬性的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f133-144">Unique identifier for the property.</span></span> <br/>       |



 

## <a name="remarks"></a><span data-ttu-id="8f133-145">備註</span><span class="sxs-lookup"><span data-stu-id="8f133-145">Remarks</span></span>

<span data-ttu-id="8f133-146">這些專案會傳回屬性。</span><span class="sxs-lookup"><span data-stu-id="8f133-146">These are the items return properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f133-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f133-147">Requirements</span></span>



| <span data-ttu-id="8f133-148">需求</span><span class="sxs-lookup"><span data-stu-id="8f133-148">Requirement</span></span> | <span data-ttu-id="8f133-149">值</span><span class="sxs-lookup"><span data-stu-id="8f133-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f133-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f133-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8f133-151">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f133-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8f133-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f133-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8f133-153">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f133-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8f133-154">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8f133-154">Redistributable</span></span><br/>          | <span data-ttu-id="8f133-155">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="8f133-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="8f133-156">標頭</span><span class="sxs-lookup"><span data-stu-id="8f133-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f133-157"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f133-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

