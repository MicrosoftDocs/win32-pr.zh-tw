---
title: 'ICM_DECOMPRESS_SET_PALETTE 訊息 (Vfw .h) '
description: 如果要 \_ 將 \_ \_ 影片解壓縮驅動程式解壓縮至使用調色板的格式，請使用 ICM 解壓縮設定的選擇區訊息。 您可以使用 ICDecompressSetPalette 宏明確地傳送此訊息。
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- ICM_DECOMPRESS_SET_PALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967558"
---
# <a name="icm_decompress_set_palette-message"></a><span data-ttu-id="36537-105">ICM \_ 解壓縮 \_ 設定的 \_ 調色板訊息</span><span class="sxs-lookup"><span data-stu-id="36537-105">ICM\_DECOMPRESS\_SET\_PALETTE message</span></span>

<span data-ttu-id="36537-106">如果要將影片解壓縮驅動程式解壓縮至使用調色板的格式，請使用 **ICM \_ 解壓縮 \_ 設定 \_** 的選擇區訊息。</span><span class="sxs-lookup"><span data-stu-id="36537-106">The **ICM\_DECOMPRESS\_SET\_PALETTE** message specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette.</span></span> <span data-ttu-id="36537-107">您可以使用 [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="36537-107">You can send this message explicitly or by using the [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="36537-108">參數</span><span class="sxs-lookup"><span data-stu-id="36537-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36537-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span><span class="sxs-lookup"><span data-stu-id="36537-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span></span>
</dt> <dd>

<span data-ttu-id="36537-110">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))結構的指標，其色彩表包含應該盡可能使用的色彩。</span><span class="sxs-lookup"><span data-stu-id="36537-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure whose color table contains the colors that should be used if possible.</span></span> <span data-ttu-id="36537-111">您可以指定零來使用一組預設的輸出色彩。</span><span class="sxs-lookup"><span data-stu-id="36537-111">You can specify zero to use the default set of output colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36537-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="36537-112">Return Value</span></span>

<span data-ttu-id="36537-113">\_如果解壓縮驅動程式可以精確地將影像解壓縮至建議的調色板，請使用在選擇區中排列的色彩集合，以進行 ICERR 確定。</span><span class="sxs-lookup"><span data-stu-id="36537-113">Returns ICERR\_OK if the decompression driver can precisely decompress images to the suggested palette using the set of colors as they are arranged in the palette.</span></span> <span data-ttu-id="36537-114">否則會傳回 \_ 不支援的 ICERR。</span><span class="sxs-lookup"><span data-stu-id="36537-114">Returns ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="36537-115">備註</span><span class="sxs-lookup"><span data-stu-id="36537-115">Remarks</span></span>

<span data-ttu-id="36537-116">此訊息不會影響正在進行的解壓縮;相反地，應該傳回使用此訊息傳遞的色彩，以回應未來的 [**ICM \_ 解壓縮 \_ 取得 \_ 格式**](icm-decompress-get-format.md) 和 [**ICM \_ 解壓縮 \_ 取得 \_**](icm-decompress-get-palette.md) 選擇區訊息。</span><span class="sxs-lookup"><span data-stu-id="36537-116">This message should not affect decompression already in progress; rather, colors passed using this message should be returned in response to future [**ICM\_DECOMPRESS\_GET\_FORMAT**](icm-decompress-get-format.md) and [**ICM\_DECOMPRESS\_GET\_PALETTE**](icm-decompress-get-palette.md) messages.</span></span> <span data-ttu-id="36537-117">在未來的 [**ICM \_ 解壓縮 \_ 開始**](icm-decompress-begin.md) 訊息中，色彩會傳送回解壓縮驅動程式。</span><span class="sxs-lookup"><span data-stu-id="36537-117">Colors are sent back to the decompression driver in a future [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="36537-118">此訊息主要是在驅動程式將影像解壓縮至螢幕，而另一個使用調色板的應用程式在前景時使用，以強制解壓縮驅動程式適應一組外部的色彩。</span><span class="sxs-lookup"><span data-stu-id="36537-118">This message is used primarily when a driver decompresses images to the screen and another application that uses a palette is in the foreground, forcing the decompression driver to adapt to a foreign set of colors.</span></span>

## <a name="requirements"></a><span data-ttu-id="36537-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="36537-119">Requirements</span></span>



| <span data-ttu-id="36537-120">需求</span><span class="sxs-lookup"><span data-stu-id="36537-120">Requirement</span></span> | <span data-ttu-id="36537-121">值</span><span class="sxs-lookup"><span data-stu-id="36537-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36537-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36537-122">Minimum supported client</span></span><br/> | <span data-ttu-id="36537-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36537-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="36537-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36537-124">Minimum supported server</span></span><br/> | <span data-ttu-id="36537-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36537-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="36537-126">標頭</span><span class="sxs-lookup"><span data-stu-id="36537-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="36537-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="36537-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36537-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36537-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36537-129">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="36537-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="36537-130">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="36537-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

