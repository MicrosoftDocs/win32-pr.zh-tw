---
title: 'MCIWNDM_SETOWNER 訊息 (Vfw .h) '
description: MCIWNDM \_ SETOWNER 訊息會設定視窗，以接收與 MCIWnd 視窗相關聯的通知訊息。 您可以使用 MCIWndSetOwner 宏明確地傳送此訊息。
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- MCIWNDM_SETOWNER message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104718"
---
# <a name="mciwndm_setowner-message"></a><span data-ttu-id="fa81a-105">MCIWNDM \_ SETOWNER 訊息</span><span class="sxs-lookup"><span data-stu-id="fa81a-105">MCIWNDM\_SETOWNER message</span></span>

<span data-ttu-id="fa81a-106">**MCIWNDM \_ SETOWNER** 訊息會設定視窗，以接收與 MCIWnd 視窗相關聯的通知訊息。</span><span class="sxs-lookup"><span data-stu-id="fa81a-106">The **MCIWNDM\_SETOWNER** message sets the window to receive notification messages associated with the MCIWnd window.</span></span> <span data-ttu-id="fa81a-107">您可以使用 [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="fa81a-107">You can send this message explicitly or by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="fa81a-108">參數</span><span class="sxs-lookup"><span data-stu-id="fa81a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa81a-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span><span class="sxs-lookup"><span data-stu-id="fa81a-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span></span>
</dt> <dd>

<span data-ttu-id="fa81a-110">接收通知訊息的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="fa81a-110">Handle to the window to receive the notification messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa81a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa81a-111">Return Value</span></span>

<span data-ttu-id="fa81a-112">傳回零。</span><span class="sxs-lookup"><span data-stu-id="fa81a-112">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa81a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa81a-113">Requirements</span></span>



| <span data-ttu-id="fa81a-114">需求</span><span class="sxs-lookup"><span data-stu-id="fa81a-114">Requirement</span></span> | <span data-ttu-id="fa81a-115">值</span><span class="sxs-lookup"><span data-stu-id="fa81a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fa81a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa81a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa81a-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa81a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fa81a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa81a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa81a-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa81a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fa81a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fa81a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa81a-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa81a-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa81a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa81a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa81a-123">**MCIWndSetOwner**</span><span class="sxs-lookup"><span data-stu-id="fa81a-123">**MCIWndSetOwner**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





