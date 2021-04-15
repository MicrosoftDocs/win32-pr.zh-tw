---
title: 'TVM_ENDEDITLABELNOW 訊息 (Commctrl .h) '
description: 結束編輯樹狀檢視專案的標籤。 您可以使用 TreeView EndEditLabelNow 宏明確地傳送此訊息 \_ 。
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508448"
---
# <a name="tvm_endeditlabelnow-message"></a><span data-ttu-id="445a7-105">TVM \_ ENDEDITLABELNOW 訊息</span><span class="sxs-lookup"><span data-stu-id="445a7-105">TVM\_ENDEDITLABELNOW message</span></span>

<span data-ttu-id="445a7-106">結束編輯樹狀檢視專案的標籤。</span><span class="sxs-lookup"><span data-stu-id="445a7-106">Ends the editing of a tree-view item's label.</span></span> <span data-ttu-id="445a7-107">您可以使用 [**TreeView \_ EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="445a7-107">You can send this message explicitly or by using the [**TreeView\_EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="445a7-108">參數</span><span class="sxs-lookup"><span data-stu-id="445a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="445a7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="445a7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="445a7-110">變數，指出編輯是否取消，而不儲存至標籤。</span><span class="sxs-lookup"><span data-stu-id="445a7-110">Variable that indicates whether the editing is canceled without being saved to the label.</span></span> <span data-ttu-id="445a7-111">如果此參數為 **TRUE**，系統就會取消編輯，而不儲存變更。</span><span class="sxs-lookup"><span data-stu-id="445a7-111">If this parameter is **TRUE**, the system cancels editing without saving the changes.</span></span> <span data-ttu-id="445a7-112">否則，系統會將變更儲存至標籤。</span><span class="sxs-lookup"><span data-stu-id="445a7-112">Otherwise, the system saves the changes to the label.</span></span>

</dd> <dt>

<span data-ttu-id="445a7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="445a7-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="445a7-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="445a7-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="445a7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="445a7-115">Return value</span></span>

<span data-ttu-id="445a7-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="445a7-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="445a7-117">備註</span><span class="sxs-lookup"><span data-stu-id="445a7-117">Remarks</span></span>

<span data-ttu-id="445a7-118">此訊息會使 [izdebski \_ ENDLABELEDIT](tvn-endlabeledit.md) 通知程式碼傳送至樹狀檢視控制項的父視窗。</span><span class="sxs-lookup"><span data-stu-id="445a7-118">This message causes the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code to be sent to the parent window of the tree-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="445a7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="445a7-119">Requirements</span></span>



| <span data-ttu-id="445a7-120">需求</span><span class="sxs-lookup"><span data-stu-id="445a7-120">Requirement</span></span> | <span data-ttu-id="445a7-121">值</span><span class="sxs-lookup"><span data-stu-id="445a7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="445a7-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="445a7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="445a7-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="445a7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="445a7-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="445a7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="445a7-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="445a7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="445a7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="445a7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="445a7-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="445a7-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





