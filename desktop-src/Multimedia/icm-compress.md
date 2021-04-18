---
title: 'ICM_COMPRESS 訊息 (Vfw .h) '
description: ICM \_ 壓縮訊息會通知視訊壓縮驅動程式，將資料框架壓縮成應用程式定義的緩衝區。
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965748"
---
# <a name="icm_compress-message"></a><span data-ttu-id="b6ca8-104">ICM \_ 壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="b6ca8-104">ICM\_COMPRESS message</span></span>

<span data-ttu-id="b6ca8-105">**ICM \_ 壓縮** 訊息會通知視訊壓縮驅動程式，將資料框架壓縮成應用程式定義的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b6ca8-105">The **ICM\_COMPRESS** message notifies a video compression driver to compress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="b6ca8-106">參數</span><span class="sxs-lookup"><span data-stu-id="b6ca8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ca8-107"><span id="icc"></span><span id="ICC"></span>*Icc*</span><span class="sxs-lookup"><span data-stu-id="b6ca8-107"><span id="icc"></span><span id="ICC"></span>*icc*</span></span>
</dt> <dd>

<span data-ttu-id="b6ca8-108">[**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b6ca8-108">Pointer to an [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) structure.</span></span> <span data-ttu-id="b6ca8-109">下列結構的成員會指定壓縮參數： **lpbiInput**、 **lpInput**、 **lpbiOutput**、 **lpOutput**、 **lpbiPrev**、 **lpPrev**、 **lpckid**、 **lpdwFlags**、 **dwFrameSize** 和 **dwQuality**。</span><span class="sxs-lookup"><span data-stu-id="b6ca8-109">The following members of this structure specify the compression parameters: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize**, and **dwQuality**.</span></span> <span data-ttu-id="b6ca8-110">驅動程式也應該使用與 **LpbiOutput** **ICCOMPRESS** 相關聯之 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))結構的 **biSizeImage** 成員，以傳回壓縮框架的大小。</span><span class="sxs-lookup"><span data-stu-id="b6ca8-110">The driver should also use the **biSizeImage** member of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure associated with **lpbiOutput** of **ICCOMPRESS** to return the size of the compressed frame.</span></span>

</dd> <dt>

<span data-ttu-id="b6ca8-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6ca8-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b6ca8-112">[**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6ca8-112">Size, in bytes, of [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6ca8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6ca8-113">Return Value</span></span>

<span data-ttu-id="b6ca8-114">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b6ca8-114">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ca8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6ca8-115">Requirements</span></span>



| <span data-ttu-id="b6ca8-116">需求</span><span class="sxs-lookup"><span data-stu-id="b6ca8-116">Requirement</span></span> | <span data-ttu-id="b6ca8-117">值</span><span class="sxs-lookup"><span data-stu-id="b6ca8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b6ca8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6ca8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ca8-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6ca8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b6ca8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6ca8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ca8-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6ca8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b6ca8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b6ca8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6ca8-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6ca8-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6ca8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6ca8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ca8-125">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="b6ca8-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b6ca8-126">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="b6ca8-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

