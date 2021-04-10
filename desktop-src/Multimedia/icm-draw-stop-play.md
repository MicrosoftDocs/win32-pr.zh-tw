---
title: 'ICM_DRAW_STOP_PLAY 訊息 (Vfw .h) '
description: '\_ \_ 當播放作業完成時，ICM DRAW 停止 \_ 播放訊息會通知轉譯驅動程式。 您可以使用 ICDrawStopPlay 宏明確地傳送此訊息。'
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- ICM_DRAW_STOP_PLAY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106553"
---
# <a name="icm_draw_stop_play-message"></a><span data-ttu-id="66400-105">ICM \_ 繪圖 \_ 停止 \_ 播放訊息</span><span class="sxs-lookup"><span data-stu-id="66400-105">ICM\_DRAW\_STOP\_PLAY message</span></span>

<span data-ttu-id="66400-106">當播放作業完成時， **ICM \_ DRAW \_ 停止 \_ 播放** 訊息會通知轉譯驅動程式。</span><span class="sxs-lookup"><span data-stu-id="66400-106">The **ICM\_DRAW\_STOP\_PLAY** message notifies a rendering driver when a play operation is complete.</span></span> <span data-ttu-id="66400-107">您可以使用 [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="66400-107">You can send this message explicitly or by using the [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) macro.</span></span>


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="66400-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="66400-108">Return Value</span></span>

<span data-ttu-id="66400-109">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="66400-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66400-110">備註</span><span class="sxs-lookup"><span data-stu-id="66400-110">Remarks</span></span>

<span data-ttu-id="66400-111">當播放作業完成時，請使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="66400-111">Use this message when the play operation is complete.</span></span> <span data-ttu-id="66400-112">使用 [**ICM \_ 繪製 \_ 停止**](icm-draw-stop.md) 訊息來結束計時。</span><span class="sxs-lookup"><span data-stu-id="66400-112">Use the [**ICM\_DRAW\_STOP**](icm-draw-stop.md) message to end timing.</span></span>

## <a name="requirements"></a><span data-ttu-id="66400-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="66400-113">Requirements</span></span>



| <span data-ttu-id="66400-114">需求</span><span class="sxs-lookup"><span data-stu-id="66400-114">Requirement</span></span> | <span data-ttu-id="66400-115">值</span><span class="sxs-lookup"><span data-stu-id="66400-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="66400-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66400-116">Minimum supported client</span></span><br/> | <span data-ttu-id="66400-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66400-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="66400-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66400-118">Minimum supported server</span></span><br/> | <span data-ttu-id="66400-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66400-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="66400-120">標頭</span><span class="sxs-lookup"><span data-stu-id="66400-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="66400-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="66400-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66400-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66400-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66400-123">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="66400-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="66400-124">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="66400-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





