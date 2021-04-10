---
title: 'ICM_COMPRESS_GET_SIZE 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 取得 \_ 大小訊息要求當壓縮成指定的輸出格式時，影片壓縮驅動程式會提供一個資料框架的大小上限。 您可以使用 ICCompressGetSize 宏明確地傳送此訊息。
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934882"
---
# <a name="icm_compress_get_size-message"></a><span data-ttu-id="15aaa-105">ICM \_ 壓縮 \_ 取得 \_ 大小訊息</span><span class="sxs-lookup"><span data-stu-id="15aaa-105">ICM\_COMPRESS\_GET\_SIZE message</span></span>

<span data-ttu-id="15aaa-106">**ICM \_ 壓縮 \_ 取得 \_ 大小** 訊息要求當壓縮成指定的輸出格式時，影片壓縮驅動程式會提供一個資料框架的大小上限。</span><span class="sxs-lookup"><span data-stu-id="15aaa-106">The **ICM\_COMPRESS\_GET\_SIZE** message requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format.</span></span> <span data-ttu-id="15aaa-107">您可以使用 [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="15aaa-107">You can send this message explicitly or by using the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro.</span></span>


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="15aaa-108">參數</span><span class="sxs-lookup"><span data-stu-id="15aaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15aaa-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="15aaa-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="15aaa-110">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="15aaa-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="15aaa-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="15aaa-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="15aaa-112">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸出格式。</span><span class="sxs-lookup"><span data-stu-id="15aaa-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15aaa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="15aaa-113">Return Value</span></span>

<span data-ttu-id="15aaa-114">傳回單一壓縮框架可佔用的位元組數目上限。</span><span class="sxs-lookup"><span data-stu-id="15aaa-114">Returns the maximum number of bytes a single compressed frame can occupy.</span></span>

## <a name="remarks"></a><span data-ttu-id="15aaa-115">備註</span><span class="sxs-lookup"><span data-stu-id="15aaa-115">Remarks</span></span>

<span data-ttu-id="15aaa-116">一般而言，應用程式會傳送此訊息，以判斷要為壓縮框架配置的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="15aaa-116">Typically, applications send this message to determine how large a buffer to allocate for the compressed frame.</span></span>

<span data-ttu-id="15aaa-117">驅動程式應根據輸入和輸出格式來計算最大可能框架的大小。</span><span class="sxs-lookup"><span data-stu-id="15aaa-117">The driver should calculate the size of the largest possible frame based on the input and output formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="15aaa-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="15aaa-118">Requirements</span></span>



| <span data-ttu-id="15aaa-119">需求</span><span class="sxs-lookup"><span data-stu-id="15aaa-119">Requirement</span></span> | <span data-ttu-id="15aaa-120">值</span><span class="sxs-lookup"><span data-stu-id="15aaa-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15aaa-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15aaa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15aaa-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15aaa-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="15aaa-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15aaa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15aaa-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15aaa-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="15aaa-125">標頭</span><span class="sxs-lookup"><span data-stu-id="15aaa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15aaa-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="15aaa-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15aaa-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15aaa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15aaa-128">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="15aaa-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="15aaa-129">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="15aaa-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

