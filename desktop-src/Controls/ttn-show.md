---
title: 'TTN_SHOW (Commctrl 的通知碼) '
description: 通知擁有者視窗即將顯示工具提示控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934444"
---
# <a name="ttn_show-notification-code"></a><span data-ttu-id="9eb7b-105">TTN \_ 顯示通知碼</span><span class="sxs-lookup"><span data-stu-id="9eb7b-105">TTN\_SHOW notification code</span></span>

<span data-ttu-id="9eb7b-106">通知擁有者視窗即將顯示工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="9eb7b-106">Notifies the owner window that a tooltip control is about to be displayed.</span></span> <span data-ttu-id="9eb7b-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="9eb7b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9eb7b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9eb7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9eb7b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb7b-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9eb7b-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb7b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9eb7b-111">Return value</span></span>

<span data-ttu-id="9eb7b-112">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="9eb7b-112">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="9eb7b-113">若要將工具提示顯示在其預設位置，請傳回零。</span><span class="sxs-lookup"><span data-stu-id="9eb7b-113">To display the tooltip in its default location, return zero.</span></span> <span data-ttu-id="9eb7b-114">若要自訂工具提示位置，請使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函式重新置放工具提示視窗，並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9eb7b-114">To customize the tooltip position, reposition the tooltip window with the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function and return **TRUE**.</span></span>

> [!Note]  
> <span data-ttu-id="9eb7b-115">若為4.70 之前的版本，則不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9eb7b-115">For versions earlier than 4.70, there is no return value.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="9eb7b-116">備註</span><span class="sxs-lookup"><span data-stu-id="9eb7b-116">Remarks</span></span>

<span data-ttu-id="9eb7b-117">工具提示視窗矩形會比其文字顯示矩形稍微大一點，且其原點會向上和向左位移。</span><span class="sxs-lookup"><span data-stu-id="9eb7b-117">A tooltip window rectangle is somewhat larger than its text display rectangle, and its origin is offset up and to the left.</span></span> <span data-ttu-id="9eb7b-118">如果您需要精確地定位工具提示的文字顯示矩形， [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) 訊息會將文字顯示矩形轉換成對應的工具提示視窗矩形，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="9eb7b-118">If you need to accurately position the text display rectangle of a tooltip, the [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message converts a text display rectangle into the corresponding tooltip window rectangle and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb7b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9eb7b-119">Requirements</span></span>



| <span data-ttu-id="9eb7b-120">需求</span><span class="sxs-lookup"><span data-stu-id="9eb7b-120">Requirement</span></span> | <span data-ttu-id="9eb7b-121">值</span><span class="sxs-lookup"><span data-stu-id="9eb7b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb7b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9eb7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb7b-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9eb7b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9eb7b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9eb7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb7b-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9eb7b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9eb7b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9eb7b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eb7b-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb7b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

