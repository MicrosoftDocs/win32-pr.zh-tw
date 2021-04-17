---
title: 'ICM_DECOMPRESSEX_END 訊息 (Vfw .h) '
description: ICM \_ DECOMPRESSEX \_ 終端訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。 您可以使用 ICDecompressExEnd 宏明確地傳送此訊息。
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- ICM_DECOMPRESSEX_END message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509151"
---
# <a name="icm_decompressex_end-message"></a><span data-ttu-id="a91a7-105">ICM \_ DECOMPRESSEX \_ 結束訊息</span><span class="sxs-lookup"><span data-stu-id="a91a7-105">ICM\_DECOMPRESSEX\_END message</span></span>

<span data-ttu-id="a91a7-106">**ICM \_ DECOMPRESSEX \_ 終端** 訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。</span><span class="sxs-lookup"><span data-stu-id="a91a7-106">The **ICM\_DECOMPRESSEX\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="a91a7-107">您可以使用 [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a91a7-107">You can send this message explicitly or by using the [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) macro.</span></span>


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="a91a7-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a91a7-108">Return Value</span></span>

<span data-ttu-id="a91a7-109">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a91a7-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a91a7-110">備註</span><span class="sxs-lookup"><span data-stu-id="a91a7-110">Remarks</span></span>

<span data-ttu-id="a91a7-111">驅動程式會釋出配置給 [**ICM \_ DECOMPRESSEX \_ 開始**](icm-decompressex-begin.md) 訊息的任何資源。</span><span class="sxs-lookup"><span data-stu-id="a91a7-111">The driver frees any resources allocated for the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

<span data-ttu-id="a91a7-112">[**ICM \_DECOMPRESSEX \_ BEGIN**](icm-decompressex-begin.md) 和 **ICM \_ DECOMPRESSEX \_ END** 不會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="a91a7-112">[**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) and **ICM\_DECOMPRESSEX\_END** do not nest.</span></span> <span data-ttu-id="a91a7-113">如果您的驅動程式收到 Icm DECOMPRESSEX 在使用 **icm \_ DECOMPRESSEX \_ END** 停止解壓縮之前 **\_ \_ 開始**，則應該以新的參數重新開機解壓縮。</span><span class="sxs-lookup"><span data-stu-id="a91a7-113">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a91a7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a91a7-114">Requirements</span></span>



| <span data-ttu-id="a91a7-115">需求</span><span class="sxs-lookup"><span data-stu-id="a91a7-115">Requirement</span></span> | <span data-ttu-id="a91a7-116">值</span><span class="sxs-lookup"><span data-stu-id="a91a7-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a91a7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a91a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a91a7-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a91a7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a91a7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a91a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a91a7-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a91a7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a91a7-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a91a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a91a7-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="a91a7-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a91a7-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a91a7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a91a7-124">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="a91a7-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a91a7-125">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="a91a7-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





