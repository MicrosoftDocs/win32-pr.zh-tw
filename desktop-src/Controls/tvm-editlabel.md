---
title: 'TVM_EDITLABEL 訊息 (Commctrl .h) '
description: 開始編輯指定專案的文字，並將專案的文字取代為包含文字的單行編輯控制項。
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- TVM_EDITLABEL message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934190"
---
# <a name="tvm_editlabel-message"></a><span data-ttu-id="0e1d9-104">TVM \_ EDITLABEL 訊息</span><span class="sxs-lookup"><span data-stu-id="0e1d9-104">TVM\_EDITLABEL message</span></span>

<span data-ttu-id="0e1d9-105">開始編輯指定專案的文字，並將專案的文字取代為包含文字的單行編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-105">Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text.</span></span> <span data-ttu-id="0e1d9-106">此訊息會隱含地選取並將焦點放在指定的專案。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-106">This message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="0e1d9-107">您可以使用 [**TreeView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-107">You can send this message explicitly or by using the [**TreeView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e1d9-108">參數</span><span class="sxs-lookup"><span data-stu-id="0e1d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e1d9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e1d9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0e1d9-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0e1d9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e1d9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e1d9-112">要編輯之專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-112">Handle to the item to edit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e1d9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e1d9-113">Return value</span></span>

<span data-ttu-id="0e1d9-114">如果成功，則傳回編輯控制項所用的編輯控制項的控制碼，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-114">Returns the handle to the edit control used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e1d9-115">備註</span><span class="sxs-lookup"><span data-stu-id="0e1d9-115">Remarks</span></span>

<span data-ttu-id="0e1d9-116">此訊息會將 [izdebski \_ BEGINLABELEDIT](tvn-beginlabeledit.md) 通知程式碼傳送至樹狀檢視控制項的父代。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-116">This message sends a [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code to the parent of the tree-view control.</span></span>

<span data-ttu-id="0e1d9-117">當使用者完成或取消編輯時，就會終結編輯控制項，而且控制碼不再有效。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-117">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="0e1d9-118">您可以子類別化編輯控制項，但不要終結它。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-118">You can subclass the edit control, but do not destroy it.</span></span>

<span data-ttu-id="0e1d9-119">當您將此訊息傳送至控制項之前，控制項必須具有焦點。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-119">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="0e1d9-120">您可以使用 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數來設定焦點。</span><span class="sxs-lookup"><span data-stu-id="0e1d9-120">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e1d9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e1d9-121">Requirements</span></span>



| <span data-ttu-id="0e1d9-122">需求</span><span class="sxs-lookup"><span data-stu-id="0e1d9-122">Requirement</span></span> | <span data-ttu-id="0e1d9-123">值</span><span class="sxs-lookup"><span data-stu-id="0e1d9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e1d9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e1d9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0e1d9-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e1d9-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e1d9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e1d9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0e1d9-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e1d9-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e1d9-128">標頭</span><span class="sxs-lookup"><span data-stu-id="0e1d9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e1d9-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e1d9-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0e1d9-130">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="0e1d9-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e1d9-131">**TVM \_EDITLABELW** (Unicode) 和 **TVM \_ EDITLABELA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="0e1d9-131">**TVM\_EDITLABELW** (Unicode) and **TVM\_EDITLABELA** (ANSI)</span></span><br/>               |



 

