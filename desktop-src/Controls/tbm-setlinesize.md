---
title: 'TBM_SETLINESIZE 訊息 (Commctrl .h) '
description: 設定從箭號按鍵（例如，或按鍵）回應鍵盤輸入時，會將這些捲軸滑杆移動的邏輯位置數目。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- TBM_SETLINESIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934043"
---
# <a name="tbm_setlinesize-message"></a><span data-ttu-id="d0462-105">TBM \_ SETLINESIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="d0462-105">TBM\_SETLINESIZE message</span></span>

<span data-ttu-id="d0462-106">設定從箭號按鍵（例如，或按鍵）回應鍵盤輸入時，會將這些捲軸滑杆移動的邏輯位置數目。</span><span class="sxs-lookup"><span data-stu-id="d0462-106">Sets the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="d0462-107">邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。</span><span class="sxs-lookup"><span data-stu-id="d0462-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0462-108">參數</span><span class="sxs-lookup"><span data-stu-id="d0462-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0462-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0462-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d0462-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d0462-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d0462-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0462-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0462-112">新行大小。</span><span class="sxs-lookup"><span data-stu-id="d0462-112">New line size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0462-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0462-113">Return value</span></span>

<span data-ttu-id="d0462-114">傳回指定前一行大小的32位值。</span><span class="sxs-lookup"><span data-stu-id="d0462-114">Returns a 32-bit value that specifies the previous line size.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0462-115">備註</span><span class="sxs-lookup"><span data-stu-id="d0462-115">Remarks</span></span>

<span data-ttu-id="d0462-116">行大小的預設設定為1。</span><span class="sxs-lookup"><span data-stu-id="d0462-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="d0462-117">當使用者按下方向鍵時，此項資訊也會將具有 TB 組合和 TB LINEDOWN 通知碼的 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送 \_ \_ 至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="d0462-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0462-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0462-118">Requirements</span></span>



| <span data-ttu-id="d0462-119">需求</span><span class="sxs-lookup"><span data-stu-id="d0462-119">Requirement</span></span> | <span data-ttu-id="d0462-120">值</span><span class="sxs-lookup"><span data-stu-id="d0462-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0462-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0462-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d0462-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0462-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0462-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0462-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d0462-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0462-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0462-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d0462-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0462-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0462-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0462-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0462-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0462-128">**TBM \_ GETLINESIZE**</span><span class="sxs-lookup"><span data-stu-id="d0462-128">**TBM\_GETLINESIZE**</span></span>](tbm-getlinesize.md)
</dt> </dl>

 

 





