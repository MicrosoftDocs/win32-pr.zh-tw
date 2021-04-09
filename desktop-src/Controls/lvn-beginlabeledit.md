---
title: 'LVN_BEGINLABELEDIT (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，瞭解專案的標籤編輯開始。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933958"
---
# <a name="lvn_beginlabeledit-notification-code"></a><span data-ttu-id="129ad-105">LVN \_ BEGINLABELEDIT 通知碼</span><span class="sxs-lookup"><span data-stu-id="129ad-105">LVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="129ad-106">通知清單視圖控制項的父視窗，瞭解專案的標籤編輯開始。</span><span class="sxs-lookup"><span data-stu-id="129ad-106">Notifies a list-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="129ad-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="129ad-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="129ad-108">參數</span><span class="sxs-lookup"><span data-stu-id="129ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="129ad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="129ad-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="129ad-110">[**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="129ad-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="129ad-111">此結構的 **專案** 成員是 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構，其 **iItem** 成員會識別正在編輯的專案。</span><span class="sxs-lookup"><span data-stu-id="129ad-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="129ad-112">請注意，子無法編輯。 **iSubItem** 成員一律設定為零。</span><span class="sxs-lookup"><span data-stu-id="129ad-112">Note that subitems cannot be edited; the **iSubItem** member is always set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="129ad-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="129ad-113">Return value</span></span>

<span data-ttu-id="129ad-114">若要允許使用者編輯標籤，請傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="129ad-114">To allow the user to edit the label, return **FALSE**.</span></span>

<span data-ttu-id="129ad-115">若要防止使用者編輯標籤，請傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="129ad-115">To prevent the user from editing the label, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="129ad-116">備註</span><span class="sxs-lookup"><span data-stu-id="129ad-116">Remarks</span></span>

<span data-ttu-id="129ad-117">當標籤編輯開始時，會建立、定位和初始化編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="129ad-117">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="129ad-118">在顯示之前，清單視圖控制項會將 LVN BEGINLABELEDIT 通知程式碼傳送給其父視窗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="129ad-118">Before it is displayed, the list-view control sends its parent window an LVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="129ad-119">若要自訂標籤編輯，請執行 LVN BEGINLABELEDIT 的處理常式， \_ 並讓它將 [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) 訊息傳送至清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="129ad-119">To customize label editing, implement a handler for LVN\_BEGINLABELEDIT and have it send an [**LVM\_GETEDITCONTROL**](lvm-geteditcontrol.md) message to the list-view control.</span></span> <span data-ttu-id="129ad-120">如果正在編輯標籤，傳回值將會是編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="129ad-120">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="129ad-121">您可以使用此控制碼來自訂編輯控制項，方法是傳送一般的 **EM \_ XXX** 訊息。</span><span class="sxs-lookup"><span data-stu-id="129ad-121">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="129ad-122">當使用者取消或完成編輯時，父視窗會收到 [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="129ad-122">When the user cancels or completes the editing, the parent window receives an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="129ad-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="129ad-123">Requirements</span></span>



| <span data-ttu-id="129ad-124">需求</span><span class="sxs-lookup"><span data-stu-id="129ad-124">Requirement</span></span> | <span data-ttu-id="129ad-125">值</span><span class="sxs-lookup"><span data-stu-id="129ad-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="129ad-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="129ad-126">Minimum supported client</span></span><br/> | <span data-ttu-id="129ad-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="129ad-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="129ad-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="129ad-128">Minimum supported server</span></span><br/> | <span data-ttu-id="129ad-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="129ad-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="129ad-130">標頭</span><span class="sxs-lookup"><span data-stu-id="129ad-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="129ad-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="129ad-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="129ad-132">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="129ad-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="129ad-133">**LVN \_BEGINLABELEDITW** (Unicode) 和 **LVN \_ BEGINLABELEDITA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="129ad-133">**LVN\_BEGINLABELEDITW** (Unicode) and **LVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





