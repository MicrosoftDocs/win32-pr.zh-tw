---
title: 'ICM_COMPRESS_QUERY 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 查詢訊息會查詢視訊壓縮驅動程式，以判斷它是否支援特定輸入格式，或是否可以將特定的輸入格式壓縮成特定的輸出格式。
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- ICM_COMPRESS_QUERY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969198"
---
# <a name="icm_compress_query-message"></a><span data-ttu-id="2a47c-104">ICM \_ 壓縮 \_ 查詢訊息</span><span class="sxs-lookup"><span data-stu-id="2a47c-104">ICM\_COMPRESS\_QUERY message</span></span>

<span data-ttu-id="2a47c-105">**ICM \_ 壓縮 \_ 查詢** 訊息會查詢視訊壓縮驅動程式，以判斷它是否支援特定輸入格式，或是否可以將特定的輸入格式壓縮成特定的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="2a47c-105">The **ICM\_COMPRESS\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format.</span></span> <span data-ttu-id="2a47c-106">您可以使用 [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2a47c-106">You can send this message explicitly or by using the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro.</span></span>


```C++
ICM_COMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="2a47c-107">參數</span><span class="sxs-lookup"><span data-stu-id="2a47c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a47c-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="2a47c-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="2a47c-109">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="2a47c-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="2a47c-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="2a47c-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="2a47c-111">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸出格式。</span><span class="sxs-lookup"><span data-stu-id="2a47c-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="2a47c-112">您可以為此參數指定零，以表示可接受任何輸出格式。</span><span class="sxs-lookup"><span data-stu-id="2a47c-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a47c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a47c-113">Return Value</span></span>

<span data-ttu-id="2a47c-114">\_如果支援指定的壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK （否則為） \_ 。</span><span class="sxs-lookup"><span data-stu-id="2a47c-114">Returns ICERR\_OK if the specified compression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a47c-115">備註</span><span class="sxs-lookup"><span data-stu-id="2a47c-115">Remarks</span></span>

<span data-ttu-id="2a47c-116">當驅動程式收到此訊息時，它應該會檢查與 *lpbiInput* 相關聯的 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構，以判斷它是否可以壓縮輸入格式。</span><span class="sxs-lookup"><span data-stu-id="2a47c-116">When a driver receives this message, it should examine the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure associated with *lpbiInput* to determine if it can compress the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a47c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a47c-117">Requirements</span></span>



| <span data-ttu-id="2a47c-118">需求</span><span class="sxs-lookup"><span data-stu-id="2a47c-118">Requirement</span></span> | <span data-ttu-id="2a47c-119">值</span><span class="sxs-lookup"><span data-stu-id="2a47c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a47c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a47c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a47c-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a47c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2a47c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a47c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a47c-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a47c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2a47c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2a47c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a47c-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a47c-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a47c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a47c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a47c-127">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="2a47c-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2a47c-128">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="2a47c-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

