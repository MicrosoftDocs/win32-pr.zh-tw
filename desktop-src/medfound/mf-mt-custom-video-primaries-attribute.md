---
description: 指定影片媒體類型的自訂色彩主要複本。
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: 'MF_MT_CUSTOM_VIDEO_PRIMARIES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980686"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a><span data-ttu-id="eea27-103">MF \_ MT \_ 自訂 \_ 影片 \_ 主要複本屬性</span><span class="sxs-lookup"><span data-stu-id="eea27-103">MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="eea27-104">指定影片媒體類型的自訂色彩主要複本。</span><span class="sxs-lookup"><span data-stu-id="eea27-104">Specifies custom color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="eea27-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="eea27-105">Data type</span></span>

<span data-ttu-id="eea27-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="eea27-106">**UINT32**</span></span>

<span data-ttu-id="eea27-107">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="eea27-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="eea27-108">備註</span><span class="sxs-lookup"><span data-stu-id="eea27-108">Remarks</span></span>

<span data-ttu-id="eea27-109">屬性資料是 [**MT \_ 自訂 \_ 影片 \_ 主要複本**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) 結構。</span><span class="sxs-lookup"><span data-stu-id="eea27-109">The attribute data is an [**MT\_CUSTOM\_VIDEO\_PRIMARIES**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) structure.</span></span>

<span data-ttu-id="eea27-110">這個屬性會指定內容的實際色彩量或顯示。</span><span class="sxs-lookup"><span data-stu-id="eea27-110">This attribute specifies the actual color volume of content or a display.</span></span> <span data-ttu-id="eea27-111">CEA-861.3/SMPTE ST. 2006 色彩磁片區主控資訊是由解碼器儲存在這個屬性中。</span><span class="sxs-lookup"><span data-stu-id="eea27-111">CEA-861.3 / SMPTE ST.2086 color volume mastering information is stored in this attribute by decoders.</span></span> <span data-ttu-id="eea27-112">請注意，此屬性不會取代 [**MF \_ MT \_ 影片 \_ 主要複本**](mf-mt-video-primaries-attribute.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="eea27-112">Note that this attribute does not replace the [**MF\_MT\_VIDEO\_PRIMARIES**](mf-mt-video-primaries-attribute.md)attribute.</span></span> <span data-ttu-id="eea27-113">此屬性描述內容之色彩量的提示，而 [ **MF \_ MT \_ 影片 \_ 主要複本** ] 則描述內容實際上的編碼方式的色彩主要複本 (例如：浮點數標記法之 R/g/B 通道中的1.0 意義) 。</span><span class="sxs-lookup"><span data-stu-id="eea27-113">This attribute describes a hint about the color volume of the content, whereas **MF\_MT\_VIDEO\_PRIMARIES** describes the color primaries in which the content is actually coded (e.g: the meaning of 1.0 in the R/G/B channels of a floating point representation).</span></span>

<span data-ttu-id="eea27-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="eea27-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea27-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="eea27-115">Requirements</span></span>



| <span data-ttu-id="eea27-116">需求</span><span class="sxs-lookup"><span data-stu-id="eea27-116">Requirement</span></span> | <span data-ttu-id="eea27-117">值</span><span class="sxs-lookup"><span data-stu-id="eea27-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eea27-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eea27-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eea27-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eea27-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eea27-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eea27-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eea27-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eea27-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eea27-122">標頭</span><span class="sxs-lookup"><span data-stu-id="eea27-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea27-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="eea27-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eea27-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eea27-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea27-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="eea27-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eea27-126">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="eea27-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="eea27-127">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="eea27-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="eea27-128">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="eea27-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="eea27-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="eea27-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




