---
title: 'ICM_DRAW_END 訊息 (Vfw .h) '
description: ICM \_ 繪製 \_ 結束訊息會通知轉譯驅動程式將目前的影像解壓縮至螢幕，以及釋放配置給解壓縮和繪製的資源。 您可以使用 ICDrawEnd 宏明確地傳送此訊息。
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- ICM_DRAW_END message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686023"
---
# <a name="icm_draw_end-message"></a><span data-ttu-id="1d6ba-105">ICM \_ 繪製 \_ 結束訊息</span><span class="sxs-lookup"><span data-stu-id="1d6ba-105">ICM\_DRAW\_END message</span></span>

<span data-ttu-id="1d6ba-106">**ICM \_ 繪製 \_ 結束** 訊息會通知轉譯驅動程式將目前的影像解壓縮至螢幕，以及釋放配置給解壓縮和繪製的資源。</span><span class="sxs-lookup"><span data-stu-id="1d6ba-106">The **ICM\_DRAW\_END** message notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing.</span></span> <span data-ttu-id="1d6ba-107">您可以使用 [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1d6ba-107">You can send this message explicitly or by using the [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macro.</span></span>


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="1d6ba-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d6ba-108">Return Value</span></span>

<span data-ttu-id="1d6ba-109">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1d6ba-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d6ba-110">備註</span><span class="sxs-lookup"><span data-stu-id="1d6ba-110">Remarks</span></span>

<span data-ttu-id="1d6ba-111">[**Icm \_ draw \_ BEGIN**](icm-draw-begin.md)和 **icm \_ draw \_ END** 訊息不會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="1d6ba-111">The [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) and **ICM\_DRAW\_END** messages do not nest.</span></span> <span data-ttu-id="1d6ba-112">如果您的驅動程式會在使用 **icm \_ draw \_ END** 停止解壓縮之前 **\_ \_ 開始進行 icm 繪製**，則應該以新的參數重新開機解壓縮。</span><span class="sxs-lookup"><span data-stu-id="1d6ba-112">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d6ba-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d6ba-113">Requirements</span></span>



| <span data-ttu-id="1d6ba-114">需求</span><span class="sxs-lookup"><span data-stu-id="1d6ba-114">Requirement</span></span> | <span data-ttu-id="1d6ba-115">值</span><span class="sxs-lookup"><span data-stu-id="1d6ba-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1d6ba-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d6ba-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1d6ba-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d6ba-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1d6ba-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d6ba-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1d6ba-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d6ba-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1d6ba-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1d6ba-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d6ba-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d6ba-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d6ba-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d6ba-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6ba-123">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="1d6ba-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="1d6ba-124">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="1d6ba-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





