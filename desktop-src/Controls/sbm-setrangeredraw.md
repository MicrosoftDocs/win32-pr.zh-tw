---
title: 'SBM_SETRANGEREDRAW 訊息 (Winuser .h) '
description: 應用程式會將 SBM \_ SETRANGEREDRAW 訊息傳送到捲軸控制項，以設定最小和最大位置值，以及重新繪製控制項。
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- SBM_SETRANGEREDRAW message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024578"
---
# <a name="sbm_setrangeredraw-message"></a><span data-ttu-id="dc01a-104">SBM \_ SETRANGEREDRAW 訊息</span><span class="sxs-lookup"><span data-stu-id="dc01a-104">SBM\_SETRANGEREDRAW message</span></span>

<span data-ttu-id="dc01a-105">應用程式會將 **SBM \_ SETRANGEREDRAW** 訊息傳送到捲軸控制項，以設定最小和最大位置值，以及重新繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="dc01a-105">An application sends the **SBM\_SETRANGEREDRAW** message to a scroll bar control to set the minimum and maximum position values and to redraw the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc01a-106">參數</span><span class="sxs-lookup"><span data-stu-id="dc01a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc01a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc01a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc01a-108">指定最小滾動位置。</span><span class="sxs-lookup"><span data-stu-id="dc01a-108">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="dc01a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc01a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc01a-110">指定最大滾動位置。</span><span class="sxs-lookup"><span data-stu-id="dc01a-110">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc01a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc01a-111">Return value</span></span>

<span data-ttu-id="dc01a-112">**ComCtl32.dll 5.0 版**：如果捲動方塊的位置已變更，則傳回值是捲動方塊的先前位置;否則，它是零。</span><span class="sxs-lookup"><span data-stu-id="dc01a-112">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="dc01a-113">**ComCtl32.dll 版本 6.0**：捲動方塊的目前位置，不論是否已變更。</span><span class="sxs-lookup"><span data-stu-id="dc01a-113">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc01a-114">備註</span><span class="sxs-lookup"><span data-stu-id="dc01a-114">Remarks</span></span>

<span data-ttu-id="dc01a-115">預設的最小和最大位置值為零。</span><span class="sxs-lookup"><span data-stu-id="dc01a-115">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="dc01a-116">*WParam* 和 *lParam* 參數所指定值之間的差異不得大於 MAXLONG。</span><span class="sxs-lookup"><span data-stu-id="dc01a-116">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="dc01a-117">如果最小和最大位置值相等，則捲軸控制項是隱藏的，且實際上是停用的。</span><span class="sxs-lookup"><span data-stu-id="dc01a-117">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc01a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc01a-118">Requirements</span></span>



| <span data-ttu-id="dc01a-119">需求</span><span class="sxs-lookup"><span data-stu-id="dc01a-119">Requirement</span></span> | <span data-ttu-id="dc01a-120">值</span><span class="sxs-lookup"><span data-stu-id="dc01a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc01a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc01a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc01a-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc01a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dc01a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc01a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc01a-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc01a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc01a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="dc01a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc01a-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="dc01a-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc01a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc01a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc01a-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="dc01a-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dc01a-129">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="dc01a-129">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="dc01a-130">**SBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="dc01a-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="dc01a-131">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="dc01a-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="dc01a-132">**SBM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="dc01a-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> </dl>

 

 





