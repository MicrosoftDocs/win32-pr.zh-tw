---
title: 'ICM_DECOMPRESSEX 訊息 (Vfw .h) '
description: ICM \_ DECOMPRESSEX 訊息會通知影片壓縮驅動程式將資料框架直接解壓縮至螢幕、解壓縮至倒置的 DIB，或將來源和目的地矩形所描述的影像解壓縮。
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- ICM_DECOMPRESSEX message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025365"
---
# <a name="icm_decompressex-message"></a><span data-ttu-id="2b81e-104">ICM \_ DECOMPRESSEX 訊息</span><span class="sxs-lookup"><span data-stu-id="2b81e-104">ICM\_DECOMPRESSEX message</span></span>

<span data-ttu-id="2b81e-105">**ICM \_ DECOMPRESSEX** 訊息會通知影片壓縮驅動程式將資料框架直接解壓縮至螢幕、解壓縮至倒置的 DIB，或將來源和目的地矩形所描述的影像解壓縮。</span><span class="sxs-lookup"><span data-stu-id="2b81e-105">The **ICM\_DECOMPRESSEX** message notifies a video compression driver to decompress a frame of data directly to the screen, decompress to an upside-down DIB, or decompress images described with source and destination rectangles.</span></span>


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="2b81e-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b81e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b81e-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="2b81e-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="2b81e-108">[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2b81e-108">Pointer to an [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2b81e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b81e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2b81e-110">[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2b81e-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b81e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b81e-111">Return Value</span></span>

<span data-ttu-id="2b81e-112">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2b81e-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b81e-113">備註</span><span class="sxs-lookup"><span data-stu-id="2b81e-113">Remarks</span></span>

<span data-ttu-id="2b81e-114">這則訊息與 [**ICM \_ 解壓縮**](icm-decompress.md) 類似，不同之處在于它會使用 [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) 結構來定義其解壓縮資訊。</span><span class="sxs-lookup"><span data-stu-id="2b81e-114">This message is similar to [**ICM\_DECOMPRESS**](icm-decompress.md) except that it uses the [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure to define its decompression information.</span></span>

<span data-ttu-id="2b81e-115">如果您希望驅動程式將資料直接解壓縮到畫面，請傳送 [**ICM \_ 繪製**](icm-draw.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="2b81e-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="2b81e-116">如果在 [**ICM \_ DECOMPRESSEX \_ 開始**](icm-decompressex-begin.md) 訊息之前收到此訊息，驅動程式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2b81e-116">The driver returns an error if this message is received before the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b81e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b81e-117">Requirements</span></span>



| <span data-ttu-id="2b81e-118">需求</span><span class="sxs-lookup"><span data-stu-id="2b81e-118">Requirement</span></span> | <span data-ttu-id="2b81e-119">值</span><span class="sxs-lookup"><span data-stu-id="2b81e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2b81e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b81e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2b81e-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b81e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2b81e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b81e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2b81e-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b81e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2b81e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2b81e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b81e-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b81e-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b81e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b81e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b81e-127">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="2b81e-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2b81e-128">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="2b81e-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





