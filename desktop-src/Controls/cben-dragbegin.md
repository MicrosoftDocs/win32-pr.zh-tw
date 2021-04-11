---
title: 'CBEN_DRAGBEGIN (Commctrl 的通知碼) '
description: 當使用者開始拖曳顯示在控制項編輯部分的專案影像時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105756"
---
# <a name="cben_dragbegin-notification-code"></a><span data-ttu-id="a5089-105">CBEN \_ DRAGBEGIN 通知碼</span><span class="sxs-lookup"><span data-stu-id="a5089-105">CBEN\_DRAGBEGIN notification code</span></span>

<span data-ttu-id="a5089-106">當使用者開始拖曳顯示在控制項編輯部分的專案影像時傳送。</span><span class="sxs-lookup"><span data-stu-id="a5089-106">Sent when the user begins dragging the image of the item displayed in the edit portion of the control.</span></span> <span data-ttu-id="a5089-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a5089-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a5089-108">參數</span><span class="sxs-lookup"><span data-stu-id="a5089-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5089-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5089-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5089-110">[**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5089-110">A pointer to a [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5089-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5089-111">Return value</span></span>

<span data-ttu-id="a5089-112">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a5089-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5089-113">備註</span><span class="sxs-lookup"><span data-stu-id="a5089-113">Remarks</span></span>

<span data-ttu-id="a5089-114">如果接收應用程式會從控制項中執行拖放功能，應用程式就會開始拖放作業來回應此通知碼。</span><span class="sxs-lookup"><span data-stu-id="a5089-114">If the receiving application implements drag-and-drop functionality from the control, the application will begin the drag-and-drop operation in response to this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5089-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5089-115">Requirements</span></span>



| <span data-ttu-id="a5089-116">需求</span><span class="sxs-lookup"><span data-stu-id="a5089-116">Requirement</span></span> | <span data-ttu-id="a5089-117">值</span><span class="sxs-lookup"><span data-stu-id="a5089-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5089-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5089-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a5089-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5089-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5089-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5089-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a5089-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5089-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5089-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a5089-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5089-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5089-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a5089-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a5089-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a5089-125">**CBEN \_DRAGBEGINW** (Unicode) 和 **CBEN \_ DRAGBEGINA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a5089-125">**CBEN\_DRAGBEGINW** (Unicode) and **CBEN\_DRAGBEGINA** (ANSI)</span></span><br/>             |



 

 





