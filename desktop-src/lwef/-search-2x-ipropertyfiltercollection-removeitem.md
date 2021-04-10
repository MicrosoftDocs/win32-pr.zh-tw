---
title: 'IPropertyFilterCollection RemoveItem 屬性 (WdsSharedIDL .h) '
description: 移除集合中的特定篩選。
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- RemoveItem 屬性舊版 Windows 環境功能
- RemoveItem 屬性舊版 Windows 環境功能，IPropertyFilterCollection 介面
- IPropertyFilterCollection 介面舊版 Windows 環境功能，RemoveItem 屬性
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2994b636a7b8483d4b3f219648f137166b75790d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686114"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a><span data-ttu-id="b13b7-106">IPropertyFilterCollection：： RemoveItem 屬性</span><span class="sxs-lookup"><span data-stu-id="b13b7-106">IPropertyFilterCollection::RemoveItem property</span></span>

> [!NOTE]
> <span data-ttu-id="b13b7-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="b13b7-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b13b7-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="b13b7-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="b13b7-109">移除集合中的特定篩選。</span><span class="sxs-lookup"><span data-stu-id="b13b7-109">Removes a specific filter to the collection.</span></span>

<span data-ttu-id="b13b7-110">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="b13b7-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b13b7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b13b7-111">Syntax</span></span>


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a><span data-ttu-id="b13b7-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="b13b7-112">Property value</span></span>

<span data-ttu-id="b13b7-113">接受要移除之篩選的索引指標。</span><span class="sxs-lookup"><span data-stu-id="b13b7-113">Accepts a pointer to the index for the filter to be removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b13b7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b13b7-114">Requirements</span></span>



| <span data-ttu-id="b13b7-115">需求</span><span class="sxs-lookup"><span data-stu-id="b13b7-115">Requirement</span></span> | <span data-ttu-id="b13b7-116">值</span><span class="sxs-lookup"><span data-stu-id="b13b7-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b13b7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b13b7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b13b7-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b13b7-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b13b7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b13b7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b13b7-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b13b7-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b13b7-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b13b7-121">Redistributable</span></span><br/>          | <span data-ttu-id="b13b7-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="b13b7-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="b13b7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b13b7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b13b7-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="b13b7-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





