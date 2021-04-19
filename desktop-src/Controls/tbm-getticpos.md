---
title: 'TBM_GETTICPOS 訊息 (Commctrl .h) '
description: 抓取刻度中刻度標記目前的實體位置。
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966114"
---
# <a name="tbm_getticpos-message"></a><span data-ttu-id="c78d6-104">TBM \_ GETTICPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="c78d6-104">TBM\_GETTICPOS message</span></span>

<span data-ttu-id="c78d6-105">抓取刻度中刻度標記目前的實體位置。</span><span class="sxs-lookup"><span data-stu-id="c78d6-105">Retrieves the current physical position of a tick mark in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c78d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="c78d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c78d6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c78d6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c78d6-108">以零為基底的索引，識別刻度。</span><span class="sxs-lookup"><span data-stu-id="c78d6-108">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="c78d6-109">第一個和最後一個刻度的位置無法透過此訊息直接使用。</span><span class="sxs-lookup"><span data-stu-id="c78d6-109">The positions of the first and last tick marks are not directly available via this message.</span></span>

</dd> <dt>

<span data-ttu-id="c78d6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c78d6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c78d6-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c78d6-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c78d6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c78d6-112">Return value</span></span>

<span data-ttu-id="c78d6-113">傳回用戶端座標中的距離（以客戶座標為單位），從頁首的工作區左邊或頂端到指定的刻度。</span><span class="sxs-lookup"><span data-stu-id="c78d6-113">Returns the distance, in client coordinates, from the left or top of the trackbar's client area to the specified tick mark.</span></span> <span data-ttu-id="c78d6-114">傳回值是水準交叉標記之刻度的 x 座標，或垂直橫條的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="c78d6-114">The return value is the x-coordinate of the tick mark for a horizontal trackbar or the y-coordinate for a vertical trackbar.</span></span> <span data-ttu-id="c78d6-115">如果 *wParam* 不是有效的索引，則傳回值為-1。</span><span class="sxs-lookup"><span data-stu-id="c78d6-115">If *wParam* is not a valid index, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="c78d6-116">備註</span><span class="sxs-lookup"><span data-stu-id="c78d6-116">Remarks</span></span>

<span data-ttu-id="c78d6-117">因為第一個和最後一個刻度無法透過這則訊息來使用，所以有效的索引會在其刻度上與其刻度位置位移。</span><span class="sxs-lookup"><span data-stu-id="c78d6-117">Because the first and last tick marks are not available through this message, valid indexes are offset from their tick position on the trackbar.</span></span> <span data-ttu-id="c78d6-118">如果 [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) 和 [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) 之間的差異小於二，則沒有有效的索引，而且此訊息將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c78d6-118">If the difference between [**TBM\_GETRANGEMIN**](tbm-getrangemin.md) and [**TBM\_GETRANGEMAX**](tbm-getrangemax.md) is less than two, then there is no valid index and this message will fail.</span></span>

<span data-ttu-id="c78d6-119">以下說明在顯示的刻度之間的關聯性、由此訊息提供的刻度，以及其以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="c78d6-119">The following illustrates the relation between the ticks on a trackbar, the ticks available through this message, and their zero-based indexes.</span></span>

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a><span data-ttu-id="c78d6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c78d6-120">Requirements</span></span>



| <span data-ttu-id="c78d6-121">需求</span><span class="sxs-lookup"><span data-stu-id="c78d6-121">Requirement</span></span> | <span data-ttu-id="c78d6-122">值</span><span class="sxs-lookup"><span data-stu-id="c78d6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c78d6-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c78d6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c78d6-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c78d6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c78d6-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c78d6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c78d6-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c78d6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c78d6-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c78d6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c78d6-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c78d6-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





