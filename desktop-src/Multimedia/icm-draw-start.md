---
title: 'ICM_DRAW_START 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ 開始訊息會通知轉譯驅動程式，以在繪製框架的時機啟動其內部時鐘。 您可以使用 ICDrawStart 宏明確地傳送此訊息。
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384482"
---
# <a name="icm_draw_start-message"></a><span data-ttu-id="d6e85-105">ICM \_ 繪圖 \_ 開始訊息</span><span class="sxs-lookup"><span data-stu-id="d6e85-105">ICM\_DRAW\_START message</span></span>

<span data-ttu-id="d6e85-106">**ICM \_ DRAW \_ 開始** 訊息會通知轉譯驅動程式，以在繪製框架的時機啟動其內部時鐘。</span><span class="sxs-lookup"><span data-stu-id="d6e85-106">The **ICM\_DRAW\_START** message notifies a rendering driver to start its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="d6e85-107">您可以使用 [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d6e85-107">You can send this message explicitly or by using the [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) macro.</span></span>


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="d6e85-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6e85-108">Return Value</span></span>

<span data-ttu-id="d6e85-109">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d6e85-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6e85-110">備註</span><span class="sxs-lookup"><span data-stu-id="d6e85-110">Remarks</span></span>

<span data-ttu-id="d6e85-111">此訊息是由執行自己的非同步解壓縮、時間和繪圖的硬體所使用。</span><span class="sxs-lookup"><span data-stu-id="d6e85-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="d6e85-112">當驅動程式收到此訊息時，它應該會以 [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) 訊息指定的速率開始轉譯資料。</span><span class="sxs-lookup"><span data-stu-id="d6e85-112">When the driver receives this message, it should start rendering data at the rate specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="d6e85-113">**Icm \_ 繪圖 \_ 開始** 和 [**ICM \_ 繪圖 \_ 停止**](icm-draw-stop.md)訊息不會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="d6e85-113">The **ICM\_DRAW\_START** and [**ICM\_DRAW\_STOP**](icm-draw-stop.md) messages do not nest.</span></span> <span data-ttu-id="d6e85-114">如果您的驅動程式會在使用 **icm \_ draw \_ STOP** 停止轉譯之前收到 **icm \_ draw \_ 開始**，則應該以新的參數重新開機轉譯。</span><span class="sxs-lookup"><span data-stu-id="d6e85-114">If your driver receives **ICM\_DRAW\_START** before rendering is stopped with **ICM\_DRAW\_STOP**, it should restart rendering with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e85-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6e85-115">Requirements</span></span>



| <span data-ttu-id="d6e85-116">需求</span><span class="sxs-lookup"><span data-stu-id="d6e85-116">Requirement</span></span> | <span data-ttu-id="d6e85-117">值</span><span class="sxs-lookup"><span data-stu-id="d6e85-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d6e85-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6e85-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e85-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6e85-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d6e85-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6e85-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e85-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6e85-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d6e85-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d6e85-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6e85-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="d6e85-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6e85-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6e85-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e85-125">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="d6e85-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="d6e85-126">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="d6e85-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





