---
title: 'ICM_DECOMPRESSEX_BEGIN 訊息 (Vfw .h) '
description: ICM \_ DECOMPRESSEX \_ 開始訊息會通知影片壓縮驅動程式準備將資料解壓縮。
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686271"
---
# <a name="icm_decompressex_begin-message"></a><span data-ttu-id="44fe7-104">ICM \_ DECOMPRESSEX \_ 開始訊息</span><span class="sxs-lookup"><span data-stu-id="44fe7-104">ICM\_DECOMPRESSEX\_BEGIN message</span></span>

<span data-ttu-id="44fe7-105">**ICM \_ DECOMPRESSEX \_ 開始** 訊息會通知影片壓縮驅動程式準備將資料解壓縮。</span><span class="sxs-lookup"><span data-stu-id="44fe7-105">The **ICM\_DECOMPRESSEX\_BEGIN** message notifies a video compression driver to prepare to decompress data.</span></span>


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="44fe7-106">參數</span><span class="sxs-lookup"><span data-stu-id="44fe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44fe7-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="44fe7-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="44fe7-108">[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)結構的指標，其中包含輸入和輸出格式。</span><span class="sxs-lookup"><span data-stu-id="44fe7-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input and output formats.</span></span>

</dd> <dt>

<span data-ttu-id="44fe7-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="44fe7-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="44fe7-110">[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="44fe7-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44fe7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="44fe7-111">Return Value</span></span>

<span data-ttu-id="44fe7-112">\_如果支援指定的解壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK （否則為） \_ 。</span><span class="sxs-lookup"><span data-stu-id="44fe7-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="44fe7-113">備註</span><span class="sxs-lookup"><span data-stu-id="44fe7-113">Remarks</span></span>

<span data-ttu-id="44fe7-114">當驅動程式收到此訊息時，它應該配置緩衝區，並進行任何耗時的作業，讓它能夠有效率地處理 [**ICM \_ DECOMPRESSEX**](icm-decompressex.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="44fe7-114">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESSEX**](icm-decompressex.md) messages efficiently.</span></span>

<span data-ttu-id="44fe7-115">如果您希望驅動程式將資料直接解壓縮到畫面，請傳送 [**ICM \_ DRAW \_ 開始**](icm-draw-begin.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="44fe7-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="44fe7-116">**Icm \_ DECOMPRESSEX \_ BEGIN** 和 [**icm \_ DECOMPRESSEX \_ END**](icm-decompressex-end.md)訊息不會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="44fe7-116">The **ICM\_DECOMPRESSEX\_BEGIN** and [**ICM\_DECOMPRESSEX\_END**](icm-decompressex-end.md) messages do not nest.</span></span> <span data-ttu-id="44fe7-117">如果您的驅動程式收到 Icm DECOMPRESSEX 在使用 **icm \_ DECOMPRESSEX \_ END** 停止解壓縮之前 **\_ \_ 開始**，則應該以新的參數重新開機解壓縮。</span><span class="sxs-lookup"><span data-stu-id="44fe7-117">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="44fe7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="44fe7-118">Requirements</span></span>



| <span data-ttu-id="44fe7-119">需求</span><span class="sxs-lookup"><span data-stu-id="44fe7-119">Requirement</span></span> | <span data-ttu-id="44fe7-120">值</span><span class="sxs-lookup"><span data-stu-id="44fe7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="44fe7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44fe7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44fe7-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44fe7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="44fe7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44fe7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44fe7-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44fe7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="44fe7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="44fe7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="44fe7-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="44fe7-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44fe7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44fe7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fe7-128">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="44fe7-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="44fe7-129">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="44fe7-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





