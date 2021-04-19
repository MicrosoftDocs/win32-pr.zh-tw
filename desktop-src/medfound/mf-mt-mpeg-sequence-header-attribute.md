---
description: 包含適用于影片媒體類型的 MPEG-2 或 MPEG-2 序列標頭。
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: 'MF_MT_MPEG_SEQUENCE_HEADER 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997550"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a><span data-ttu-id="f4385-103">MF \_ MT \_ MPEG \_ SEQUENCE \_ 標頭屬性</span><span class="sxs-lookup"><span data-stu-id="f4385-103">MF\_MT\_MPEG\_SEQUENCE\_HEADER attribute</span></span>

<span data-ttu-id="f4385-104">包含適用于影片媒體類型的 MPEG-2 或 MPEG-2 序列標頭。</span><span class="sxs-lookup"><span data-stu-id="f4385-104">Contains the MPEG-1 or MPEG-2 sequence header for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="f4385-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f4385-105">Data type</span></span>

<span data-ttu-id="f4385-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="f4385-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="f4385-107">備註</span><span class="sxs-lookup"><span data-stu-id="f4385-107">Remarks</span></span>

<span data-ttu-id="f4385-108">這個屬性會對應至 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)結構的 **dwSequenceHeader** 成員，或 [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)結構的 **bSequenceHeader** 成員。</span><span class="sxs-lookup"><span data-stu-id="f4385-108">This attribute corresponds to the **dwSequenceHeader** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure, or the **bSequenceHeader** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) structure.</span></span>

<span data-ttu-id="f4385-109">針對 h264 和 h265 video，blob 包含附錄 B 格式的串連 [NAL 單位](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) 以及其起始程式碼。</span><span class="sxs-lookup"><span data-stu-id="f4385-109">For h264 and h265 video, the blob contains concatenated [NAL units](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) in Annex B format, along with their start codes.</span></span> <span data-ttu-id="f4385-110">具體來說，針對 h264 video，它們是 SPS & PPS NAL 單位。</span><span class="sxs-lookup"><span data-stu-id="f4385-110">Specifically, for h264 video they are SPS & PPS NAL units.</span></span> <span data-ttu-id="f4385-111">針對 h265，它們是 VPS，SPS & PPS。</span><span class="sxs-lookup"><span data-stu-id="f4385-111">For h265 they are VPS, SPS & PPS.</span></span>

<span data-ttu-id="f4385-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="f4385-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4385-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4385-113">Requirements</span></span>



| <span data-ttu-id="f4385-114">需求</span><span class="sxs-lookup"><span data-stu-id="f4385-114">Requirement</span></span> | <span data-ttu-id="f4385-115">值</span><span class="sxs-lookup"><span data-stu-id="f4385-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4385-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4385-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f4385-117">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4385-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f4385-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4385-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f4385-119">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4385-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f4385-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f4385-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4385-121"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4385-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4385-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4385-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4385-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f4385-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4385-124">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="f4385-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="f4385-125">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="f4385-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="f4385-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="f4385-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f4385-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="f4385-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
