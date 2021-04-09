---
title: 'ICM_DECOMPRESS 訊息 (Vfw .h) '
description: ICM \_ 解壓縮訊息會通知影片解壓縮驅動程式將資料框架解壓縮至應用程式定義的緩衝區。
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- ICM_DECOMPRESS message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025366"
---
# <a name="icm_decompress-message"></a><span data-ttu-id="6056b-104">ICM \_ 解壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="6056b-104">ICM\_DECOMPRESS message</span></span>

<span data-ttu-id="6056b-105">**ICM \_ 解壓縮** 訊息會通知影片解壓縮驅動程式將資料框架解壓縮至應用程式定義的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6056b-105">The **ICM\_DECOMPRESS** message notifies a video decompression driver to decompress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="6056b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6056b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6056b-107"><span id="icd"></span><span id="ICD"></span>*Icd*</span><span class="sxs-lookup"><span data-stu-id="6056b-107"><span id="icd"></span><span id="ICD"></span>*icd*</span></span>
</dt> <dd>

<span data-ttu-id="6056b-108">[**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6056b-108">Pointer to an [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6056b-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="6056b-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="6056b-110">[**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6056b-110">Size, in bytes, of [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6056b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6056b-111">Return Value</span></span>

<span data-ttu-id="6056b-112">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6056b-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6056b-113">備註</span><span class="sxs-lookup"><span data-stu-id="6056b-113">Remarks</span></span>

<span data-ttu-id="6056b-114">如果您希望驅動程式將資料直接解壓縮到畫面，請傳送 [**ICM \_ 繪製**](icm-draw.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="6056b-114">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="6056b-115">如果在 [**ICM \_ 解壓縮 \_ 開始**](icm-decompress-begin.md) 訊息之前收到此訊息，驅動程式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6056b-115">The driver returns an error if this message is received before the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6056b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6056b-116">Requirements</span></span>



| <span data-ttu-id="6056b-117">需求</span><span class="sxs-lookup"><span data-stu-id="6056b-117">Requirement</span></span> | <span data-ttu-id="6056b-118">值</span><span class="sxs-lookup"><span data-stu-id="6056b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6056b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6056b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6056b-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6056b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6056b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6056b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6056b-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6056b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6056b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6056b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6056b-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="6056b-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6056b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6056b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6056b-126">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="6056b-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="6056b-127">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="6056b-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





