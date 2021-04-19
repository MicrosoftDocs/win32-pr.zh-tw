---
title: 'LVN_INCREMENTALSEARCH (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，累加式搜尋已開始。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967774"
---
# <a name="lvn_incrementalsearch-notification-code"></a><span data-ttu-id="a674d-105">LVN \_ INCREMENTALSEARCH 通知碼</span><span class="sxs-lookup"><span data-stu-id="a674d-105">LVN\_INCREMENTALSEARCH notification code</span></span>

<span data-ttu-id="a674d-106">通知清單視圖控制項的父視窗，累加式搜尋已開始。</span><span class="sxs-lookup"><span data-stu-id="a674d-106">Notifies a list-view control's parent window that an incremental search has started.</span></span> <span data-ttu-id="a674d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a674d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a674d-108">參數</span><span class="sxs-lookup"><span data-stu-id="a674d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a674d-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a674d-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a674d-110">描述通知碼的 [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="a674d-110">Pointer to a [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that describes the notification code.</span></span> <span data-ttu-id="a674d-111">呼叫端負責配置此結構，包括包含的 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 和 [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) 結構。</span><span class="sxs-lookup"><span data-stu-id="a674d-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) and [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structures.</span></span> <span data-ttu-id="a674d-112">設定 **NMHDR** 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="a674d-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="a674d-113">程式 **代碼** 成員必須設定為 LVN \_ INCREMENTALSEARCH。</span><span class="sxs-lookup"><span data-stu-id="a674d-113">The **code** member must be set to LVN\_INCREMENTALSEARCH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a674d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a674d-114">Return value</span></span>

<span data-ttu-id="a674d-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="a674d-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a674d-116">備註</span><span class="sxs-lookup"><span data-stu-id="a674d-116">Remarks</span></span>

<span data-ttu-id="a674d-117">通知接收者會轉換 *lParam* 來取出 [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) 結構。</span><span class="sxs-lookup"><span data-stu-id="a674d-117">The notification receiver casts *lParam* to retrieve the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span> <span data-ttu-id="a674d-118">*WParam* 參數包含傳送此通知碼之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a674d-118">The *wParam* parameter contains the ID of the control that sends this notification code.</span></span>

<span data-ttu-id="a674d-119">此通知碼會提供應用程式 (或通知接收器) 自訂增量搜尋的機會。</span><span class="sxs-lookup"><span data-stu-id="a674d-119">This notification code gives an application (or the notification receiver) the opportunity to customize an incremental search.</span></span> <span data-ttu-id="a674d-120">例如，如果搜尋專案是數值，則應用程式可以執行數值搜尋，而不是字串搜尋。</span><span class="sxs-lookup"><span data-stu-id="a674d-120">For example, if the search items are numeric, the application can perform a numerical search instead of a string search.</span></span>

<span data-ttu-id="a674d-121">應用程式會將 [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema)結構中所包含之 [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa)結構的 **lParam** 成員設定為搜尋結果，或設定為另一個應用程式定義的值，以使搜尋失敗，並向控制項指出如何繼續進行。</span><span class="sxs-lookup"><span data-stu-id="a674d-121">The application sets the **lParam** member of the [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure contained in [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure  to the result of the search, or to another application defined value to fail the search and indicate to the control how to proceed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a674d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a674d-122">Requirements</span></span>



| <span data-ttu-id="a674d-123">需求</span><span class="sxs-lookup"><span data-stu-id="a674d-123">Requirement</span></span> | <span data-ttu-id="a674d-124">值</span><span class="sxs-lookup"><span data-stu-id="a674d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a674d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a674d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a674d-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a674d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a674d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a674d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a674d-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a674d-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a674d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a674d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a674d-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a674d-130"><dt>Commctrl.h</dt></span></span> </dl>   |
| <span data-ttu-id="a674d-131">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a674d-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a674d-132">**LVN \_INCREMENTALSEARCHW** (Unicode) 和 **LVN \_ INCREMENTALSEARCHA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a674d-132">**LVN\_INCREMENTALSEARCHW** (Unicode) and **LVN\_INCREMENTALSEARCHA** (ANSI)</span></span><br/> |



 

 





