---
title: 'MCIWNDM_SETTIMERS 訊息 (Vfw .h) '
description: MCIWNDM \_ SETTIMERS 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新顯示在視窗標題列中的位置資訊，以及將通知訊息傳送至父視窗的更新期間。
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685591"
---
# <a name="mciwndm_settimers-message"></a><span data-ttu-id="b443d-104">MCIWNDM \_ SETTIMERS 訊息</span><span class="sxs-lookup"><span data-stu-id="b443d-104">MCIWNDM\_SETTIMERS message</span></span>

<span data-ttu-id="b443d-105">**MCIWNDM \_ SETTIMERS** 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新顯示在視窗標題列中的位置資訊，以及將通知訊息傳送至父視窗的更新期間。</span><span class="sxs-lookup"><span data-stu-id="b443d-105">The **MCIWNDM\_SETTIMERS** message sets the update periods used by MCIWnd to update the trackbar in the MCIWnd window, update the position information displayed in the window title bar, and send notification messages to the parent window.</span></span> <span data-ttu-id="b443d-106">您可以使用 [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b443d-106">You can send this message explicitly or by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span>


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a><span data-ttu-id="b443d-107">參數</span><span class="sxs-lookup"><span data-stu-id="b443d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b443d-108"><span id="active"></span><span id="ACTIVE"></span>*積極*</span><span class="sxs-lookup"><span data-stu-id="b443d-108"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="b443d-109">當 MCIWnd 為使用中視窗時，所使用的更新期間。</span><span class="sxs-lookup"><span data-stu-id="b443d-109">Update period used by MCIWnd when it is the active window.</span></span> <span data-ttu-id="b443d-110">預設值為500毫秒。</span><span class="sxs-lookup"><span data-stu-id="b443d-110">The default value is 500 milliseconds.</span></span> <span data-ttu-id="b443d-111">此值的儲存體限制為16位。</span><span class="sxs-lookup"><span data-stu-id="b443d-111">Storage for this value is limited to 16 bits.</span></span>

</dd> <dt>

<span data-ttu-id="b443d-112"><span id="inactive"></span><span id="INACTIVE"></span>*無效*</span><span class="sxs-lookup"><span data-stu-id="b443d-112"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="b443d-113">MCIWnd 在非作用中視窗時所使用的更新期間。</span><span class="sxs-lookup"><span data-stu-id="b443d-113">Update period used by MCIWnd when it is the inactive window.</span></span> <span data-ttu-id="b443d-114">預設值為2000毫秒。</span><span class="sxs-lookup"><span data-stu-id="b443d-114">The default value is 2000 milliseconds.</span></span> <span data-ttu-id="b443d-115">此值的儲存體限制為16位。</span><span class="sxs-lookup"><span data-stu-id="b443d-115">Storage for this value is limited to 16 bits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b443d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b443d-116">Return Value</span></span>

<span data-ttu-id="b443d-117">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b443d-117">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b443d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b443d-118">Requirements</span></span>



| <span data-ttu-id="b443d-119">需求</span><span class="sxs-lookup"><span data-stu-id="b443d-119">Requirement</span></span> | <span data-ttu-id="b443d-120">值</span><span class="sxs-lookup"><span data-stu-id="b443d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b443d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b443d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b443d-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b443d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b443d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b443d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b443d-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b443d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b443d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b443d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b443d-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="b443d-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b443d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b443d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b443d-128">**MCIWndSetTimers**</span><span class="sxs-lookup"><span data-stu-id="b443d-128">**MCIWndSetTimers**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





