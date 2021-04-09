---
title: 'UDM_SETRANGE 訊息 (Commctrl .h) '
description: 設定上下按鈕 (範圍) 的最小和最大位置。
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- UDM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025275"
---
# <a name="udm_setrange-message"></a><span data-ttu-id="02a32-104">UDM \_ SETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="02a32-104">UDM\_SETRANGE message</span></span>

<span data-ttu-id="02a32-105">設定上下按鈕 (範圍) 的最小和最大位置。</span><span class="sxs-lookup"><span data-stu-id="02a32-105">Sets the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="02a32-106">參數</span><span class="sxs-lookup"><span data-stu-id="02a32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a32-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02a32-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="02a32-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="02a32-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="02a32-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02a32-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02a32-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是指定上下按鈕控制項最大位置的 **短**，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))則是指定最小位置的 **簡短**。</span><span class="sxs-lookup"><span data-stu-id="02a32-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **short** that specifies the maximum position for the up-down control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **short** that specifies the minimum position.</span></span> <span data-ttu-id="02a32-111">這兩個位置都不能大於 UD \_ MAXVAL 值或小於 ud \_ MINVAL 值。</span><span class="sxs-lookup"><span data-stu-id="02a32-111">Neither position can be greater than the UD\_MAXVAL value or less than the UD\_MINVAL value.</span></span> <span data-ttu-id="02a32-112">此外，兩個位置之間的差異不能超過 UD \_ MAXVAL。</span><span class="sxs-lookup"><span data-stu-id="02a32-112">In addition, the difference between the two positions cannot exceed UD\_MAXVAL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a32-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="02a32-113">Return value</span></span>

<span data-ttu-id="02a32-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="02a32-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02a32-115">備註</span><span class="sxs-lookup"><span data-stu-id="02a32-115">Remarks</span></span>

<span data-ttu-id="02a32-116">最大位置可能小於最小位置。</span><span class="sxs-lookup"><span data-stu-id="02a32-116">The maximum position can be less than the minimum position.</span></span> <span data-ttu-id="02a32-117">按一下向上箭號按鈕，將目前的位置向下移動到最大位置，然後按一下向下箭號按鈕移至最小位置。</span><span class="sxs-lookup"><span data-stu-id="02a32-117">Clicking the up arrow button moves the current position closer to the maximum position, and clicking the down arrow button moves toward the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a32-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="02a32-118">Requirements</span></span>



| <span data-ttu-id="02a32-119">需求</span><span class="sxs-lookup"><span data-stu-id="02a32-119">Requirement</span></span> | <span data-ttu-id="02a32-120">值</span><span class="sxs-lookup"><span data-stu-id="02a32-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02a32-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02a32-121">Minimum supported client</span></span><br/> | <span data-ttu-id="02a32-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02a32-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02a32-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02a32-123">Minimum supported server</span></span><br/> | <span data-ttu-id="02a32-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02a32-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02a32-125">標頭</span><span class="sxs-lookup"><span data-stu-id="02a32-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="02a32-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="02a32-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02a32-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02a32-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a32-128">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="02a32-128">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="02a32-129">**UDM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="02a32-129">**UDM\_SETRANGE**</span></span>](udm-setrange.md)
</dt> </dl>

 

