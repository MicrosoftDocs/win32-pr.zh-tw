---
title: 'ICM_DECOMPRESS_GET_FORMAT 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 取得格式訊息會向 \_ 影片解壓縮驅動程式要求解壓縮資料的輸出格式。 您可以使用 ICDecompressGetFormat 宏明確地傳送此訊息。
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- ICM_DECOMPRESS_GET_FORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7eefa655646deae8e67fa16a87bfdb81a8b936
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025368"
---
# <a name="icm_decompress_get_format-message"></a><span data-ttu-id="0fca8-105">ICM \_ 解壓縮 \_ 取得 \_ 格式訊息</span><span class="sxs-lookup"><span data-stu-id="0fca8-105">ICM\_DECOMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="0fca8-106">**ICM \_ 解壓縮 \_ 取得 \_ 格式** 訊息會向影片解壓縮驅動程式要求解壓縮資料的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="0fca8-106">The **ICM\_DECOMPRESS\_GET\_FORMAT** message requests the output format of the decompressed data from a video decompression driver.</span></span> <span data-ttu-id="0fca8-107">您可以使用 [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0fca8-107">You can send this message explicitly or by using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="0fca8-108">參數</span><span class="sxs-lookup"><span data-stu-id="0fca8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fca8-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="0fca8-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="0fca8-110">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="0fca8-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="0fca8-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="0fca8-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="0fca8-112">要包含輸出格式之 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0fca8-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="0fca8-113">您可以指定零來要求輸出格式的大小，如同在 [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) 宏中一樣。</span><span class="sxs-lookup"><span data-stu-id="0fca8-113">You can specify zero to request only the size of the output format, as in the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fca8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fca8-114">Return Value</span></span>

<span data-ttu-id="0fca8-115">如果 *lpbiOutput* 為零，則會傳回結構的大小。</span><span class="sxs-lookup"><span data-stu-id="0fca8-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="0fca8-116">如果 *lpbiOutput* 為非零值，則會 \_ 在成功時傳回 ICERR OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0fca8-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fca8-117">備註</span><span class="sxs-lookup"><span data-stu-id="0fca8-117">Remarks</span></span>

<span data-ttu-id="0fca8-118">如果 *lpbiOutput* 為非零值，則驅動程式應該以對應至針對 *lpbiInput* 指定之輸入格式的預設輸出格式來填滿 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構。</span><span class="sxs-lookup"><span data-stu-id="0fca8-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="0fca8-119">如果壓縮程式可能會產生數種格式，預設格式應該是保留最大量資訊的格式。</span><span class="sxs-lookup"><span data-stu-id="0fca8-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fca8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fca8-120">Requirements</span></span>



| <span data-ttu-id="0fca8-121">需求</span><span class="sxs-lookup"><span data-stu-id="0fca8-121">Requirement</span></span> | <span data-ttu-id="0fca8-122">值</span><span class="sxs-lookup"><span data-stu-id="0fca8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0fca8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fca8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0fca8-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fca8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0fca8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fca8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0fca8-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fca8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0fca8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0fca8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fca8-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="0fca8-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fca8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fca8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fca8-130">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="0fca8-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0fca8-131">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="0fca8-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

