---
title: 'EM_SHOWSCROLLBAR 訊息 (Richedit .h) '
description: 顯示或隱藏 rich edit 控制項主視窗中的其中一個捲軸。
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- EM_SHOWSCROLLBAR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934273"
---
# <a name="em_showscrollbar-message"></a><span data-ttu-id="33910-104">EM \_ SHOWSCROLLBAR 訊息</span><span class="sxs-lookup"><span data-stu-id="33910-104">EM\_SHOWSCROLLBAR message</span></span>

<span data-ttu-id="33910-105">顯示或隱藏 rich edit 控制項主視窗中的其中一個捲軸。</span><span class="sxs-lookup"><span data-stu-id="33910-105">Shows or hides one of the scroll bars in the host window of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="33910-106">參數</span><span class="sxs-lookup"><span data-stu-id="33910-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33910-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33910-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33910-108">識別要顯示的捲軸：水準或垂直。</span><span class="sxs-lookup"><span data-stu-id="33910-108">Identifies which scroll bar to display: horizontal or vertical.</span></span> <span data-ttu-id="33910-109">此參數必須是 **sb \_ 垂直** 或 **sb \_ HORZ**。</span><span class="sxs-lookup"><span data-stu-id="33910-109">This parameter must be **SB\_VERT** or **SB\_HORZ**.</span></span>

</dd> <dt>

<span data-ttu-id="33910-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33910-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33910-111">指定是否要顯示捲軸或隱藏捲軸。</span><span class="sxs-lookup"><span data-stu-id="33910-111">Specifies whether to show the scroll bar or hide it.</span></span> <span data-ttu-id="33910-112">指定 **TRUE** 可顯示捲軸，而 **FALSE** 則會隱藏。</span><span class="sxs-lookup"><span data-stu-id="33910-112">Specify **TRUE** to show the scroll bar and **FALSE** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33910-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="33910-113">Return value</span></span>

<span data-ttu-id="33910-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="33910-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33910-115">備註</span><span class="sxs-lookup"><span data-stu-id="33910-115">Remarks</span></span>

<span data-ttu-id="33910-116">只有在控制項為就地使用中時，此方法才有效。</span><span class="sxs-lookup"><span data-stu-id="33910-116">This method is only valid when the control is in-place active.</span></span> <span data-ttu-id="33910-117">控制項處於非使用中狀態時所發出的呼叫可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="33910-117">Calls made while the control is inactive may fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="33910-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="33910-118">Requirements</span></span>



| <span data-ttu-id="33910-119">需求</span><span class="sxs-lookup"><span data-stu-id="33910-119">Requirement</span></span> | <span data-ttu-id="33910-120">值</span><span class="sxs-lookup"><span data-stu-id="33910-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33910-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33910-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33910-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33910-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33910-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33910-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33910-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33910-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33910-125">標頭</span><span class="sxs-lookup"><span data-stu-id="33910-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="33910-126"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="33910-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33910-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33910-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="33910-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="33910-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="33910-129">**EM \_ GETSCROLLPOS**</span><span class="sxs-lookup"><span data-stu-id="33910-129">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> <dt>

[<span data-ttu-id="33910-130">**EM \_ SETSCROLLPOS**</span><span class="sxs-lookup"><span data-stu-id="33910-130">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

 





