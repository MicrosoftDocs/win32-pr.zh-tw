---
title: 'ICM_DECOMPRESS_QUERY 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 查詢訊息會查詢影片解壓縮驅動程式，以判斷它是否支援特定輸入格式，或是否可以將特定的輸入格式解壓縮至特定的輸出格式。
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- ICM_DECOMPRESS_QUERY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968783"
---
# <a name="icm_decompress_query-message"></a><span data-ttu-id="afa44-104">ICM \_ 解壓縮 \_ 查詢訊息</span><span class="sxs-lookup"><span data-stu-id="afa44-104">ICM\_DECOMPRESS\_QUERY message</span></span>

<span data-ttu-id="afa44-105">**ICM \_ 解壓縮 \_ 查詢** 訊息會查詢影片解壓縮驅動程式，以判斷它是否支援特定輸入格式，或是否可以將特定的輸入格式解壓縮至特定的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="afa44-105">The **ICM\_DECOMPRESS\_QUERY** message queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span> <span data-ttu-id="afa44-106">您可以使用 [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="afa44-106">You can send this message explicitly or by using the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro.</span></span>


```C++
ICM_DECOMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="afa44-107">參數</span><span class="sxs-lookup"><span data-stu-id="afa44-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afa44-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="afa44-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="afa44-109">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="afa44-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="afa44-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="afa44-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="afa44-111">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸出格式。</span><span class="sxs-lookup"><span data-stu-id="afa44-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="afa44-112">您可以為此參數指定零，以表示可接受任何輸出格式。</span><span class="sxs-lookup"><span data-stu-id="afa44-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afa44-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="afa44-113">Return Value</span></span>

<span data-ttu-id="afa44-114">\_如果支援指定的解壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK （否則為） \_ 。</span><span class="sxs-lookup"><span data-stu-id="afa44-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="afa44-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="afa44-115">Requirements</span></span>



| <span data-ttu-id="afa44-116">需求</span><span class="sxs-lookup"><span data-stu-id="afa44-116">Requirement</span></span> | <span data-ttu-id="afa44-117">值</span><span class="sxs-lookup"><span data-stu-id="afa44-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="afa44-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afa44-118">Minimum supported client</span></span><br/> | <span data-ttu-id="afa44-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afa44-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="afa44-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afa44-120">Minimum supported server</span></span><br/> | <span data-ttu-id="afa44-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afa44-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="afa44-122">標頭</span><span class="sxs-lookup"><span data-stu-id="afa44-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="afa44-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="afa44-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afa44-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afa44-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa44-125">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="afa44-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="afa44-126">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="afa44-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

