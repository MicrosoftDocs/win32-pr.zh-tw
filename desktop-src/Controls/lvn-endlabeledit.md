---
title: 'LVN_ENDLABELEDIT (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，瞭解專案的標籤編輯結尾。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- LVN_ENDLABELEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965540"
---
# <a name="lvn_endlabeledit-notification-code"></a><span data-ttu-id="2e223-105">LVN \_ ENDLABELEDIT 通知碼</span><span class="sxs-lookup"><span data-stu-id="2e223-105">LVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="2e223-106">通知清單視圖控制項的父視窗，瞭解專案的標籤編輯結尾。</span><span class="sxs-lookup"><span data-stu-id="2e223-106">Notifies a list-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="2e223-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="2e223-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2e223-108">參數</span><span class="sxs-lookup"><span data-stu-id="2e223-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e223-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e223-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e223-110">[**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2e223-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="2e223-111">此結構的 **專案** 成員是 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構，其 **iItem** 成員會識別正在編輯的專案。</span><span class="sxs-lookup"><span data-stu-id="2e223-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="2e223-112">當傳送 LVN ENDLABELEDIT 通知碼時，**專案** 的 **pszText** 成員會包含有效的值 \_ ，不論 LVIF \_ 文字旗標是否在 **LVITEM** 結構的 **mask** 成員中設定。</span><span class="sxs-lookup"><span data-stu-id="2e223-112">The **pszText** member of **item** contains a valid value when the LVN\_ENDLABELEDIT notification code is sent, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of the **LVITEM** structure.</span></span> <span data-ttu-id="2e223-113">如果使用者取消編輯， **LVITEM** 結構的 **pszText** 成員會是 **Null**;否則， **pszText** 是已編輯文字的位址。</span><span class="sxs-lookup"><span data-stu-id="2e223-113">If the user cancels editing, the **pszText** member of the **LVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e223-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e223-114">Return value</span></span>

<span data-ttu-id="2e223-115">如果 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **pszText** 成員為非 **Null**，則傳回 **TRUE** 將專案的標籤設定為已編輯的文字。</span><span class="sxs-lookup"><span data-stu-id="2e223-115">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="2e223-116">傳回 **FALSE** 以拒絕編輯過的文字，並還原為原始標籤。</span><span class="sxs-lookup"><span data-stu-id="2e223-116">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

<span data-ttu-id="2e223-117">如果 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **PszText** 成員是 **Null**，則會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="2e223-117">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is **NULL**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e223-118">備註</span><span class="sxs-lookup"><span data-stu-id="2e223-118">Remarks</span></span>

<span data-ttu-id="2e223-119">對話程式的傳回值就是是否已處理訊息。</span><span class="sxs-lookup"><span data-stu-id="2e223-119">The return value of the dialog procedure is whether the message was handled.</span></span> <span data-ttu-id="2e223-120">第二個傳回值必須藉由使用 **DWLP_MSGRESULT** 呼叫 [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)來設定。</span><span class="sxs-lookup"><span data-stu-id="2e223-120">The second return value must be set by calling [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) with **DWLP_MSGRESULT**.</span></span>

<span data-ttu-id="2e223-121">當使用者開始編輯專案標籤時，清單視圖控制項的父視窗會收到 [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="2e223-121">When the user begins editing an item label, the parent window of the list-view control receives an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span> <span data-ttu-id="2e223-122">當使用者取消或完成編輯時，父視窗會收到 LVN \_ ENDLABELEDIT 通知碼。</span><span class="sxs-lookup"><span data-stu-id="2e223-122">When the user cancels or completes the editing, the parent window receives an LVN\_ENDLABELEDIT notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e223-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e223-123">Requirements</span></span>



| <span data-ttu-id="2e223-124">需求</span><span class="sxs-lookup"><span data-stu-id="2e223-124">Requirement</span></span> | <span data-ttu-id="2e223-125">值</span><span class="sxs-lookup"><span data-stu-id="2e223-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e223-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e223-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2e223-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e223-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e223-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e223-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2e223-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e223-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e223-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2e223-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e223-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e223-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2e223-132">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="2e223-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2e223-133">**LVN \_ENDLABELEDITW** (Unicode) 和 **LVN \_ ENDLABELEDITA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="2e223-133">**LVN\_ENDLABELEDITW** (Unicode) and **LVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





