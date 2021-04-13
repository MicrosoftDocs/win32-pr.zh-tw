---
title: 'ICM_COMPRESS_GET_FORMAT 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 取得格式訊息會向 \_ 視訊壓縮驅動程式要求壓縮資料的輸出格式。 您可以使用 ICCompressGetFormat 宏明確地傳送此訊息。
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- ICM_COMPRESS_GET_FORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466476"
---
# <a name="icm_compress_get_format-message"></a><span data-ttu-id="92cec-105">ICM \_ 壓縮 \_ 取得 \_ 格式訊息</span><span class="sxs-lookup"><span data-stu-id="92cec-105">ICM\_COMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="92cec-106">**ICM \_ 壓縮 \_ 取得 \_ 格式** 訊息會向視訊壓縮驅動程式要求壓縮資料的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="92cec-106">The **ICM\_COMPRESS\_GET\_FORMAT** message requests the output format of the compressed data from a video compression driver.</span></span> <span data-ttu-id="92cec-107">您可以使用 [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="92cec-107">You can send this message explicitly or by using the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) macro.</span></span>


```C++
ICM_COMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="92cec-108">參數</span><span class="sxs-lookup"><span data-stu-id="92cec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92cec-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="92cec-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="92cec-110">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="92cec-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="92cec-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="92cec-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="92cec-112">要包含輸出格式之 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="92cec-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="92cec-113">您可以為此參數指定零，以要求輸出格式的大小，如同在 [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) 宏中一樣。</span><span class="sxs-lookup"><span data-stu-id="92cec-113">You can specify zero for this parameter to request only the size of the output format, as in the [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92cec-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="92cec-114">Return Value</span></span>

<span data-ttu-id="92cec-115">如果 *lpbiOutput* 為零，則會傳回結構的大小。</span><span class="sxs-lookup"><span data-stu-id="92cec-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="92cec-116">如果 *lpbiOutput* 為非零值，則會 \_ 在成功時傳回 ICERR OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="92cec-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="92cec-117">備註</span><span class="sxs-lookup"><span data-stu-id="92cec-117">Remarks</span></span>

<span data-ttu-id="92cec-118">如果 *lpbiOutput* 為非零值，則驅動程式應該以對應至針對 *lpbiInput* 指定之輸入格式的預設輸出格式來填滿 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構。</span><span class="sxs-lookup"><span data-stu-id="92cec-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="92cec-119">如果壓縮程式可能會產生數種格式，預設格式應該是保留最大量資訊的格式。</span><span class="sxs-lookup"><span data-stu-id="92cec-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="92cec-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="92cec-120">Requirements</span></span>



| <span data-ttu-id="92cec-121">需求</span><span class="sxs-lookup"><span data-stu-id="92cec-121">Requirement</span></span> | <span data-ttu-id="92cec-122">值</span><span class="sxs-lookup"><span data-stu-id="92cec-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="92cec-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92cec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="92cec-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92cec-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="92cec-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92cec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="92cec-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92cec-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="92cec-127">標頭</span><span class="sxs-lookup"><span data-stu-id="92cec-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="92cec-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="92cec-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92cec-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92cec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92cec-130">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="92cec-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="92cec-131">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="92cec-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

