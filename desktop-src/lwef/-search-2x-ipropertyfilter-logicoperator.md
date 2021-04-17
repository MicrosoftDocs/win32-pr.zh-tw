---
title: 'IPropertyFilter LogicOperator 屬性 (WdsSharedIDL .h) '
description: 套用篩選時要使用的邏輯運算子。
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- LogicOperator 屬性舊版 Windows 環境功能
- LogicOperator 屬性舊版 Windows 環境功能，IPropertyFilter 介面
- IPropertyFilter 介面舊版 Windows 環境功能，LogicOperator 屬性
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c514ae6231a9d83063b4a294680bdd3949c91102
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466945"
---
# <a name="ipropertyfilterlogicoperator-property"></a><span data-ttu-id="cc21a-106">IPropertyFilter：： LogicOperator 屬性</span><span class="sxs-lookup"><span data-stu-id="cc21a-106">IPropertyFilter::LogicOperator property</span></span>

> [!NOTE]
> <span data-ttu-id="cc21a-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="cc21a-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cc21a-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="cc21a-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="cc21a-109">套用篩選時要使用的邏輯運算子。</span><span class="sxs-lookup"><span data-stu-id="cc21a-109">Logic Operator to use when applying a filter.</span></span>

<span data-ttu-id="cc21a-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cc21a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc21a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc21a-111">Syntax</span></span>


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a><span data-ttu-id="cc21a-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="cc21a-112">Property value</span></span>

<span data-ttu-id="cc21a-113">設定邏輯運算子類型。</span><span class="sxs-lookup"><span data-stu-id="cc21a-113">Sets the logic operator type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc21a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc21a-114">Requirements</span></span>



| <span data-ttu-id="cc21a-115">需求</span><span class="sxs-lookup"><span data-stu-id="cc21a-115">Requirement</span></span> | <span data-ttu-id="cc21a-116">值</span><span class="sxs-lookup"><span data-stu-id="cc21a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc21a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc21a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc21a-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc21a-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cc21a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc21a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc21a-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc21a-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cc21a-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="cc21a-121">Redistributable</span></span><br/>          | <span data-ttu-id="cc21a-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="cc21a-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="cc21a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="cc21a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc21a-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="cc21a-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





