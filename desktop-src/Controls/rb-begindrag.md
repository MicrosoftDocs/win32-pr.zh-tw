---
title: 'RB_BEGINDRAG 訊息 (Commctrl .h) '
description: 將 Rebar 控制項放在拖放模式中。 此訊息不會造成 RBN \_ BEGINDRAG 通知傳送。
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- RB_BEGINDRAG message Windows 控制項
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466089"
---
# <a name="rb_begindrag-message"></a><span data-ttu-id="44cc5-105">RB \_ BEGINDRAG 訊息</span><span class="sxs-lookup"><span data-stu-id="44cc5-105">RB\_BEGINDRAG message</span></span>

<span data-ttu-id="44cc5-106">將 Rebar 控制項放在拖放模式中。</span><span class="sxs-lookup"><span data-stu-id="44cc5-106">Puts the rebar control in drag-and-drop mode.</span></span> <span data-ttu-id="44cc5-107">此訊息不會造成 [RBN \_ BEGINDRAG](rbn-begindrag.md) 通知傳送。</span><span class="sxs-lookup"><span data-stu-id="44cc5-107">This message does not cause a [RBN\_BEGINDRAG](rbn-begindrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="44cc5-108">參數</span><span class="sxs-lookup"><span data-stu-id="44cc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44cc5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44cc5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44cc5-110">以零為基底的索引，此為拖放作業會影響的頻外索引。</span><span class="sxs-lookup"><span data-stu-id="44cc5-110">Zero-based index of the band that the drag-and-drop operation will affect.</span></span>

</dd> <dt>

<span data-ttu-id="44cc5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44cc5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44cc5-112">包含開始滑鼠座標的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="44cc5-112">**DWORD** value that contains the starting mouse coordinates.</span></span> <span data-ttu-id="44cc5-113">水準座標是包含在 LOWORD 中，而垂直座標則是包含在 HIWORD 中。</span><span class="sxs-lookup"><span data-stu-id="44cc5-113">The horizontal coordinate is contained in the LOWORD and the vertical coordinate is contained in the HIWORD.</span></span> <span data-ttu-id="44cc5-114">如果您傳遞 (**DWORD**) -1，Rebar 控制項將會使用滑鼠的位置，這是上一次控制項的執行緒，稱為 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)。</span><span class="sxs-lookup"><span data-stu-id="44cc5-114">If you pass (**DWORD**)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44cc5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="44cc5-115">Return value</span></span>

<span data-ttu-id="44cc5-116">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="44cc5-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="44cc5-117">備註</span><span class="sxs-lookup"><span data-stu-id="44cc5-117">Remarks</span></span>

<span data-ttu-id="44cc5-118">**Rb \_ BEGINDRAG**、 [**rb \_ DRAGMOVE**](rb-dragmove.md)和 [**rb \_ ENDDRAG**](rb-enddrag.md)訊息可讓您針對 Rebar 控制項執行 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget)介面。</span><span class="sxs-lookup"><span data-stu-id="44cc5-118">The **RB\_BEGINDRAG**, [**RB\_DRAGMOVE**](rb-dragmove.md), and [**RB\_ENDDRAG**](rb-enddrag.md) messages allow you to implement an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface for a rebar control.</span></span> <span data-ttu-id="44cc5-119">您會傳送 **rb \_ BEGINDRAG** 訊息以回應 [**IDropTarget：:D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter)、傳送 **rb \_ DRAGMOVE** 訊息以回應 [**IDropTarget：:D Ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)，並傳送 **rb \_ ENDDRAG** 訊息以回應 [**IDropTarget：:D rop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) 和 [**IDropTarget：:D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave)。</span><span class="sxs-lookup"><span data-stu-id="44cc5-119">You send the **RB\_BEGINDRAG** message in response to [**IDropTarget::DragEnter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), send the **RB\_DRAGMOVE** message in response to [**IDropTarget::DragOver**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover), and the **RB\_ENDDRAG** message in response to [**IDropTarget::Drop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) and [**IDropTarget::DragLeave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span></span>

## <a name="requirements"></a><span data-ttu-id="44cc5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="44cc5-120">Requirements</span></span>



| <span data-ttu-id="44cc5-121">需求</span><span class="sxs-lookup"><span data-stu-id="44cc5-121">Requirement</span></span> | <span data-ttu-id="44cc5-122">值</span><span class="sxs-lookup"><span data-stu-id="44cc5-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44cc5-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44cc5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="44cc5-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44cc5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44cc5-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44cc5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="44cc5-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44cc5-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44cc5-127">標頭</span><span class="sxs-lookup"><span data-stu-id="44cc5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="44cc5-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="44cc5-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

