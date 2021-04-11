---
title: 'ICM_DECOMPRESSEX_QUERY 訊息 (Vfw .h) '
description: ICM \_ DECOMPRESSEX \_ 查詢訊息會查詢視訊壓縮驅動程式，以判斷它是否支援特定輸入格式，或是否可將特定輸入格式解壓縮至特定的輸出格式。
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- ICM_DECOMPRESSEX_QUERY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844068"
---
# <a name="icm_decompressex_query-message"></a><span data-ttu-id="8cb7b-104">ICM \_ DECOMPRESSEX \_ 查詢訊息</span><span class="sxs-lookup"><span data-stu-id="8cb7b-104">ICM\_DECOMPRESSEX\_QUERY message</span></span>

<span data-ttu-id="8cb7b-105">**ICM \_ DECOMPRESSEX \_ 查詢** 訊息會查詢視訊壓縮驅動程式，以判斷它是否支援特定輸入格式，或是否可將特定輸入格式解壓縮至特定的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="8cb7b-105">The **ICM\_DECOMPRESSEX\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span>


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="8cb7b-106">參數</span><span class="sxs-lookup"><span data-stu-id="8cb7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cb7b-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="8cb7b-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="8cb7b-108">[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="8cb7b-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="8cb7b-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cb7b-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8cb7b-110">[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8cb7b-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cb7b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cb7b-111">Return Value</span></span>

<span data-ttu-id="8cb7b-112">\_如果支援指定的解壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK （否則為） \_ 。</span><span class="sxs-lookup"><span data-stu-id="8cb7b-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cb7b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8cb7b-113">Requirements</span></span>



| <span data-ttu-id="8cb7b-114">需求</span><span class="sxs-lookup"><span data-stu-id="8cb7b-114">Requirement</span></span> | <span data-ttu-id="8cb7b-115">值</span><span class="sxs-lookup"><span data-stu-id="8cb7b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8cb7b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8cb7b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb7b-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8cb7b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8cb7b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8cb7b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb7b-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8cb7b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8cb7b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8cb7b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cb7b-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="8cb7b-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cb7b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cb7b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb7b-123">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="8cb7b-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8cb7b-124">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="8cb7b-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





