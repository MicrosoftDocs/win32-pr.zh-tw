---
title: 'UDM_SETPOS32 訊息 (Commctrl .h) '
description: 設定具有32位精確度的上下按鈕控制項的位置。
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- UDM_SETPOS32 message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934699"
---
# <a name="udm_setpos32-message"></a><span data-ttu-id="97063-104">UDM \_ SETPOS32 訊息</span><span class="sxs-lookup"><span data-stu-id="97063-104">UDM\_SETPOS32 message</span></span>

<span data-ttu-id="97063-105">設定具有32位精確度的上下按鈕控制項的位置。</span><span class="sxs-lookup"><span data-stu-id="97063-105">Sets the position of an up-down control with 32-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="97063-106">參數</span><span class="sxs-lookup"><span data-stu-id="97063-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97063-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97063-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="97063-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="97063-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="97063-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97063-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97063-110">整數類型的變數，指定上下按鈕控制項的新位置。</span><span class="sxs-lookup"><span data-stu-id="97063-110">Variable of type integer that specifies the new position for the up-down control.</span></span> <span data-ttu-id="97063-111">如果參數超出控制項的指定範圍， *lParam* 會設為最接近的有效值。</span><span class="sxs-lookup"><span data-stu-id="97063-111">If the parameter is outside the control's specified range, *lParam* is set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97063-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="97063-112">Return value</span></span>

<span data-ttu-id="97063-113">傳回先前的位置。</span><span class="sxs-lookup"><span data-stu-id="97063-113">Returns the previous position.</span></span>

## <a name="requirements"></a><span data-ttu-id="97063-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="97063-114">Requirements</span></span>



| <span data-ttu-id="97063-115">需求</span><span class="sxs-lookup"><span data-stu-id="97063-115">Requirement</span></span> | <span data-ttu-id="97063-116">值</span><span class="sxs-lookup"><span data-stu-id="97063-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97063-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97063-117">Minimum supported client</span></span><br/> | <span data-ttu-id="97063-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97063-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97063-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97063-119">Minimum supported server</span></span><br/> | <span data-ttu-id="97063-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97063-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97063-121">標頭</span><span class="sxs-lookup"><span data-stu-id="97063-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="97063-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="97063-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97063-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97063-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="97063-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="97063-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97063-125">**UDM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="97063-125">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="97063-126">**UDM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="97063-126">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="97063-127">**UDM \_ GETPOS32**</span><span class="sxs-lookup"><span data-stu-id="97063-127">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)
</dt> </dl>

 

 





