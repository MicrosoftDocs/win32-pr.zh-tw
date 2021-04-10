---
title: 'PGN_SCROLL (Commctrl 的通知碼) '
description: 通知頁面控制項的父視窗，其中包含的視窗即將進行滾動。 此通知會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094420"
---
# <a name="pgn_scroll-notification-code"></a><span data-ttu-id="aa429-105">PGN \_ 捲軸通知碼</span><span class="sxs-lookup"><span data-stu-id="aa429-105">PGN\_SCROLL notification code</span></span>

<span data-ttu-id="aa429-106">通知頁面控制項的父視窗，其中包含的視窗即將進行滾動。</span><span class="sxs-lookup"><span data-stu-id="aa429-106">Notifies a pager control's parent window that the contained window is about to be scrolled.</span></span> <span data-ttu-id="aa429-107">此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="aa429-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="aa429-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa429-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa429-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa429-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa429-110">[**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)結構的指標，其中包含和接收通知程式碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aa429-110">Pointer to an [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="aa429-111">此結構的 **iDir** 成員會指出捲軸的方向。</span><span class="sxs-lookup"><span data-stu-id="aa429-111">The **iDir** member of this structure indicates the direction of the scroll.</span></span> <span data-ttu-id="aa429-112">**IXpos** 和 **iYpos** 成員包含滾動之前所包含視窗的水準和垂直位置。</span><span class="sxs-lookup"><span data-stu-id="aa429-112">The **iXpos** and **iYpos** members contain the horizontal and vertical position of the contained window prior to the scroll.</span></span> <span data-ttu-id="aa429-113">**IScroll** 成員包含預設的滾動差異數量。</span><span class="sxs-lookup"><span data-stu-id="aa429-113">The **iScroll** member contains the default scroll delta amount.</span></span> <span data-ttu-id="aa429-114">如有需要，您可以將此成員修改為不同的捲軸量。</span><span class="sxs-lookup"><span data-stu-id="aa429-114">You can modify this member to a different scroll amount if desired.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa429-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa429-115">Return value</span></span>

<span data-ttu-id="aa429-116">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="aa429-116">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa429-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa429-117">Requirements</span></span>



| <span data-ttu-id="aa429-118">需求</span><span class="sxs-lookup"><span data-stu-id="aa429-118">Requirement</span></span> | <span data-ttu-id="aa429-119">值</span><span class="sxs-lookup"><span data-stu-id="aa429-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa429-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa429-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa429-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa429-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa429-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa429-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa429-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa429-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa429-124">標頭</span><span class="sxs-lookup"><span data-stu-id="aa429-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa429-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa429-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





