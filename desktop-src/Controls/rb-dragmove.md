---
title: 'RB_DRAGMOVE 訊息 (Commctrl .h) '
description: 更新在上一個 RB BEGINDRAG 訊息之後，Rebar 控制項中的拖曳位置 \_ 。
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE message Windows 控制項
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934711"
---
# <a name="rb_dragmove-message"></a><span data-ttu-id="ce2bf-104">RB \_ DRAGMOVE 訊息</span><span class="sxs-lookup"><span data-stu-id="ce2bf-104">RB\_DRAGMOVE message</span></span>

<span data-ttu-id="ce2bf-105">更新在上一個 [**RB \_ BEGINDRAG**](rb-begindrag.md) 訊息之後，Rebar 控制項中的拖曳位置。</span><span class="sxs-lookup"><span data-stu-id="ce2bf-105">Updates the drag position in the rebar control after a previous [**RB\_BEGINDRAG**](rb-begindrag.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce2bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="ce2bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce2bf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce2bf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce2bf-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ce2bf-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce2bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce2bf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce2bf-110">包含新滑鼠座標的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="ce2bf-110">**DWORD** value that contains the new mouse coordinates.</span></span> <span data-ttu-id="ce2bf-111">水準座標是包含在 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中，而垂直座標則是包含在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中。</span><span class="sxs-lookup"><span data-stu-id="ce2bf-111">The horizontal coordinate is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical coordinate is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="ce2bf-112">如果您傳遞 (DWORD) -1，Rebar 控制項將會使用滑鼠的位置，這是上一次控制項的執行緒，稱為 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage)。</span><span class="sxs-lookup"><span data-stu-id="ce2bf-112">If you pass (DWORD)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce2bf-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce2bf-113">Return value</span></span>

<span data-ttu-id="ce2bf-114">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="ce2bf-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce2bf-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce2bf-115">Requirements</span></span>



| <span data-ttu-id="ce2bf-116">需求</span><span class="sxs-lookup"><span data-stu-id="ce2bf-116">Requirement</span></span> | <span data-ttu-id="ce2bf-117">值</span><span class="sxs-lookup"><span data-stu-id="ce2bf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2bf-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce2bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2bf-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce2bf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce2bf-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce2bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2bf-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce2bf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce2bf-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ce2bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce2bf-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce2bf-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce2bf-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce2bf-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce2bf-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="ce2bf-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ce2bf-126">**RB \_ ENDDRAG**</span><span class="sxs-lookup"><span data-stu-id="ce2bf-126">**RB\_ENDDRAG**</span></span>](rb-enddrag.md)
</dt> </dl>

 

