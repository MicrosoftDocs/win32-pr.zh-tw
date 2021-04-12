---
title: 'TVM_GETEDITCONTROL 訊息 (Commctrl .h) '
description: 抓取編輯控制項的控制碼，這個控制項是用來編輯樹狀檢視專案的文字。 您可以使用 TreeView GetEditControl 宏明確地傳送此訊息 \_ 。
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- TVM_GETEDITCONTROL message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105960"
---
# <a name="tvm_geteditcontrol-message"></a><span data-ttu-id="91d92-105">TVM \_ GETEDITCONTROL 訊息</span><span class="sxs-lookup"><span data-stu-id="91d92-105">TVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="91d92-106">抓取編輯控制項的控制碼，這個控制項是用來編輯樹狀檢視專案的文字。</span><span class="sxs-lookup"><span data-stu-id="91d92-106">Retrieves the handle to the edit control being used to edit a tree-view item's text.</span></span> <span data-ttu-id="91d92-107">您可以使用 [**TreeView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="91d92-107">You can send this message explicitly or by using the [**TreeView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="91d92-108">參數</span><span class="sxs-lookup"><span data-stu-id="91d92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d92-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91d92-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="91d92-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="91d92-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="91d92-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91d92-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="91d92-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="91d92-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91d92-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="91d92-113">Return value</span></span>

<span data-ttu-id="91d92-114">如果成功，則傳回編輯控制項的控制碼，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="91d92-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d92-115">備註</span><span class="sxs-lookup"><span data-stu-id="91d92-115">Remarks</span></span>

<span data-ttu-id="91d92-116">當標籤編輯開始時，會建立編輯控制項，但不會定位或顯示。</span><span class="sxs-lookup"><span data-stu-id="91d92-116">When label editing begins, an edit control is created, but not positioned or displayed.</span></span> <span data-ttu-id="91d92-117">在顯示之前，樹狀檢視控制項會將 [izdebski \_ BEGINLABELEDIT](tvn-beginlabeledit.md) 通知程式碼傳送給其父視窗。</span><span class="sxs-lookup"><span data-stu-id="91d92-117">Before it is displayed, the tree-view control sends its parent window an [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="91d92-118">若要自訂標籤編輯，請執行 [izdebski \_ BEGINLABELEDIT](tvn-beginlabeledit.md) 的處理常式，並讓它將 **TVM \_ GETEDITCONTROL** 訊息傳送至樹狀檢視控制項。</span><span class="sxs-lookup"><span data-stu-id="91d92-118">To customize label editing, implement a handler for [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) and have it send a **TVM\_GETEDITCONTROL** message to the tree-view control.</span></span> <span data-ttu-id="91d92-119">如果正在編輯標籤，傳回值將會是編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="91d92-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="91d92-120">您可以使用此控制碼來自訂編輯控制項，方法是傳送一般的 **EM \_ XXX** 訊息。</span><span class="sxs-lookup"><span data-stu-id="91d92-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="91d92-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="91d92-121">Requirements</span></span>



| <span data-ttu-id="91d92-122">需求</span><span class="sxs-lookup"><span data-stu-id="91d92-122">Requirement</span></span> | <span data-ttu-id="91d92-123">值</span><span class="sxs-lookup"><span data-stu-id="91d92-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91d92-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91d92-124">Minimum supported client</span></span><br/> | <span data-ttu-id="91d92-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91d92-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91d92-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91d92-126">Minimum supported server</span></span><br/> | <span data-ttu-id="91d92-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91d92-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91d92-128">標頭</span><span class="sxs-lookup"><span data-stu-id="91d92-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d92-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="91d92-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





