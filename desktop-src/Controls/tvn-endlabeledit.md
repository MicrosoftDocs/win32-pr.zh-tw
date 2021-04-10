---
title: 'TVN_ENDLABELEDIT (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，瞭解專案的標籤編輯結尾。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103901"
---
# <a name="tvn_endlabeledit-notification-code"></a><span data-ttu-id="fc85b-105">IZDEBSKI \_ ENDLABELEDIT 通知碼</span><span class="sxs-lookup"><span data-stu-id="fc85b-105">TVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="fc85b-106">通知樹狀檢視控制項的父視窗，瞭解專案的標籤編輯結尾。</span><span class="sxs-lookup"><span data-stu-id="fc85b-106">Notifies a tree-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="fc85b-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="fc85b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="fc85b-108">參數</span><span class="sxs-lookup"><span data-stu-id="fc85b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc85b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc85b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc85b-110">[**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fc85b-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="fc85b-111">此結構的 **專案** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) 結構，其 **hItem**、 **lParam** 和 **pszText** 成員包含已編輯之專案的相關有效資訊。</span><span class="sxs-lookup"><span data-stu-id="fc85b-111">The **item** member of this structure is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem**, **lParam**, and **pszText** members contain valid information about the item that was edited.</span></span> <span data-ttu-id="fc85b-112">如果已取消標籤編輯，則 **TVITEM** 結構的 **PszText** 成員為 **Null**;否則， **pszText** 是已編輯文字的位址。</span><span class="sxs-lookup"><span data-stu-id="fc85b-112">If label editing was canceled, the **pszText** member of the **TVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc85b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc85b-113">Return value</span></span>

<span data-ttu-id="fc85b-114">如果 **pszText** 成員為非 **Null**，則傳回 **TRUE** 將專案的標籤設定為已編輯的文字。</span><span class="sxs-lookup"><span data-stu-id="fc85b-114">If the **pszText** member is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="fc85b-115">傳回 **FALSE** 以拒絕編輯過的文字，並還原為原始標籤。</span><span class="sxs-lookup"><span data-stu-id="fc85b-115">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc85b-116">備註</span><span class="sxs-lookup"><span data-stu-id="fc85b-116">Remarks</span></span>

<span data-ttu-id="fc85b-117">如果 **pszText** 成員為 **Null**，則會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="fc85b-117">If the **pszText** member is **NULL**, the return value is ignored.</span></span>

<span data-ttu-id="fc85b-118">如果您 \_ 為此專案指定了 LPSTR TEXTCALLBACK 值，而 **pszText** 成員為非 **Null**，則您 \_ 的 izdebski ENDLABELEDIT 處理常式應該將文字從 **pszText** 複製到本機儲存體。</span><span class="sxs-lookup"><span data-stu-id="fc85b-118">If you specified the LPSTR\_TEXTCALLBACK value for this item and the **pszText** member is non-**NULL**, your TVN\_ENDLABELEDIT handler should copy the text from **pszText** to your local storage.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc85b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc85b-119">Requirements</span></span>



| <span data-ttu-id="fc85b-120">需求</span><span class="sxs-lookup"><span data-stu-id="fc85b-120">Requirement</span></span> | <span data-ttu-id="fc85b-121">值</span><span class="sxs-lookup"><span data-stu-id="fc85b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc85b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc85b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fc85b-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc85b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc85b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc85b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fc85b-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc85b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc85b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="fc85b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc85b-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc85b-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fc85b-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="fc85b-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fc85b-129">**Izdebski \_ENDLABELEDITW** (Unicode) 和 **izdebski \_ ENDLABELEDITA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="fc85b-129">**TVN\_ENDLABELEDITW** (Unicode) and **TVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





