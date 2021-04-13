---
title: 'MCIWNDM_SETINACTIVETIMER 訊息 (Vfw .h) '
description: MCIWNDM \_ SETINACTIVETIMER 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新在視窗標題列中顯示的位置資訊，以及在 MCIWnd 視窗處於非使用中狀態時將通知訊息傳送至父視窗的更新期間。 您可以使用 MCIWndSetInactiveTimer 宏明確地傳送此訊息。
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508891"
---
# <a name="mciwndm_setinactivetimer-message"></a><span data-ttu-id="f9c5b-105">MCIWNDM \_ SETINACTIVETIMER 訊息</span><span class="sxs-lookup"><span data-stu-id="f9c5b-105">MCIWNDM\_SETINACTIVETIMER message</span></span>

<span data-ttu-id="f9c5b-106">**MCIWNDM \_ SETINACTIVETIMER** 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新在視窗標題列中顯示的位置資訊，以及在 MCIWnd 視窗處於非使用中狀態時將通知訊息傳送至父視窗的更新期間。</span><span class="sxs-lookup"><span data-stu-id="f9c5b-106">The **MCIWNDM\_SETINACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive.</span></span> <span data-ttu-id="f9c5b-107">您可以使用 [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="f9c5b-107">You can send this message explicitly or by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span>


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="f9c5b-108">參數</span><span class="sxs-lookup"><span data-stu-id="f9c5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9c5b-109"><span id="inactive"></span><span id="INACTIVE"></span>*無效*</span><span class="sxs-lookup"><span data-stu-id="f9c5b-109"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="f9c5b-110">更新期間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f9c5b-110">Update period, in milliseconds.</span></span> <span data-ttu-id="f9c5b-111">預設值為2000毫秒。</span><span class="sxs-lookup"><span data-stu-id="f9c5b-111">The default is 2000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9c5b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9c5b-112">Return Value</span></span>

<span data-ttu-id="f9c5b-113">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f9c5b-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c5b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9c5b-114">Requirements</span></span>



| <span data-ttu-id="f9c5b-115">需求</span><span class="sxs-lookup"><span data-stu-id="f9c5b-115">Requirement</span></span> | <span data-ttu-id="f9c5b-116">值</span><span class="sxs-lookup"><span data-stu-id="f9c5b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f9c5b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9c5b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c5b-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9c5b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f9c5b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9c5b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c5b-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9c5b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f9c5b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f9c5b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9c5b-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9c5b-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c5b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9c5b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c5b-124">**MCIWndSetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="f9c5b-124">**MCIWndSetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





