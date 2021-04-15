---
title: 'ICM_COMPRESS_END 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 結束訊息會通知影片壓縮驅動程式，以結束壓縮和配置給壓縮的可用資源。 您可以使用 ICCompressEnd 宏明確地傳送此訊息。
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464836"
---
# <a name="icm_compress_end-message"></a><span data-ttu-id="3c061-105">ICM \_ 壓縮 \_ 結束訊息</span><span class="sxs-lookup"><span data-stu-id="3c061-105">ICM\_COMPRESS\_END message</span></span>

<span data-ttu-id="3c061-106">**ICM \_ 壓縮 \_ 結束** 訊息會通知影片壓縮驅動程式，以結束壓縮和配置給壓縮的可用資源。</span><span class="sxs-lookup"><span data-stu-id="3c061-106">The **ICM\_COMPRESS\_END** message notifies a video compression driver to end compression and free resources allocated for compression.</span></span> <span data-ttu-id="3c061-107">您可以使用 [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3c061-107">You can send this message explicitly or by using the [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) macro.</span></span>


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="3c061-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c061-108">Return Value</span></span>

<span data-ttu-id="3c061-109">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c061-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c061-110">備註</span><span class="sxs-lookup"><span data-stu-id="3c061-110">Remarks</span></span>

<span data-ttu-id="3c061-111">BC-VCM-LVM-HYPERV 會儲存最近的 [**ICM \_ 壓縮 \_ 開始**](icm-compress-begin.md) 訊息的設定。</span><span class="sxs-lookup"><span data-stu-id="3c061-111">VCM saves the settings of the most recent [**ICM\_COMPRESS\_BEGIN**](icm-compress-begin.md) message.</span></span> <span data-ttu-id="3c061-112">**ICM \_壓縮 \_ BEGIN** 和 **ICM \_ 壓縮 \_ 結束** 不會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="3c061-112">**ICM\_COMPRESS\_BEGIN** and **ICM\_COMPRESS\_END** do not nest.</span></span> <span data-ttu-id="3c061-113">如果您的驅動程式會在使用 **icm \_ 壓縮 \_ 結束** 的情況下，于壓縮停止之前收到 **icm \_ 壓縮 \_ 開始**，則應該以新的參數重新開機壓縮。</span><span class="sxs-lookup"><span data-stu-id="3c061-113">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c061-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c061-114">Requirements</span></span>



| <span data-ttu-id="3c061-115">需求</span><span class="sxs-lookup"><span data-stu-id="3c061-115">Requirement</span></span> | <span data-ttu-id="3c061-116">值</span><span class="sxs-lookup"><span data-stu-id="3c061-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c061-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c061-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3c061-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c061-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3c061-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c061-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3c061-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c061-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c061-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3c061-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c061-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c061-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c061-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c061-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c061-124">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="3c061-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3c061-125">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="3c061-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





