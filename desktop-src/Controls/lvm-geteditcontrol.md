---
title: 'LVM_GETEDITCONTROL 訊息 (Commctrl .h) '
description: 取得編輯控制項的控制碼，這個控制項是用來編輯清單視圖專案的文字。 您可以明確地傳送此訊息，或使用 ListView \_ GetEditControl 宏來傳送。
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024593"
---
# <a name="lvm_geteditcontrol-message"></a><span data-ttu-id="15a21-105">LVM \_ GETEDITCONTROL 訊息</span><span class="sxs-lookup"><span data-stu-id="15a21-105">LVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="15a21-106">取得編輯控制項的控制碼，這個控制項是用來編輯清單視圖專案的文字。</span><span class="sxs-lookup"><span data-stu-id="15a21-106">Gets the handle to the edit control being used to edit a list-view item's text.</span></span> <span data-ttu-id="15a21-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="15a21-107">You can send this message explicitly or by using the [**ListView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="15a21-108">參數</span><span class="sxs-lookup"><span data-stu-id="15a21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a21-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15a21-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="15a21-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="15a21-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="15a21-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15a21-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="15a21-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="15a21-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a21-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="15a21-113">Return value</span></span>

<span data-ttu-id="15a21-114">如果成功，則傳回編輯控制項的控制碼，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="15a21-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a21-115">備註</span><span class="sxs-lookup"><span data-stu-id="15a21-115">Remarks</span></span>

<span data-ttu-id="15a21-116">當標籤編輯開始時，會建立、定位和初始化編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="15a21-116">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="15a21-117">在顯示之前，清單視圖控制項會將 [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) 通知程式碼傳送給其父視窗。</span><span class="sxs-lookup"><span data-stu-id="15a21-117">Before it is displayed, the list-view control sends its parent window an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="15a21-118">若要自訂標籤編輯，請執行 [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) 的處理常式，並讓它將 **LVM \_ GETEDITCONTROL** 訊息傳送至清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="15a21-118">To customize label editing, implement a handler for [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) and have it send an **LVM\_GETEDITCONTROL** message to the list-view control.</span></span> <span data-ttu-id="15a21-119">如果正在編輯標籤，傳回值將會是編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="15a21-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="15a21-120">您可以使用此控制碼來自訂編輯控制項，方法是傳送一般的 **EM \_ XXX** 訊息。</span><span class="sxs-lookup"><span data-stu-id="15a21-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="15a21-121">當使用者完成或取消編輯時，就會終結編輯控制項，而且控制碼不再有效。</span><span class="sxs-lookup"><span data-stu-id="15a21-121">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="15a21-122">您可以子類別化編輯控制項，但您不應該將它終結。</span><span class="sxs-lookup"><span data-stu-id="15a21-122">You can subclass the edit control, but you should not destroy it.</span></span> <span data-ttu-id="15a21-123">若要取消編輯，請將清單 view 控制項傳送至 [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) 訊息。</span><span class="sxs-lookup"><span data-stu-id="15a21-123">To cancel editing, send the list-view control a [**WM\_CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) message.</span></span>

<span data-ttu-id="15a21-124">正在編輯的清單視圖專案是目前焦點的專案，也就是處於焦點狀態的專案。</span><span class="sxs-lookup"><span data-stu-id="15a21-124">The list-view item being edited is the currently focused item that is, the item in the focused state.</span></span> <span data-ttu-id="15a21-125">若要根據專案的狀態尋找專案，請使用 [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="15a21-125">To find an item based on its state, use the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a21-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="15a21-126">Requirements</span></span>



| <span data-ttu-id="15a21-127">需求</span><span class="sxs-lookup"><span data-stu-id="15a21-127">Requirement</span></span> | <span data-ttu-id="15a21-128">值</span><span class="sxs-lookup"><span data-stu-id="15a21-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15a21-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15a21-129">Minimum supported client</span></span><br/> | <span data-ttu-id="15a21-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15a21-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15a21-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15a21-131">Minimum supported server</span></span><br/> | <span data-ttu-id="15a21-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15a21-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15a21-133">標頭</span><span class="sxs-lookup"><span data-stu-id="15a21-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="15a21-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="15a21-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a21-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15a21-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a21-136">**ListView \_ GetEditControl**</span><span class="sxs-lookup"><span data-stu-id="15a21-136">**ListView\_GetEditControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

