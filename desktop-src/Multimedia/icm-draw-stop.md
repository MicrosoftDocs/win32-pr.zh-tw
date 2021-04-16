---
title: 'ICM_DRAW_STOP 訊息 (Vfw .h) '
description: ICM \_ 繪製 \_ 停止訊息會通知轉譯驅動程式，以在繪製框架的時機停止其內部時鐘。 您可以使用 ICDrawStop 宏明確地傳送此訊息。
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464993"
---
# <a name="icm_draw_stop-message"></a><span data-ttu-id="3809b-105">ICM \_ 繪圖 \_ 停止訊息</span><span class="sxs-lookup"><span data-stu-id="3809b-105">ICM\_DRAW\_STOP message</span></span>

<span data-ttu-id="3809b-106">**ICM \_ 繪製 \_ 停止** 訊息會通知轉譯驅動程式，以在繪製框架的時機停止其內部時鐘。</span><span class="sxs-lookup"><span data-stu-id="3809b-106">The **ICM\_DRAW\_STOP** message notifies a rendering driver to stop its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="3809b-107">您可以使用 [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3809b-107">You can send this message explicitly or by using the [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) macro.</span></span>


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="3809b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3809b-108">Return Value</span></span>

<span data-ttu-id="3809b-109">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3809b-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3809b-110">備註</span><span class="sxs-lookup"><span data-stu-id="3809b-110">Remarks</span></span>

<span data-ttu-id="3809b-111">此訊息是由執行自己的非同步解壓縮、時間和繪圖的硬體所使用。</span><span class="sxs-lookup"><span data-stu-id="3809b-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="3809b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3809b-112">Requirements</span></span>



| <span data-ttu-id="3809b-113">需求</span><span class="sxs-lookup"><span data-stu-id="3809b-113">Requirement</span></span> | <span data-ttu-id="3809b-114">值</span><span class="sxs-lookup"><span data-stu-id="3809b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3809b-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3809b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3809b-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3809b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3809b-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3809b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3809b-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3809b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3809b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3809b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3809b-120"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="3809b-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3809b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3809b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3809b-122">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="3809b-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3809b-123">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="3809b-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





