---
title: 'LVM_EDITLABEL 訊息 (Commctrl .h) '
description: 開始就地編輯指定清單視圖專案的文字。 訊息會隱含地選取並將焦點放在指定的專案。 您可以明確地傳送此訊息，或使用 ListView \_ EditLabel 宏來傳送。
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- LVM_EDITLABEL message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685524"
---
# <a name="lvm_editlabel-message"></a><span data-ttu-id="39abf-106">LVM \_ EDITLABEL 訊息</span><span class="sxs-lookup"><span data-stu-id="39abf-106">LVM\_EDITLABEL message</span></span>

<span data-ttu-id="39abf-107">開始就地編輯指定清單視圖專案的文字。</span><span class="sxs-lookup"><span data-stu-id="39abf-107">Begins in-place editing of the specified list-view item's text.</span></span> <span data-ttu-id="39abf-108">訊息會隱含地選取並將焦點放在指定的專案。</span><span class="sxs-lookup"><span data-stu-id="39abf-108">The message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="39abf-109">您可以明確地傳送此訊息，或使用 [**ListView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="39abf-109">You can send this message explicitly or by using the [**ListView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="39abf-110">參數</span><span class="sxs-lookup"><span data-stu-id="39abf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39abf-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39abf-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39abf-112">清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="39abf-112">The index of the list-view item.</span></span> <span data-ttu-id="39abf-113">若要取消編輯，請將索引設定為-1。</span><span class="sxs-lookup"><span data-stu-id="39abf-113">To cancel editing, set the index to -1.</span></span>

</dd> <dt>

<span data-ttu-id="39abf-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39abf-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="39abf-115">必須為零。</span><span class="sxs-lookup"><span data-stu-id="39abf-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39abf-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="39abf-116">Return value</span></span>

<span data-ttu-id="39abf-117">傳回編輯控制項的控制碼，如果成功，則會用來編輯專案文字，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="39abf-117">Returns the handle to the edit control that is used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="39abf-118">備註</span><span class="sxs-lookup"><span data-stu-id="39abf-118">Remarks</span></span>

<span data-ttu-id="39abf-119">當使用者完成或取消編輯時，就會終結編輯控制項，而且控制碼不再有效。</span><span class="sxs-lookup"><span data-stu-id="39abf-119">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="39abf-120">您可以子類別化編輯控制項，但您不應該將它終結。</span><span class="sxs-lookup"><span data-stu-id="39abf-120">You can subclass the edit control, but you should not destroy it.</span></span>

<span data-ttu-id="39abf-121">當您將此訊息傳送至控制項之前，控制項必須具有焦點。</span><span class="sxs-lookup"><span data-stu-id="39abf-121">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="39abf-122">您可以使用 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數來設定焦點。</span><span class="sxs-lookup"><span data-stu-id="39abf-122">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

<span data-ttu-id="39abf-123">如果 *wParam* 為-1，則會傳送 [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="39abf-123">If *wParam* is -1, an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="39abf-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="39abf-124">Requirements</span></span>



| <span data-ttu-id="39abf-125">需求</span><span class="sxs-lookup"><span data-stu-id="39abf-125">Requirement</span></span> | <span data-ttu-id="39abf-126">值</span><span class="sxs-lookup"><span data-stu-id="39abf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39abf-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39abf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="39abf-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39abf-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39abf-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39abf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="39abf-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39abf-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39abf-131">標頭</span><span class="sxs-lookup"><span data-stu-id="39abf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="39abf-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="39abf-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="39abf-133">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="39abf-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="39abf-134">**LVM \_EDITLABELW** (Unicode) 和 **LVM \_ EDITLABELA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="39abf-134">**LVM\_EDITLABELW** (Unicode) and **LVM\_EDITLABELA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="39abf-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39abf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39abf-136">**WM \_ CANCELMODE**</span><span class="sxs-lookup"><span data-stu-id="39abf-136">**WM\_CANCELMODE**</span></span>](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

