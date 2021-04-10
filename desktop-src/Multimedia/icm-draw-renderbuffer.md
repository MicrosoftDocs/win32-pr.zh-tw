---
title: 'ICM_DRAW_RENDERBUFFER 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ RENDERBUFFER 訊息會通知轉譯驅動程式，以繪製已傳遞給它的框架。 您可以使用 ICDrawRenderBuffer 宏明確地傳送此訊息。
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- ICM_DRAW_RENDERBUFFER message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934843"
---
# <a name="icm_draw_renderbuffer-message"></a><span data-ttu-id="b0c8a-105">ICM \_ 繪圖 \_ RENDERBUFFER 訊息</span><span class="sxs-lookup"><span data-stu-id="b0c8a-105">ICM\_DRAW\_RENDERBUFFER message</span></span>

<span data-ttu-id="b0c8a-106">**ICM \_ DRAW \_ RENDERBUFFER** 訊息會通知轉譯驅動程式，以繪製已傳遞給它的框架。</span><span class="sxs-lookup"><span data-stu-id="b0c8a-106">The **ICM\_DRAW\_RENDERBUFFER** message notifies a rendering driver to draw the frames that have been passed to it.</span></span> <span data-ttu-id="b0c8a-107">您可以使用 [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b0c8a-107">You can send this message explicitly or by using the [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) macro.</span></span>


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="b0c8a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0c8a-108">Return Value</span></span>

<span data-ttu-id="b0c8a-109">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b0c8a-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0c8a-110">備註</span><span class="sxs-lookup"><span data-stu-id="b0c8a-110">Remarks</span></span>

<span data-ttu-id="b0c8a-111">使用此訊息搭配執行自己的非同步解壓縮、計時和繪製的硬體。</span><span class="sxs-lookup"><span data-stu-id="b0c8a-111">Use this message with hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="b0c8a-112">此訊息通常用來執行搜尋作業，而必須特別指示驅動程式顯示每個傳遞給它的影片畫面，而不是播放一連串的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="b0c8a-112">This message is typically used to perform a seek operation when the driver must be specifically instructed to display each video frame passed to it rather than playing a sequence of video frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0c8a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0c8a-113">Requirements</span></span>



| <span data-ttu-id="b0c8a-114">需求</span><span class="sxs-lookup"><span data-stu-id="b0c8a-114">Requirement</span></span> | <span data-ttu-id="b0c8a-115">值</span><span class="sxs-lookup"><span data-stu-id="b0c8a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b0c8a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0c8a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b0c8a-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0c8a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b0c8a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0c8a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b0c8a-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0c8a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b0c8a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b0c8a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0c8a-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0c8a-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0c8a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0c8a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c8a-123">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="b0c8a-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b0c8a-124">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="b0c8a-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





