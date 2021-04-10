---
title: 'TVN_GETINFOTIP (Commctrl 的通知碼) '
description: 由具有電視提示樣式的樹狀檢視控制項所傳送 \_ 。 當控制項要求要顯示在工具提示中的其他文字資訊時，就會傳送此通知碼。 通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686096"
---
# <a name="tvn_getinfotip-notification-code"></a><span data-ttu-id="57a06-106">IZDEBSKI \_ GETINFOTIP 通知碼</span><span class="sxs-lookup"><span data-stu-id="57a06-106">TVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="57a06-107">由具有 [**電視 \_**](tree-view-control-window-styles.md) 提示樣式的樹狀檢視控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="57a06-107">Sent by a tree-view control that has the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span> <span data-ttu-id="57a06-108">當控制項要求要顯示在工具提示中的其他文字資訊時，就會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="57a06-108">This notification code is sent when the control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="57a06-109">通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="57a06-109">The notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a><span data-ttu-id="57a06-110">參數</span><span class="sxs-lookup"><span data-stu-id="57a06-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a06-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57a06-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57a06-112">[**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="57a06-112">Pointer to an [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a06-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="57a06-113">Return value</span></span>

<span data-ttu-id="57a06-114">控制項會忽略此通知碼的傳回值。</span><span class="sxs-lookup"><span data-stu-id="57a06-114">The control ignores the return value for this notification code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57a06-115">備註</span><span class="sxs-lookup"><span data-stu-id="57a06-115">Remarks</span></span>

<span data-ttu-id="57a06-116">此通知碼僅由具有 [**電視 \_**](tree-view-control-window-styles.md) 提示樣式的樹狀檢視控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="57a06-116">This notification code is only sent by tree-view controls that have the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a06-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="57a06-117">Requirements</span></span>



| <span data-ttu-id="57a06-118">需求</span><span class="sxs-lookup"><span data-stu-id="57a06-118">Requirement</span></span> | <span data-ttu-id="57a06-119">值</span><span class="sxs-lookup"><span data-stu-id="57a06-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57a06-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57a06-120">Minimum supported client</span></span><br/> | <span data-ttu-id="57a06-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57a06-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57a06-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57a06-122">Minimum supported server</span></span><br/> | <span data-ttu-id="57a06-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57a06-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57a06-124">標頭</span><span class="sxs-lookup"><span data-stu-id="57a06-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a06-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="57a06-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="57a06-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="57a06-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="57a06-127">**Izdebski \_GETINFOTIPW** (Unicode) 和 **izdebski \_ GETINFOTIPA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="57a06-127">**TVN\_GETINFOTIPW** (Unicode) and **TVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





