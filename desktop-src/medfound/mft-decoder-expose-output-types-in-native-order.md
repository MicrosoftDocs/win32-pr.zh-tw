---
description: 指定解碼器是否公開 IYUV/I420 輸出類型 (適用于其他格式之前的轉碼) 。
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: 'MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692316"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a><span data-ttu-id="c2715-103">MFT \_ 解碼 \_ 會 \_ \_ \_ 以 \_ 原生 \_ 順序屬性公開輸出類型</span><span class="sxs-lookup"><span data-stu-id="c2715-103">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER attribute</span></span>

<span data-ttu-id="c2715-104">指定解碼器是否公開 IYUV/I420 輸出類型 (適用于其他格式之前的轉碼) 。</span><span class="sxs-lookup"><span data-stu-id="c2715-104">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2715-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c2715-105">Data type</span></span>

<span data-ttu-id="c2715-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c2715-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c2715-107">備註</span><span class="sxs-lookup"><span data-stu-id="c2715-107">Remarks</span></span>

<span data-ttu-id="c2715-108">這個屬性（attribute）是一種提示，可讓您根據預期的使用方式（播放或轉碼），以特定順序排列其輸出類型清單。</span><span class="sxs-lookup"><span data-stu-id="c2715-108">This attribute is a hint for the decoder to arrange its list of output types in a particular order, depending on the intended use, either playback or transcode.</span></span>

<span data-ttu-id="c2715-109">針對大部分的編碼格式 (h.264、MPEG-2、WMV) 、Microsoft 媒體基礎中的影片編碼器支援數個常見的 YUV 輸出，包括 NV12、YV12、YUY2、IYUV 和 I420。</span><span class="sxs-lookup"><span data-stu-id="c2715-109">For most encoding formats (H.264, MPEG-2, WMV), the video decoders in Microsoft Media Foundation support several common YUV outputs, including NV12, YV12, YUY2, IYUV, and I420.</span></span> <span data-ttu-id="c2715-110">此解碼器會透過其 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法，提供輸出類型的排序清單。</span><span class="sxs-lookup"><span data-stu-id="c2715-110">The decoder offers an ordered list of output types through its [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

<span data-ttu-id="c2715-111">針對播放，NV12 是最有效率且廣泛支援的格式。</span><span class="sxs-lookup"><span data-stu-id="c2715-111">For playback, NV12 is the most efficient and widely supported format.</span></span> <span data-ttu-id="c2715-112">因此，根據預設，解碼器通常會提供 NV12 做為清單中的第一個輸出類型。</span><span class="sxs-lookup"><span data-stu-id="c2715-112">Therefore, by default, decoders typically offer NV12 as the first output type in the list.</span></span> <span data-ttu-id="c2715-113">這可將在建立播放拓撲時解析媒體類型所需的時間降至最低。</span><span class="sxs-lookup"><span data-stu-id="c2715-113">This minimizes the time needed to resolve the media type when building a playback topology.</span></span> <span data-ttu-id="c2715-114">不過，針對轉碼，IYUV 或 I420 對於 CPU 來說更有效率，而且通常是由編碼器所偏好。</span><span class="sxs-lookup"><span data-stu-id="c2715-114">For transcoding, however, IYUV or I420 are more efficient for the CPU and are typically preferred by encoders.</span></span>

<span data-ttu-id="c2715-115">如果解碼器支援這個屬性，屬性就會有下列行為：</span><span class="sxs-lookup"><span data-stu-id="c2715-115">If a decoder supports this attribute, the attribute has the following behavior:</span></span>

-   <span data-ttu-id="c2715-116">如果屬性具有非零值，則 IYUV 和 I420 會先出現在輸出媒體類型清單中。</span><span class="sxs-lookup"><span data-stu-id="c2715-116">If the attribute has a non-zero value, IYUV and I420 appear first in the list of output media types.</span></span> <span data-ttu-id="c2715-117">這項設定最有效率的轉碼。</span><span class="sxs-lookup"><span data-stu-id="c2715-117">This setting is most efficient for transcoding.</span></span>
-   <span data-ttu-id="c2715-118">如果屬性為零，NV12 會先出現在輸出媒體類型清單中。</span><span class="sxs-lookup"><span data-stu-id="c2715-118">If the attribute is zero, NV12 appears first in the list of output media types.</span></span> <span data-ttu-id="c2715-119">這項設定最適合用來播放，而且是預設值。</span><span class="sxs-lookup"><span data-stu-id="c2715-119">This setting is most efficient for playback, and is the default.</span></span>

<span data-ttu-id="c2715-120">若要設定此屬性：</span><span class="sxs-lookup"><span data-stu-id="c2715-120">To set this attribute:</span></span>

1.  <span data-ttu-id="c2715-121">在解碼器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="c2715-121">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="c2715-122">呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 以加入屬性。</span><span class="sxs-lookup"><span data-stu-id="c2715-122">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2715-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2715-123">Requirements</span></span>



| <span data-ttu-id="c2715-124">需求</span><span class="sxs-lookup"><span data-stu-id="c2715-124">Requirement</span></span> | <span data-ttu-id="c2715-125">值</span><span class="sxs-lookup"><span data-stu-id="c2715-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2715-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2715-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c2715-127">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2715-127">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c2715-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2715-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c2715-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="c2715-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c2715-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c2715-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2715-131"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2715-131"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2715-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2715-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2715-133">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c2715-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




