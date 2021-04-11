---
title: 'LVN_SETDISPINFO (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，它必須更新它為專案維護的資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934728"
---
# <a name="lvn_setdispinfo-notification-code"></a><span data-ttu-id="00650-105">LVN \_ SETDISPINFO 通知碼</span><span class="sxs-lookup"><span data-stu-id="00650-105">LVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="00650-106">通知清單視圖控制項的父視窗，它必須更新它為專案維護的資訊。</span><span class="sxs-lookup"><span data-stu-id="00650-106">Notifies a list-view control's parent window that it must update the information it maintains for an item.</span></span> <span data-ttu-id="00650-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="00650-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="00650-108">參數</span><span class="sxs-lookup"><span data-stu-id="00650-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00650-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00650-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00650-110">[**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)結構的指標，指定已變更之專案的資訊。</span><span class="sxs-lookup"><span data-stu-id="00650-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure that specifies information for the changed item.</span></span> <span data-ttu-id="00650-111">此結構的 **專案** 成員是 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構，其中包含已變更之專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="00650-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains information about the item that was changed.</span></span> <span data-ttu-id="00650-112">**專案** 的 **pszText** 成員包含有效的值，不論是否在 \_ 此結構的 **遮罩** 成員中設定 LVIF 文字旗標。</span><span class="sxs-lookup"><span data-stu-id="00650-112">The **pszText** member of **item** contains a valid value, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00650-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="00650-113">Return value</span></span>

<span data-ttu-id="00650-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="00650-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00650-115">備註</span><span class="sxs-lookup"><span data-stu-id="00650-115">Remarks</span></span>

<span data-ttu-id="00650-116">通知接收者會轉換 *lParam* 來取出 [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) 結構。</span><span class="sxs-lookup"><span data-stu-id="00650-116">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="00650-117">*WParam* 參數包含訊息碼。</span><span class="sxs-lookup"><span data-stu-id="00650-117">The *wParam* parameter contains the message code.</span></span>

## <a name="requirements"></a><span data-ttu-id="00650-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="00650-118">Requirements</span></span>



| <span data-ttu-id="00650-119">需求</span><span class="sxs-lookup"><span data-stu-id="00650-119">Requirement</span></span> | <span data-ttu-id="00650-120">值</span><span class="sxs-lookup"><span data-stu-id="00650-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00650-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00650-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00650-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00650-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00650-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00650-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00650-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00650-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00650-125">標頭</span><span class="sxs-lookup"><span data-stu-id="00650-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00650-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="00650-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="00650-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="00650-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="00650-128">**LVN \_SETDISPINFOW** (Unicode) 和 **LVN \_ SETDISPINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="00650-128">**LVN\_SETDISPINFOW** (Unicode) and **LVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="00650-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00650-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00650-130">LVN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="00650-130">LVN\_GETDISPINFO</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





