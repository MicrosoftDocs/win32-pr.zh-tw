---
title: 'TBM_GETSELEND 訊息 (Commctrl .h) '
description: 抓取目前選取範圍的結束位置。
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- TBM_GETSELEND message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 486d66d3e7fc2dd4d23b89cb5e9406fa81b34638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465365"
---
# <a name="tbm_getselend-message"></a><span data-ttu-id="6a4ac-104">TBM \_ GETSELEND 訊息</span><span class="sxs-lookup"><span data-stu-id="6a4ac-104">TBM\_GETSELEND message</span></span>

<span data-ttu-id="6a4ac-105">抓取目前選取範圍的結束位置。</span><span class="sxs-lookup"><span data-stu-id="6a4ac-105">Retrieves the ending position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a4ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a4ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a4ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a4ac-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6a4ac-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6a4ac-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6a4ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a4ac-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6a4ac-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6a4ac-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a4ac-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a4ac-111">Return value</span></span>

<span data-ttu-id="6a4ac-112">傳回32位值，指定目前選取範圍的結束位置。</span><span class="sxs-lookup"><span data-stu-id="6a4ac-112">Returns a 32-bit value that specifies the ending position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a4ac-113">備註</span><span class="sxs-lookup"><span data-stu-id="6a4ac-113">Remarks</span></span>

<span data-ttu-id="6a4ac-114">只有當您在建立時，如果您已指定 [ [**tb] \_ ENABLESELRANGE**](trackbar-control-styles.md) 樣式，則會有一個選取範圍。</span><span class="sxs-lookup"><span data-stu-id="6a4ac-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a4ac-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a4ac-115">Requirements</span></span>



| <span data-ttu-id="6a4ac-116">需求</span><span class="sxs-lookup"><span data-stu-id="6a4ac-116">Requirement</span></span> | <span data-ttu-id="6a4ac-117">值</span><span class="sxs-lookup"><span data-stu-id="6a4ac-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4ac-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a4ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6a4ac-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a4ac-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a4ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6a4ac-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a4ac-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6a4ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a4ac-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a4ac-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a4ac-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a4ac-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="6a4ac-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6a4ac-126">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="6a4ac-126">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="6a4ac-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="6a4ac-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="6a4ac-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="6a4ac-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="6a4ac-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="6a4ac-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





