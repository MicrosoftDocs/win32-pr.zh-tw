---
title: 'TVN_BEGINLABELEDIT (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，瞭解專案的標籤編輯開始。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966315"
---
# <a name="tvn_beginlabeledit-notification-code"></a><span data-ttu-id="bb1b5-105">IZDEBSKI \_ BEGINLABELEDIT 通知碼</span><span class="sxs-lookup"><span data-stu-id="bb1b5-105">TVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="bb1b5-106">通知樹狀檢視控制項的父視窗，瞭解專案的標籤編輯開始。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-106">Notifies a tree-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="bb1b5-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="bb1b5-108">參數</span><span class="sxs-lookup"><span data-stu-id="bb1b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb1b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb1b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb1b5-110">[**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="bb1b5-111">**專案** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含在 **hItem**、 **state**、 **lParam** 和 **pszText** 成員中編輯之專案的相關有效資訊。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being edited in the **hItem**, **state**, **lParam**, and **pszText** members.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb1b5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb1b5-112">Return value</span></span>

<span data-ttu-id="bb1b5-113">傳回 **TRUE** 表示取消標籤編輯。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-113">Returns **TRUE** to cancel label editing.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb1b5-114">備註</span><span class="sxs-lookup"><span data-stu-id="bb1b5-114">Remarks</span></span>

<span data-ttu-id="bb1b5-115">當標籤編輯開始時，會建立編輯控制項，但不會放置或顯示該控制項。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-115">When label editing begins, an edit control is created but not positioned or displayed.</span></span> <span data-ttu-id="bb1b5-116">在顯示之前，樹狀檢視控制項會將 IZDEBSKI BEGINLABELEDIT 通知程式碼傳送至其父視窗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-116">Before it is displayed, the tree-view control sends its parent window a TVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="bb1b5-117">若要自訂標籤編輯，請執行 IZDEBSKI BEGINLABELEDIT 的處理常式， \_ 並讓它將 [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) 訊息傳送至樹狀檢視控制項。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-117">To customize label editing, implement a handler for TVN\_BEGINLABELEDIT and have it send a [**TVM\_GETEDITCONTROL**](tvm-geteditcontrol.md) message to the tree-view control.</span></span> <span data-ttu-id="bb1b5-118">如果正在編輯標籤，傳回值將會是編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-118">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="bb1b5-119">您可以使用此控制碼來自訂編輯控制項，方法是傳送一般的 EM \_ XXX 訊息。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-119">Use this handle to customize the edit control by sending the usual EM\_XXX messages.</span></span>

<span data-ttu-id="bb1b5-120">當使用者取消或完成編輯時，父視窗會收到 [izdebski \_ ENDLABELEDIT](tvn-endlabeledit.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="bb1b5-120">When the user cancels or completes the editing, the parent window receives a [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb1b5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb1b5-121">Requirements</span></span>



| <span data-ttu-id="bb1b5-122">需求</span><span class="sxs-lookup"><span data-stu-id="bb1b5-122">Requirement</span></span> | <span data-ttu-id="bb1b5-123">值</span><span class="sxs-lookup"><span data-stu-id="bb1b5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1b5-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb1b5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bb1b5-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb1b5-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb1b5-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb1b5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bb1b5-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb1b5-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb1b5-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bb1b5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb1b5-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b5-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bb1b5-130">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="bb1b5-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bb1b5-131">**Izdebski \_BEGINLABELEDITW** (Unicode) 和 **izdebski \_ BEGINLABELEDITA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="bb1b5-131">**TVN\_BEGINLABELEDITW** (Unicode) and **TVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





