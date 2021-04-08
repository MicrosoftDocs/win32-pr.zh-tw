---
title: 'ICM_DECOMPRESS_END 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 結束訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。 您可以使用 ICDecompressEnd 宏明確地傳送此訊息。
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686275"
---
# <a name="icm_decompress_end-message"></a><span data-ttu-id="ccf23-105">ICM \_ 解壓縮 \_ 結束訊息</span><span class="sxs-lookup"><span data-stu-id="ccf23-105">ICM\_DECOMPRESS\_END message</span></span>

<span data-ttu-id="ccf23-106">**ICM \_ 解壓縮 \_ 結束** 訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。</span><span class="sxs-lookup"><span data-stu-id="ccf23-106">The **ICM\_DECOMPRESS\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="ccf23-107">您可以使用 [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ccf23-107">You can send this message explicitly or by using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ccf23-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccf23-108">Return Value</span></span>

<span data-ttu-id="ccf23-109">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ccf23-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf23-110">備註</span><span class="sxs-lookup"><span data-stu-id="ccf23-110">Remarks</span></span>

<span data-ttu-id="ccf23-111">驅動程式應該釋放配置給 [**ICM \_ 解壓縮 \_ 開始**](icm-decompress-begin.md) 訊息的任何資源。</span><span class="sxs-lookup"><span data-stu-id="ccf23-111">The driver should free any resources allocated for the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="ccf23-112">[**ICM \_解壓縮 \_ 開始**](icm-decompress-begin.md) 和 **ICM \_ 解壓縮 \_ 結束** 不會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="ccf23-112">[**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) and **ICM\_DECOMPRESS\_END** do not nest.</span></span> <span data-ttu-id="ccf23-113">如果您的驅動程式在使用 **icm \_ 解壓縮 \_ 結束** 解壓縮之前收到 **icm \_ 解壓縮 \_** ，則應該以新的參數重新開機解壓縮。</span><span class="sxs-lookup"><span data-stu-id="ccf23-113">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf23-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccf23-114">Requirements</span></span>



| <span data-ttu-id="ccf23-115">需求</span><span class="sxs-lookup"><span data-stu-id="ccf23-115">Requirement</span></span> | <span data-ttu-id="ccf23-116">值</span><span class="sxs-lookup"><span data-stu-id="ccf23-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ccf23-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccf23-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf23-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccf23-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ccf23-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccf23-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf23-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccf23-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ccf23-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ccf23-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccf23-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf23-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf23-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccf23-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf23-124">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="ccf23-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ccf23-125">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="ccf23-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





