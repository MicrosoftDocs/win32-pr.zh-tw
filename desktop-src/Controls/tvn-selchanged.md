---
title: 'TVN_SELCHANGED (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，選取範圍已從某個專案變更為另一個專案。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844247"
---
# <a name="tvn_selchanged-notification-code"></a><span data-ttu-id="a34f7-105">IZDEBSKI \_ SELCHANGED 通知碼</span><span class="sxs-lookup"><span data-stu-id="a34f7-105">TVN\_SELCHANGED notification code</span></span>

<span data-ttu-id="a34f7-106">通知樹狀檢視控制項的父視窗，選取範圍已從某個專案變更為另一個專案。</span><span class="sxs-lookup"><span data-stu-id="a34f7-106">Notifies a tree-view control's parent window that the selection has changed from one item to another.</span></span> <span data-ttu-id="a34f7-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a34f7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="a34f7-108">參數</span><span class="sxs-lookup"><span data-stu-id="a34f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a34f7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a34f7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a34f7-110">[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a34f7-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="a34f7-111">**NMTREEVIEW** 結構的 **itemOld** 和 **itemNew** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含先前選取之專案和新選取專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a34f7-111">The **itemOld** and **itemNew** members of the **NMTREEVIEW** structure are [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structures that contain information about the previously selected item and the newly selected item.</span></span> <span data-ttu-id="a34f7-112">只有這些結構的 **mask**、 **hItem**、 **state** 和 **lParam** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="a34f7-112">Only the **mask**, **hItem**, **state**, and **lParam** members of these structures are valid.</span></span> <span data-ttu-id="a34f7-113">在輸入時， **itemOld** 和 **itemNew** 所指定之 **TVITEM** 結構的 **stateMask** 成員是未定義的。</span><span class="sxs-lookup"><span data-stu-id="a34f7-113">The **stateMask** members of the **TVITEM** structures specified by **itemOld** and **itemNew** are undefined on input.</span></span> <span data-ttu-id="a34f7-114">**NMTREEVIEW** 結構的 **action** 成員表示導致選取專案變更的動作類型。</span><span class="sxs-lookup"><span data-stu-id="a34f7-114">The **action** member of the **NMTREEVIEW** structure indicates the type of action that caused the selection to change.</span></span> <span data-ttu-id="a34f7-115">它可能是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="a34f7-115">It can be one of the following values:</span></span>



| <span data-ttu-id="a34f7-116">需求</span><span class="sxs-lookup"><span data-stu-id="a34f7-116">Requirement</span></span> | <span data-ttu-id="a34f7-117">值</span><span class="sxs-lookup"><span data-stu-id="a34f7-117">Value</span></span> |
|-----------------|-------------------|
| <span data-ttu-id="a34f7-118">TVC \_ BYKEYBOARD</span><span class="sxs-lookup"><span data-stu-id="a34f7-118">TVC\_BYKEYBOARD</span></span> | <span data-ttu-id="a34f7-119">按鍵。</span><span class="sxs-lookup"><span data-stu-id="a34f7-119">By a keystroke.</span></span>   |
| <span data-ttu-id="a34f7-120">TVC \_ BYMOUSE</span><span class="sxs-lookup"><span data-stu-id="a34f7-120">TVC\_BYMOUSE</span></span>    | <span data-ttu-id="a34f7-121">按一下滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="a34f7-121">By a mouse click.</span></span> |
| <span data-ttu-id="a34f7-122">TVC \_ 不明</span><span class="sxs-lookup"><span data-stu-id="a34f7-122">TVC\_UNKNOWN</span></span>    | <span data-ttu-id="a34f7-123">不明。</span><span class="sxs-lookup"><span data-stu-id="a34f7-123">Unknown.</span></span>          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a34f7-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="a34f7-124">Return value</span></span>

<span data-ttu-id="a34f7-125">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a34f7-125">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a34f7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a34f7-126">Requirements</span></span>



| <span data-ttu-id="a34f7-127">需求</span><span class="sxs-lookup"><span data-stu-id="a34f7-127">Requirement</span></span> | <span data-ttu-id="a34f7-128">值</span><span class="sxs-lookup"><span data-stu-id="a34f7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a34f7-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a34f7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a34f7-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a34f7-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a34f7-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a34f7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a34f7-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a34f7-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a34f7-133">標頭</span><span class="sxs-lookup"><span data-stu-id="a34f7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a34f7-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a34f7-134"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a34f7-135">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a34f7-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a34f7-136">**Izdebski \_SELCHANGEDW** (Unicode) 和 **izdebski \_ SELCHANGEDA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a34f7-136">**TVN\_SELCHANGEDW** (Unicode) and **TVN\_SELCHANGEDA** (ANSI)</span></span><br/>             |



 

 





