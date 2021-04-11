---
title: 'TBM_GETLINESIZE 訊息 (Commctrl .h) '
description: 抓取捲軸滑動軸移動以回應鍵盤輸入的邏輯位置數目，例如，或索引鍵。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- TBM_GETLINESIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935152"
---
# <a name="tbm_getlinesize-message"></a><span data-ttu-id="f0a20-105">TBM \_ GETLINESIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="f0a20-105">TBM\_GETLINESIZE message</span></span>

<span data-ttu-id="f0a20-106">抓取捲軸滑動軸移動以回應鍵盤輸入的邏輯位置數目，例如，或索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f0a20-106">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="f0a20-107">邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。</span><span class="sxs-lookup"><span data-stu-id="f0a20-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0a20-108">參數</span><span class="sxs-lookup"><span data-stu-id="f0a20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0a20-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0a20-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f0a20-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f0a20-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f0a20-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0a20-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f0a20-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f0a20-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0a20-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0a20-113">Return value</span></span>

<span data-ttu-id="f0a20-114">傳回32位的值，這個值會指定列的行大小。</span><span class="sxs-lookup"><span data-stu-id="f0a20-114">Returns a 32-bit value that specifies the line size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0a20-115">備註</span><span class="sxs-lookup"><span data-stu-id="f0a20-115">Remarks</span></span>

<span data-ttu-id="f0a20-116">行大小的預設設定為1。</span><span class="sxs-lookup"><span data-stu-id="f0a20-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="f0a20-117">當使用者按下方向鍵時，此項資訊也會將具有 TB 組合和 TB LINEDOWN 通知碼的 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送 \_ \_ 至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="f0a20-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a20-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0a20-118">Requirements</span></span>



| <span data-ttu-id="f0a20-119">需求</span><span class="sxs-lookup"><span data-stu-id="f0a20-119">Requirement</span></span> | <span data-ttu-id="f0a20-120">值</span><span class="sxs-lookup"><span data-stu-id="f0a20-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a20-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0a20-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a20-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0a20-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0a20-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0a20-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a20-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0a20-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0a20-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f0a20-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0a20-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0a20-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





