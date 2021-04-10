---
title: 'IPropertyFilterCollection 介面 (WdsSharedIDL .h) '
description: 根據提交的查詢，公開傳回之集合的屬性。
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- IPropertyFilterCollection 介面舊版 Windows 環境功能
- IPropertyFilterCollection 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317319"
---
# <a name="ipropertyfiltercollection-interface"></a><span data-ttu-id="0af8b-105">IPropertyFilterCollection 介面</span><span class="sxs-lookup"><span data-stu-id="0af8b-105">IPropertyFilterCollection interface</span></span>

> [!NOTE]
> <span data-ttu-id="0af8b-106">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="0af8b-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0af8b-107">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="0af8b-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0af8b-108">根據提交的查詢，公開傳回之集合的屬性。</span><span class="sxs-lookup"><span data-stu-id="0af8b-108">Exposes properties of the returned collection based on the query submitted.</span></span>

## <a name="members"></a><span data-ttu-id="0af8b-109">成員</span><span class="sxs-lookup"><span data-stu-id="0af8b-109">Members</span></span>

<span data-ttu-id="0af8b-110">**IPropertyFilterCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="0af8b-110">The **IPropertyFilterCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0af8b-111">**IPropertyFilterCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0af8b-111">**IPropertyFilterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="0af8b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0af8b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0af8b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0af8b-113">Properties</span></span>

<span data-ttu-id="0af8b-114">**IPropertyFilterCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0af8b-114">The **IPropertyFilterCollection** interface has these properties.</span></span>



| <span data-ttu-id="0af8b-115">屬性</span><span class="sxs-lookup"><span data-stu-id="0af8b-115">Property</span></span>                                                                         | <span data-ttu-id="0af8b-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="0af8b-116">Access type</span></span>           | <span data-ttu-id="0af8b-117">Description</span><span class="sxs-lookup"><span data-stu-id="0af8b-117">Description</span></span>                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="0af8b-118">**AddItem**</span><span class="sxs-lookup"><span data-stu-id="0af8b-118">**AddItem**</span></span>](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | <span data-ttu-id="0af8b-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="0af8b-119">Read-only</span></span><br/>  | <span data-ttu-id="0af8b-120">將新的篩選準則加入至集合。</span><span class="sxs-lookup"><span data-stu-id="0af8b-120">Adds a new filter to the collection.</span></span> <br/>             |
| [<span data-ttu-id="0af8b-121">**清楚**</span><span class="sxs-lookup"><span data-stu-id="0af8b-121">**clear**</span></span>](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | <span data-ttu-id="0af8b-122">唯寫</span><span class="sxs-lookup"><span data-stu-id="0af8b-122">Write-only</span></span><br/> | <span data-ttu-id="0af8b-123">清除集合。</span><span class="sxs-lookup"><span data-stu-id="0af8b-123">Clears the collection.</span></span> <br/>                           |
| [<span data-ttu-id="0af8b-124">**計數**</span><span class="sxs-lookup"><span data-stu-id="0af8b-124">**Count**</span></span>](-search-2x-ipropertyfiltercollection-count.md)<br/>           | <span data-ttu-id="0af8b-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="0af8b-125">Read-only</span></span><br/>  | <span data-ttu-id="0af8b-126">集合中的篩選數目。</span><span class="sxs-lookup"><span data-stu-id="0af8b-126">Number of filters in the collection.</span></span> <br/>             |
| [<span data-ttu-id="0af8b-127">**GetITem**</span><span class="sxs-lookup"><span data-stu-id="0af8b-127">**GetITem**</span></span>](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | <span data-ttu-id="0af8b-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0af8b-128">Read/write</span></span><br/> | <span data-ttu-id="0af8b-129">傳回集合中的特定篩選。</span><span class="sxs-lookup"><span data-stu-id="0af8b-129">Returns a specific filter within the collection.</span></span> <br/> |
| [<span data-ttu-id="0af8b-130">**RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="0af8b-130">**RemoveItem**</span></span>](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | <span data-ttu-id="0af8b-131">唯寫</span><span class="sxs-lookup"><span data-stu-id="0af8b-131">Write-only</span></span><br/> | <span data-ttu-id="0af8b-132">移除集合中的特定篩選。</span><span class="sxs-lookup"><span data-stu-id="0af8b-132">Removes a specific filter to the collection.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="0af8b-133">備註</span><span class="sxs-lookup"><span data-stu-id="0af8b-133">Remarks</span></span>

<span data-ttu-id="0af8b-134">這些屬性是用來篩選查詢所傳回的集合。</span><span class="sxs-lookup"><span data-stu-id="0af8b-134">These properties are used to filter collection returned by the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="0af8b-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="0af8b-135">Requirements</span></span>



| <span data-ttu-id="0af8b-136">需求</span><span class="sxs-lookup"><span data-stu-id="0af8b-136">Requirement</span></span> | <span data-ttu-id="0af8b-137">值</span><span class="sxs-lookup"><span data-stu-id="0af8b-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af8b-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0af8b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0af8b-139">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0af8b-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0af8b-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0af8b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0af8b-141">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0af8b-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0af8b-142">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0af8b-142">Redistributable</span></span><br/>          | <span data-ttu-id="0af8b-143">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="0af8b-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="0af8b-144">標頭</span><span class="sxs-lookup"><span data-stu-id="0af8b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0af8b-145"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="0af8b-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

