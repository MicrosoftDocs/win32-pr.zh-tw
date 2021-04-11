---
title: 'ICM_DECOMPRESS_BEGIN 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 開始訊息會通知影片解壓縮驅動程式準備將資料解壓縮。 您可以使用 ICDecompressBegin 宏明確地傳送此訊息。
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105437"
---
# <a name="icm_decompress_begin-message"></a><span data-ttu-id="a2dac-105">ICM \_ 解壓縮 \_ 開始訊息</span><span class="sxs-lookup"><span data-stu-id="a2dac-105">ICM\_DECOMPRESS\_BEGIN message</span></span>

<span data-ttu-id="a2dac-106">**ICM \_ 解壓縮 \_ 開始** 訊息會通知影片解壓縮驅動程式準備將資料解壓縮。</span><span class="sxs-lookup"><span data-stu-id="a2dac-106">The **ICM\_DECOMPRESS\_BEGIN** message notifies a video decompression driver to prepare to decompress data.</span></span> <span data-ttu-id="a2dac-107">您可以使用 [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a2dac-107">You can send this message explicitly or by using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro.</span></span>


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="a2dac-108">參數</span><span class="sxs-lookup"><span data-stu-id="a2dac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2dac-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="a2dac-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="a2dac-110">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="a2dac-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="a2dac-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="a2dac-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="a2dac-112">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸出格式。</span><span class="sxs-lookup"><span data-stu-id="a2dac-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2dac-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2dac-113">Return Value</span></span>

<span data-ttu-id="a2dac-114">\_如果支援指定的解壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK （否則為） \_ 。</span><span class="sxs-lookup"><span data-stu-id="a2dac-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2dac-115">備註</span><span class="sxs-lookup"><span data-stu-id="a2dac-115">Remarks</span></span>

<span data-ttu-id="a2dac-116">當驅動程式收到此訊息時，它應該配置緩衝區，並進行任何耗時的作業，以便能夠有效率地處理 [**ICM 的 \_ 解壓縮**](icm-decompress.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="a2dac-116">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESS**](icm-decompress.md) messages efficiently.</span></span>

<span data-ttu-id="a2dac-117">如果您希望驅動程式將資料直接解壓縮到畫面，請傳送 [**ICM \_ 繪製**](icm-draw.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="a2dac-117">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="a2dac-118">**Icm \_ 解壓縮 \_ 開始** 和 [**icm \_ 解壓縮 \_ 結束**](icm-decompress-end.md)訊息不會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="a2dac-118">The **ICM\_DECOMPRESS\_BEGIN** and [**ICM\_DECOMPRESS\_END**](icm-decompress-end.md) messages do not nest.</span></span> <span data-ttu-id="a2dac-119">如果您的驅動程式在使用 **icm \_ 解壓縮 \_ 結束** 解壓縮之前收到 **icm \_ 解壓縮 \_** ，則應該以新的參數重新開機解壓縮。</span><span class="sxs-lookup"><span data-stu-id="a2dac-119">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2dac-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2dac-120">Requirements</span></span>



| <span data-ttu-id="a2dac-121">需求</span><span class="sxs-lookup"><span data-stu-id="a2dac-121">Requirement</span></span> | <span data-ttu-id="a2dac-122">值</span><span class="sxs-lookup"><span data-stu-id="a2dac-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a2dac-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2dac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2dac-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2dac-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a2dac-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2dac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2dac-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2dac-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a2dac-127">標頭</span><span class="sxs-lookup"><span data-stu-id="a2dac-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2dac-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2dac-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2dac-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2dac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2dac-130">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="a2dac-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a2dac-131">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="a2dac-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

