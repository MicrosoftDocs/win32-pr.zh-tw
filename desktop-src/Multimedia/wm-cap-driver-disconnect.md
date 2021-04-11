---
title: 'WM_CAP_DRIVER_DISCONNECT 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 驅動程式 \_ 中斷連線] 訊息會中斷捕捉驅動程式與捕捉視窗的連線。 您可以使用 capDriverDisconnect 宏明確地傳送此訊息。'
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934250"
---
# <a name="wm_cap_driver_disconnect-message"></a><span data-ttu-id="5f4d1-105">WM \_ CAP \_ 驅動程式 \_ 中斷連線訊息</span><span class="sxs-lookup"><span data-stu-id="5f4d1-105">WM\_CAP\_DRIVER\_DISCONNECT message</span></span>

<span data-ttu-id="5f4d1-106">[ **WM \_ CAP \_ 驅動程式 \_ 中斷連線]** 訊息會中斷捕捉驅動程式與捕捉視窗的連線。</span><span class="sxs-lookup"><span data-stu-id="5f4d1-106">The **WM\_CAP\_DRIVER\_DISCONNECT** message disconnects a capture driver from a capture window.</span></span> <span data-ttu-id="5f4d1-107">您可以使用 [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="5f4d1-107">You can send this message explicitly or by using the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="5f4d1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f4d1-108">Return Value</span></span>

<span data-ttu-id="5f4d1-109">如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5f4d1-109">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f4d1-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f4d1-110">Requirements</span></span>



| <span data-ttu-id="5f4d1-111">需求</span><span class="sxs-lookup"><span data-stu-id="5f4d1-111">Requirement</span></span> | <span data-ttu-id="5f4d1-112">值</span><span class="sxs-lookup"><span data-stu-id="5f4d1-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5f4d1-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f4d1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5f4d1-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f4d1-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5f4d1-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f4d1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5f4d1-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f4d1-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f4d1-117">標頭</span><span class="sxs-lookup"><span data-stu-id="5f4d1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f4d1-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f4d1-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f4d1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f4d1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f4d1-120">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="5f4d1-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="5f4d1-121">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="5f4d1-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





