---
description: 指定介於0和100之間的數位，指出編碼品質與編碼速度之間的取捨。
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: 'MF_TRANSCODE_QUALITYVSSPEED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001844"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a><span data-ttu-id="91bc2-103">MF \_ 轉碼 \_ QUALITYVSSPEED 屬性</span><span class="sxs-lookup"><span data-stu-id="91bc2-103">MF\_TRANSCODE\_QUALITYVSSPEED attribute</span></span>

<span data-ttu-id="91bc2-104">指定介於0和100之間的數位，指出編碼品質與編碼速度之間的取捨。</span><span class="sxs-lookup"><span data-stu-id="91bc2-104">Specifies a number between 0 and 100 that indicates the tradeoff between encoding quality and encoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="91bc2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="91bc2-105">Data type</span></span>

<span data-ttu-id="91bc2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="91bc2-106">**UINT32**</span></span>

<span data-ttu-id="91bc2-107">這個屬性的值具有下列範圍。</span><span class="sxs-lookup"><span data-stu-id="91bc2-107">The value of this property has the following range.</span></span>



| <span data-ttu-id="91bc2-108">值</span><span class="sxs-lookup"><span data-stu-id="91bc2-108">Value</span></span>                                                                          | <span data-ttu-id="91bc2-109">意義</span><span class="sxs-lookup"><span data-stu-id="91bc2-109">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="91bc2-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91bc2-110"><dt>0</dt></span></span> </dl>   | <span data-ttu-id="91bc2-111">較低的品質、更快速的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="91bc2-111">Lower quality, faster encoding.</span></span><br/>  |
| <dl> <span data-ttu-id="91bc2-112"><dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="91bc2-112"><dt>100</dt></span></span> </dl> | <span data-ttu-id="91bc2-113">品質較高、速度較慢的編碼。</span><span class="sxs-lookup"><span data-stu-id="91bc2-113">Higher quality, slower encoding.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="91bc2-114">取得/設定</span><span class="sxs-lookup"><span data-stu-id="91bc2-114">Get/set</span></span>

<span data-ttu-id="91bc2-115">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="91bc2-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="91bc2-116">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="91bc2-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="91bc2-117">備註</span><span class="sxs-lookup"><span data-stu-id="91bc2-117">Remarks</span></span>

<span data-ttu-id="91bc2-118">這個屬性的 GUID 值與針對 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)定義的 [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)屬性相同，而且具有相同的轉譯。</span><span class="sxs-lookup"><span data-stu-id="91bc2-118">This attribute has the same GUID value as the [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) property defined for [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi), and has the same interpretation.</span></span>

<span data-ttu-id="91bc2-119">應用程式可以在建立 Windows Media 編解碼器的轉碼拓朴之前，在轉碼設定檔上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="91bc2-119">The application can set this attribute on the transcode profile before building the transcode topology for Windows Media codecs.</span></span> <span data-ttu-id="91bc2-120">值必須在0到100的範圍內。</span><span class="sxs-lookup"><span data-stu-id="91bc2-120">The value must be in the range from 0 to 100.</span></span> <span data-ttu-id="91bc2-121">針對影片串流，轉碼拓撲產生器會將值對應到應用程式指定的值，並將對應的值提供給編碼器的 **MFPKEY \_ COMPLEXITYEX** 屬性。</span><span class="sxs-lookup"><span data-stu-id="91bc2-121">For video stream, the transcode topology builder maps a value to the application-specified value and supplies the mapped value to the **MFPKEY\_COMPLEXITYEX** property of the encoder.</span></span> <span data-ttu-id="91bc2-122">較低的值可讓編碼器使用較不復雜的編碼演算法。</span><span class="sxs-lookup"><span data-stu-id="91bc2-122">Lower values enable the encoder to use less complicated encoding algorithms.</span></span> <span data-ttu-id="91bc2-123">使用較簡單的演算法會產生較低品質的輸出，但編碼程式較快，而且需要較少的處理能力。</span><span class="sxs-lookup"><span data-stu-id="91bc2-123">Using simpler algorithms produces lower-quality output, but the encoding process is faster and requires less processing power.</span></span>

<span data-ttu-id="91bc2-124">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="91bc2-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="91bc2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="91bc2-125">Requirements</span></span>



| <span data-ttu-id="91bc2-126">需求</span><span class="sxs-lookup"><span data-stu-id="91bc2-126">Requirement</span></span> | <span data-ttu-id="91bc2-127">值</span><span class="sxs-lookup"><span data-stu-id="91bc2-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91bc2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="91bc2-128">Header</span></span><br/> | <dl> <span data-ttu-id="91bc2-129"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="91bc2-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91bc2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91bc2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91bc2-131">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="91bc2-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="91bc2-132">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="91bc2-132">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="91bc2-133">**IMFTranscodeProfile::SetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="91bc2-133">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
