---
title: 'ICM_DRAW_FLUSH 訊息 (Vfw .h) '
description: ICM 繪圖排清 \_ \_ 訊息會通知轉譯驅動程式，以轉譯任何等候繪製之影像緩衝區的內容。 您可以使用 ICDrawFlush 宏明確地傳送此訊息。
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- ICM_DRAW_FLUSH message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966121"
---
# <a name="icm_draw_flush-message"></a><span data-ttu-id="06275-105">ICM \_ 繪製 \_ 清除訊息</span><span class="sxs-lookup"><span data-stu-id="06275-105">ICM\_DRAW\_FLUSH message</span></span>

<span data-ttu-id="06275-106">**ICM \_ 繪圖 \_** 排清訊息會通知轉譯驅動程式，以轉譯任何等候繪製之影像緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="06275-106">The **ICM\_DRAW\_FLUSH** message notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn.</span></span> <span data-ttu-id="06275-107">您可以使用 [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="06275-107">You can send this message explicitly or by using the [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) macro.</span></span>


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="06275-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="06275-108">Return Value</span></span>

<span data-ttu-id="06275-109">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="06275-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="06275-110">備註</span><span class="sxs-lookup"><span data-stu-id="06275-110">Remarks</span></span>

<span data-ttu-id="06275-111">這則訊息只會由執行自己的非同步解壓縮、時間和繪圖的硬體使用。</span><span class="sxs-lookup"><span data-stu-id="06275-111">This message is used only by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="06275-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="06275-112">Requirements</span></span>



| <span data-ttu-id="06275-113">需求</span><span class="sxs-lookup"><span data-stu-id="06275-113">Requirement</span></span> | <span data-ttu-id="06275-114">值</span><span class="sxs-lookup"><span data-stu-id="06275-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="06275-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06275-115">Minimum supported client</span></span><br/> | <span data-ttu-id="06275-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06275-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="06275-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06275-117">Minimum supported server</span></span><br/> | <span data-ttu-id="06275-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06275-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="06275-119">標頭</span><span class="sxs-lookup"><span data-stu-id="06275-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="06275-120"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="06275-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06275-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06275-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06275-122">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="06275-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="06275-123">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="06275-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





