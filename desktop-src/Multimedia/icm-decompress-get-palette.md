---
title: 'ICM_DECOMPRESS_GET_PALETTE 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 取得 \_ 調色板訊息要求影片解壓縮驅動程式提供輸出 BITMAPINFOHEADER 結構的色彩表。 您可以使用 ICDecompressGetPalette 宏明確地傳送此訊息。
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- ICM_DECOMPRESS_GET_PALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998024"
---
# <a name="icm_decompress_get_palette-message"></a><span data-ttu-id="8d40e-105">ICM \_ 解壓縮 \_ 取得 \_ 選用區訊息</span><span class="sxs-lookup"><span data-stu-id="8d40e-105">ICM\_DECOMPRESS\_GET\_PALETTE message</span></span>

<span data-ttu-id="8d40e-106">**ICM \_ 解壓縮 \_ 取得 \_ 調色板** 訊息要求影片解壓縮驅動程式提供輸出 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))結構的色彩表。</span><span class="sxs-lookup"><span data-stu-id="8d40e-106">The **ICM\_DECOMPRESS\_GET\_PALETTE** message requests that the video decompression driver supply the color table of the output [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure.</span></span> <span data-ttu-id="8d40e-107">您可以使用 [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8d40e-107">You can send this message explicitly or by using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="8d40e-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d40e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d40e-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="8d40e-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="8d40e-110">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="8d40e-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="8d40e-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="8d40e-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="8d40e-112">要包含色彩表之 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8d40e-112">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure to contain the color table.</span></span> <span data-ttu-id="8d40e-113">為色彩表保留的空間一律為至少256的色彩。</span><span class="sxs-lookup"><span data-stu-id="8d40e-113">The space reserved for the color table is always at least 256 colors.</span></span> <span data-ttu-id="8d40e-114">您可以為此參數指定零，只傳回色彩表的大小。</span><span class="sxs-lookup"><span data-stu-id="8d40e-114">You can specify zero for this parameter to return only the size of the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d40e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d40e-115">Return Value</span></span>

<span data-ttu-id="8d40e-116">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8d40e-116">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d40e-117">備註</span><span class="sxs-lookup"><span data-stu-id="8d40e-117">Remarks</span></span>

<span data-ttu-id="8d40e-118">如果 *lpbiOutput* 為非零值，驅動程式會將 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))的 **biClrUsed** 成員設定為 color 資料表中的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="8d40e-118">If *lpbiOutput* is nonzero, the driver sets the **biClrUsed** member of [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) to the number of colors in the color table.</span></span> <span data-ttu-id="8d40e-119">驅動程式會以實際的色彩填滿 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)的 **bmiColors** 成員。</span><span class="sxs-lookup"><span data-stu-id="8d40e-119">The driver fills the **bmiColors** member of [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) with the actual colors.</span></span>

<span data-ttu-id="8d40e-120">驅動程式只有在使用輸入格式所指定的調色板時，才應該支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="8d40e-120">The driver should support this message only if it uses a palette other than the one specified in the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d40e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d40e-121">Requirements</span></span>



| <span data-ttu-id="8d40e-122">需求</span><span class="sxs-lookup"><span data-stu-id="8d40e-122">Requirement</span></span> | <span data-ttu-id="8d40e-123">值</span><span class="sxs-lookup"><span data-stu-id="8d40e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8d40e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d40e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8d40e-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d40e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8d40e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d40e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8d40e-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d40e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8d40e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="8d40e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d40e-129"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d40e-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d40e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d40e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d40e-131">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="8d40e-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8d40e-132">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="8d40e-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

