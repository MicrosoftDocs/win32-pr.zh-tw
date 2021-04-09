---
title: 'TRBN_THUMBPOSCHANGING (Commctrl 的通知碼) '
description: 通知正在進行的捲軸位置變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945901"
---
# <a name="trbn_thumbposchanging-notification-code"></a><span data-ttu-id="14787-105">TRBN \_ THUMBPOSCHANGING 通知碼</span><span class="sxs-lookup"><span data-stu-id="14787-105">TRBN\_THUMBPOSCHANGING notification code</span></span>

<span data-ttu-id="14787-106">通知正在進行的捲軸位置變更。</span><span class="sxs-lookup"><span data-stu-id="14787-106">Notifies that the thumb position on a trackbar is changing.</span></span> <span data-ttu-id="14787-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="14787-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="14787-108">參數</span><span class="sxs-lookup"><span data-stu-id="14787-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14787-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14787-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14787-110">[**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="14787-110">Pointer to a [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) structure.</span></span> <span data-ttu-id="14787-111">呼叫端負責配置此結構並設定其成員，包括包含之 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="14787-111">The caller is responsible for allocating this structure and setting its members, including the members of the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14787-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="14787-112">Return value</span></span>

<span data-ttu-id="14787-113">傳回 **TRUE** 以防止捲動方塊移至指定的位置。</span><span class="sxs-lookup"><span data-stu-id="14787-113">Return **TRUE** to prevent the thumb from moving to the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="14787-114">備註</span><span class="sxs-lookup"><span data-stu-id="14787-114">Remarks</span></span>

<span data-ttu-id="14787-115">將此通知傳送給未接聽 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息的用戶端。</span><span class="sxs-lookup"><span data-stu-id="14787-115">Send this notification to clients that do not listen for [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="14787-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="14787-116">Requirements</span></span>



| <span data-ttu-id="14787-117">需求</span><span class="sxs-lookup"><span data-stu-id="14787-117">Requirement</span></span> | <span data-ttu-id="14787-118">值</span><span class="sxs-lookup"><span data-stu-id="14787-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14787-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14787-119">Minimum supported client</span></span><br/> | <span data-ttu-id="14787-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14787-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14787-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14787-121">Minimum supported server</span></span><br/> | <span data-ttu-id="14787-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14787-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14787-123">標頭</span><span class="sxs-lookup"><span data-stu-id="14787-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="14787-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="14787-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





