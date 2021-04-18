---
title: 'UDM_GETPOS 訊息 (Commctrl .h) '
description: 抓取具有16位精確度之上下按鈕控制項的目前位置。
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- UDM_GETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968539"
---
# <a name="udm_getpos-message"></a><span data-ttu-id="72433-104">UDM \_ GETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="72433-104">UDM\_GETPOS message</span></span>

<span data-ttu-id="72433-105">抓取具有16位精確度之上下按鈕控制項的目前位置。</span><span class="sxs-lookup"><span data-stu-id="72433-105">Retrieves the current position of an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="72433-106">參數</span><span class="sxs-lookup"><span data-stu-id="72433-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72433-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72433-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="72433-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="72433-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="72433-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72433-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="72433-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="72433-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72433-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="72433-111">Return value</span></span>

<span data-ttu-id="72433-112">如果成功， [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 會設為零，而且 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 會設定為控制項的目前位置。</span><span class="sxs-lookup"><span data-stu-id="72433-112">If successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is set to zero and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is set to the control's current position.</span></span> <span data-ttu-id="72433-113">如果發生錯誤， **HIWORD** 會設為非零值。</span><span class="sxs-lookup"><span data-stu-id="72433-113">If an error occurs, the **HIWORD** is set to a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72433-114">備註</span><span class="sxs-lookup"><span data-stu-id="72433-114">Remarks</span></span>

<span data-ttu-id="72433-115">處理此訊息時，上下按鈕控制項會根據好友視窗的標題來更新其目前位置。</span><span class="sxs-lookup"><span data-stu-id="72433-115">When processing this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="72433-116">如果沒有任何好友視窗，或標題指定無效或超出範圍的值，則會傳回一個錯誤。</span><span class="sxs-lookup"><span data-stu-id="72433-116">The up-down control returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span> <span data-ttu-id="72433-117">此外，如果在沒有 ud [**\_ SETBUDDYINT**](up-down-control-styles.md) 樣式的情況下建立控制項，則會在傳回的 HIWORD 中設定錯誤旗標，即使它在傳回的 LOWORD 中傳回有效的位置值也一樣。</span><span class="sxs-lookup"><span data-stu-id="72433-117">Also, an error flag is set in the HIWORD of the return if the control is created without the [**UDS\_SETBUDDYINT**](up-down-control-styles.md) style, even though it returns a valid position value in the LOWORD of the return.</span></span>

<span data-ttu-id="72433-118">如果已針對具有 [**UDM \_ SETRANGE32**](udm-setrange32.md)的上下按鈕啟用32位的值，則此訊息只會傳回位置的較低16位。</span><span class="sxs-lookup"><span data-stu-id="72433-118">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), this message returns only the lower 16 bits of the position.</span></span> <span data-ttu-id="72433-119">若要取得完整的32位位置，請使用 [**UDM \_ GETPOS32**](udm-getpos32.md)。</span><span class="sxs-lookup"><span data-stu-id="72433-119">To retrieve the full 32-bit position, use [**UDM\_GETPOS32**](udm-getpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72433-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="72433-120">Requirements</span></span>



| <span data-ttu-id="72433-121">需求</span><span class="sxs-lookup"><span data-stu-id="72433-121">Requirement</span></span> | <span data-ttu-id="72433-122">值</span><span class="sxs-lookup"><span data-stu-id="72433-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72433-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72433-123">Minimum supported client</span></span><br/> | <span data-ttu-id="72433-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72433-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72433-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72433-125">Minimum supported server</span></span><br/> | <span data-ttu-id="72433-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72433-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72433-127">標頭</span><span class="sxs-lookup"><span data-stu-id="72433-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="72433-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="72433-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72433-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72433-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="72433-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="72433-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="72433-131">**UDM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="72433-131">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="72433-132">**UDM \_ GETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="72433-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)
</dt> <dt>

[<span data-ttu-id="72433-133">**UDM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="72433-133">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="72433-134">**UDM \_ SETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="72433-134">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)
</dt> </dl>

 

