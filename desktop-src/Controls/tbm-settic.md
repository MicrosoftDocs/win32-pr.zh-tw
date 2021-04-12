---
title: 'TBM_SETTIC 訊息 (Commctrl .h) '
description: 在指定的邏輯位置的 [查看] 中設定刻度。
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094171"
---
# <a name="tbm_settic-message"></a><span data-ttu-id="568b2-104">TBM \_ SETTIC 訊息</span><span class="sxs-lookup"><span data-stu-id="568b2-104">TBM\_SETTIC message</span></span>

<span data-ttu-id="568b2-105">在指定的邏輯位置的 [查看] 中設定刻度。</span><span class="sxs-lookup"><span data-stu-id="568b2-105">Sets a tick mark in a trackbar at the specified logical position.</span></span>

## <a name="parameters"></a><span data-ttu-id="568b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="568b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="568b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="568b2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="568b2-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="568b2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="568b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="568b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="568b2-110">刻度的位置。</span><span class="sxs-lookup"><span data-stu-id="568b2-110">Position of the tick mark.</span></span> <span data-ttu-id="568b2-111">此參數可以是最小至最大滑杆位置的最小值範圍中的任何整數值。</span><span class="sxs-lookup"><span data-stu-id="568b2-111">This parameter can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="568b2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="568b2-112">Return value</span></span>

<span data-ttu-id="568b2-113">如果已設定刻度，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="568b2-113">Returns **TRUE** if the tick mark is set, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="568b2-114">備註</span><span class="sxs-lookup"><span data-stu-id="568b2-114">Remarks</span></span>

<span data-ttu-id="568b2-115">然後，會建立自己的第一個和最後一個刻度標記。</span><span class="sxs-lookup"><span data-stu-id="568b2-115">A trackbar creates its own first and last tick marks.</span></span> <span data-ttu-id="568b2-116">請勿使用此訊息來設定第一個和最後一個刻度標記。</span><span class="sxs-lookup"><span data-stu-id="568b2-116">Do not use this message to set the first and last tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="568b2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="568b2-117">Requirements</span></span>



| <span data-ttu-id="568b2-118">需求</span><span class="sxs-lookup"><span data-stu-id="568b2-118">Requirement</span></span> | <span data-ttu-id="568b2-119">值</span><span class="sxs-lookup"><span data-stu-id="568b2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="568b2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="568b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="568b2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="568b2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="568b2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="568b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="568b2-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="568b2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="568b2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="568b2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="568b2-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="568b2-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="568b2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="568b2-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="568b2-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="568b2-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="568b2-128">**TBM \_ GETPTICS**</span><span class="sxs-lookup"><span data-stu-id="568b2-128">**TBM\_GETPTICS**</span></span>](tbm-getptics.md)
</dt> <dt>

[<span data-ttu-id="568b2-129">**TBM \_ GETTIC**</span><span class="sxs-lookup"><span data-stu-id="568b2-129">**TBM\_GETTIC**</span></span>](tbm-gettic.md)
</dt> </dl>

 

 





