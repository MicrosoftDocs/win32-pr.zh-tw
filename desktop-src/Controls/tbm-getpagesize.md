---
title: 'TBM_GETPAGESIZE 訊息 (Commctrl .h) '
description: 抓取捲軸的滑杆為了回應鍵盤輸入（例如或按鍵）或滑鼠輸入而移動的邏輯位置數目，例如在並排條的通道中按一下。
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- TBM_GETPAGESIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103757"
---
# <a name="tbm_getpagesize-message"></a><span data-ttu-id="80460-104">TBM \_ GETPAGESIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="80460-104">TBM\_GETPAGESIZE message</span></span>

<span data-ttu-id="80460-105">抓取捲軸的滑杆為了回應鍵盤輸入（例如或按鍵）或滑鼠輸入而移動的邏輯位置數目，例如在並排條的通道中按一下。</span><span class="sxs-lookup"><span data-stu-id="80460-105">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="80460-106">邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。</span><span class="sxs-lookup"><span data-stu-id="80460-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="80460-107">參數</span><span class="sxs-lookup"><span data-stu-id="80460-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80460-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80460-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="80460-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="80460-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="80460-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80460-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="80460-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="80460-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80460-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="80460-112">Return value</span></span>

<span data-ttu-id="80460-113">傳回指定頁尾頁面大小的32位值。</span><span class="sxs-lookup"><span data-stu-id="80460-113">Returns a 32-bit value that specifies the page size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="80460-114">備註</span><span class="sxs-lookup"><span data-stu-id="80460-114">Remarks</span></span>

<span data-ttu-id="80460-115">當您收到滾動頁的鍵盤或滑鼠輸入時，這些頁首也會將具有 TB PAGEUP 和 TB PAGEDOWN 通知碼的 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送 \_ \_ 至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="80460-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="80460-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="80460-116">Requirements</span></span>



| <span data-ttu-id="80460-117">需求</span><span class="sxs-lookup"><span data-stu-id="80460-117">Requirement</span></span> | <span data-ttu-id="80460-118">值</span><span class="sxs-lookup"><span data-stu-id="80460-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80460-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80460-119">Minimum supported client</span></span><br/> | <span data-ttu-id="80460-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80460-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80460-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80460-121">Minimum supported server</span></span><br/> | <span data-ttu-id="80460-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80460-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80460-123">標頭</span><span class="sxs-lookup"><span data-stu-id="80460-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="80460-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="80460-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80460-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80460-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80460-126">**TBM \_ >SETPAGESIZE METHOD**</span><span class="sxs-lookup"><span data-stu-id="80460-126">**TBM\_SETPAGESIZE**</span></span>](tbm-setpagesize.md)
</dt> </dl>

 

 





