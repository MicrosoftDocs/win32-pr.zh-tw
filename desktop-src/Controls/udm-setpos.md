---
title: 'UDM_SETPOS 訊息 (Commctrl .h) '
description: 設定具有16位精確度之上下按鈕控制項的目前位置。
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- UDM_SETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104760"
---
# <a name="udm_setpos-message"></a><span data-ttu-id="35d0b-104">UDM \_ SETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="35d0b-104">UDM\_SETPOS message</span></span>

<span data-ttu-id="35d0b-105">設定具有16位精確度之上下按鈕控制項的目前位置。</span><span class="sxs-lookup"><span data-stu-id="35d0b-105">Sets the current position for an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="35d0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="35d0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35d0b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35d0b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="35d0b-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="35d0b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="35d0b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35d0b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35d0b-110">上下按鈕控制項的新位置。</span><span class="sxs-lookup"><span data-stu-id="35d0b-110">New position for the up-down control.</span></span> <span data-ttu-id="35d0b-111">如果參數超出控制項的指定範圍， *lParam* 會設為最接近的有效值。</span><span class="sxs-lookup"><span data-stu-id="35d0b-111">If the parameter is outside the control's specified range, *lParam* will be set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35d0b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="35d0b-112">Return value</span></span>

<span data-ttu-id="35d0b-113">傳回值是先前的位置。</span><span class="sxs-lookup"><span data-stu-id="35d0b-113">The return value is the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="35d0b-114">備註</span><span class="sxs-lookup"><span data-stu-id="35d0b-114">Remarks</span></span>

<span data-ttu-id="35d0b-115">此訊息僅支援16位的位置。</span><span class="sxs-lookup"><span data-stu-id="35d0b-115">This message only supports 16-bit positions.</span></span> <span data-ttu-id="35d0b-116">如果已針對具有 [**UDM \_ SETRANGE32**](udm-setrange32.md)的上下控制項啟用32位值，請使用 [**udm \_ SETPOS32**](udm-setpos32.md)。</span><span class="sxs-lookup"><span data-stu-id="35d0b-116">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), use [**UDM\_SETPOS32**](udm-setpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35d0b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="35d0b-117">Requirements</span></span>



| <span data-ttu-id="35d0b-118">需求</span><span class="sxs-lookup"><span data-stu-id="35d0b-118">Requirement</span></span> | <span data-ttu-id="35d0b-119">值</span><span class="sxs-lookup"><span data-stu-id="35d0b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35d0b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35d0b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="35d0b-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35d0b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35d0b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35d0b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="35d0b-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35d0b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35d0b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="35d0b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="35d0b-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="35d0b-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d0b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35d0b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="35d0b-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="35d0b-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35d0b-128">**UDM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="35d0b-128">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="35d0b-129">**UDM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="35d0b-129">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> </dl>

 

 





