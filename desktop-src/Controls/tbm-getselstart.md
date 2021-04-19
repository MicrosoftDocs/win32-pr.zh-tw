---
title: 'TBM_GETSELSTART 訊息 (Commctrl .h) '
description: 抓取目前選取範圍在 [選取範圍] 中的開始位置。
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- TBM_GETSELSTART message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af796c57adb3615241a8f5b702ff58062468509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965904"
---
# <a name="tbm_getselstart-message"></a><span data-ttu-id="1520b-104">TBM \_ GETSELSTART 訊息</span><span class="sxs-lookup"><span data-stu-id="1520b-104">TBM\_GETSELSTART message</span></span>

<span data-ttu-id="1520b-105">抓取目前選取範圍在 [選取範圍] 中的開始位置。</span><span class="sxs-lookup"><span data-stu-id="1520b-105">Retrieves the starting position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1520b-106">參數</span><span class="sxs-lookup"><span data-stu-id="1520b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1520b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1520b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1520b-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1520b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1520b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1520b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1520b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1520b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1520b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1520b-111">Return value</span></span>

<span data-ttu-id="1520b-112">傳回32位值，指定目前選取範圍的開始位置。</span><span class="sxs-lookup"><span data-stu-id="1520b-112">Returns a 32-bit value that specifies the starting position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="1520b-113">備註</span><span class="sxs-lookup"><span data-stu-id="1520b-113">Remarks</span></span>

<span data-ttu-id="1520b-114">只有當您在建立時，如果您已指定 [ [**tb] \_ ENABLESELRANGE**](trackbar-control-styles.md) 樣式，則會有一個選取範圍。</span><span class="sxs-lookup"><span data-stu-id="1520b-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1520b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1520b-115">Requirements</span></span>



| <span data-ttu-id="1520b-116">需求</span><span class="sxs-lookup"><span data-stu-id="1520b-116">Requirement</span></span> | <span data-ttu-id="1520b-117">值</span><span class="sxs-lookup"><span data-stu-id="1520b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1520b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1520b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1520b-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1520b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1520b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1520b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1520b-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1520b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1520b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1520b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1520b-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1520b-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1520b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1520b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="1520b-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="1520b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1520b-126">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="1520b-126">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="1520b-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="1520b-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="1520b-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="1520b-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="1520b-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="1520b-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





