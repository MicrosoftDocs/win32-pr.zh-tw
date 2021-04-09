---
title: 'HDN_ITEMCLICK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，指出使用者已按一下控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- HDN_ITEMCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844123"
---
# <a name="hdn_itemclick-notification-code"></a><span data-ttu-id="5e644-105">HDN \_ ITEMCLICK 通知碼</span><span class="sxs-lookup"><span data-stu-id="5e644-105">HDN\_ITEMCLICK notification code</span></span>

<span data-ttu-id="5e644-106">通知標題控制項的父視窗，指出使用者已按一下控制項。</span><span class="sxs-lookup"><span data-stu-id="5e644-106">Notifies a header control's parent window that the user clicked the control.</span></span> <span data-ttu-id="5e644-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="5e644-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5e644-108">參數</span><span class="sxs-lookup"><span data-stu-id="5e644-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e644-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e644-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e644-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，該結構會識別標題控制項並指定已按下之標頭專案的索引，以及用來按一下專案的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="5e644-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that identifies the header control and specifies the index of the header item that was clicked and the mouse button used to click the item.</span></span> <span data-ttu-id="5e644-111">**PItem** 成員會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5e644-111">The **pItem** member is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e644-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e644-112">Return value</span></span>

<span data-ttu-id="5e644-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5e644-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e644-114">備註</span><span class="sxs-lookup"><span data-stu-id="5e644-114">Remarks</span></span>

<span data-ttu-id="5e644-115">標題控制項會在使用者放開滑鼠左鍵之後傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="5e644-115">A header control sends this notification code after the user releases the left mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e644-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e644-116">Requirements</span></span>



| <span data-ttu-id="5e644-117">需求</span><span class="sxs-lookup"><span data-stu-id="5e644-117">Requirement</span></span> | <span data-ttu-id="5e644-118">值</span><span class="sxs-lookup"><span data-stu-id="5e644-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e644-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e644-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5e644-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e644-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e644-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e644-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5e644-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e644-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e644-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5e644-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e644-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e644-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5e644-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="5e644-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5e644-126">**HDN \_ITEMCLICKW** (Unicode) 和 **HDN \_ ITEMCLICKA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="5e644-126">**HDN\_ITEMCLICKW** (Unicode) and **HDN\_ITEMCLICKA** (ANSI)</span></span><br/>               |



 

 





