---
title: 'LVN_COLUMNDROPDOWN (Commctrl 的通知碼) '
description: 當按下清單視圖的下拉式按鈕時，由清單視圖控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 752d745e-4482-425c-af3c-f9707cbb03d7
keywords:
- LVN_COLUMNDROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_COLUMNDROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792d29268548d95a7f3e70b05d9d2de368a03cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508583"
---
# <a name="lvn_columndropdown-notification-code"></a><span data-ttu-id="243f4-105">LVN \_ COLUMNDROPDOWN 通知碼</span><span class="sxs-lookup"><span data-stu-id="243f4-105">LVN\_COLUMNDROPDOWN notification code</span></span>

<span data-ttu-id="243f4-106">當按下清單視圖的下拉式按鈕時，由清單視圖控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="243f4-106">Sent by a list-view control when the list-view's drop-down button is pressed.</span></span> <span data-ttu-id="243f4-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="243f4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNDROPDOWN
        
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="243f4-108">參數</span><span class="sxs-lookup"><span data-stu-id="243f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="243f4-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="243f4-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="243f4-110">描述通知碼的 [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="243f4-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="243f4-111">呼叫端負責配置此結構，包括包含的 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構。</span><span class="sxs-lookup"><span data-stu-id="243f4-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="243f4-112">設定 **NMHDR** 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="243f4-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="243f4-113">程式 **代碼** 成員必須設定為 LVN \_ COLUMNDROPDOWN。</span><span class="sxs-lookup"><span data-stu-id="243f4-113">The **code** member must be set to LVN\_COLUMNDROPDOWN.</span></span>

<span data-ttu-id="243f4-114">將 [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的 **iItem** 成員設定為-1。</span><span class="sxs-lookup"><span data-stu-id="243f4-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="243f4-115">將 **iSubItem** 成員設定為子集合的索引。</span><span class="sxs-lookup"><span data-stu-id="243f4-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="243f4-116">將 **uNewState**、 **uOldState** 和 **lParam** 成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="243f4-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="243f4-117">不會使用 **NMLISTVIEW** 結構的其餘成員。</span><span class="sxs-lookup"><span data-stu-id="243f4-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="243f4-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="243f4-118">Return value</span></span>

<span data-ttu-id="243f4-119">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="243f4-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="243f4-120">備註</span><span class="sxs-lookup"><span data-stu-id="243f4-120">Remarks</span></span>

<span data-ttu-id="243f4-121">通知接收者會轉換 *lParam* 來取出 [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) 結構。</span><span class="sxs-lookup"><span data-stu-id="243f4-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="243f4-122">*WParam* 參數包含傳送通知碼之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="243f4-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="243f4-123">如果標題控制項是清單視圖的子系，標題控制項應該會在標題控制項收到 [HDN 的 \_ 下拉式](hdn-dropdown.md) 通知程式碼時，將這個通知程式碼傳送給清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="243f4-123">If a header control is a child of the list-view, the header control should send this notidication code to the list-view control when the header control receives the [HDN\_DROPDOWN](hdn-dropdown.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="243f4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="243f4-124">Requirements</span></span>



| <span data-ttu-id="243f4-125">需求</span><span class="sxs-lookup"><span data-stu-id="243f4-125">Requirement</span></span> | <span data-ttu-id="243f4-126">值</span><span class="sxs-lookup"><span data-stu-id="243f4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="243f4-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="243f4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="243f4-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="243f4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="243f4-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="243f4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="243f4-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="243f4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="243f4-131">標頭</span><span class="sxs-lookup"><span data-stu-id="243f4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="243f4-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="243f4-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





