---
description: 音訊媒體類型的每個音訊樣本位數。
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: 'MF_MT_AUDIO_BITS_PER_SAMPLE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969268"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a><span data-ttu-id="35d01-103">\_每個樣本的 MF MT \_ 音訊 \_ 位數 \_ \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="35d01-103">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="35d01-104">音訊媒體類型的每個音訊樣本位數。</span><span class="sxs-lookup"><span data-stu-id="35d01-104">Number of bits per audio sample in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="35d01-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="35d01-105">Data type</span></span>

<span data-ttu-id="35d01-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="35d01-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="35d01-107">備註</span><span class="sxs-lookup"><span data-stu-id="35d01-107">Remarks</span></span>

<span data-ttu-id="35d01-108">這個屬性會對應至 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構的 **wBitsPerSample** 成員。</span><span class="sxs-lookup"><span data-stu-id="35d01-108">This attribute corresponds to the **wBitsPerSample** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="35d01-109">如果某些位包含填補，請設定每個樣本屬性的 [**MF \_ MT \_ 音訊 \_ 有效 \_ 位數 \_ \_**](mf-mt-audio-valid-bits-per-sample-attribute.md) ，以指定每個樣本中的有效音訊資料位數。</span><span class="sxs-lookup"><span data-stu-id="35d01-109">If some bits contain padding, set the [**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md) attribute to specify the number of bits of valid audio data in each sample.</span></span>

<span data-ttu-id="35d01-110">如果音訊包含每個樣本8個位，則音訊樣本為不帶正負號的值。</span><span class="sxs-lookup"><span data-stu-id="35d01-110">If the audio contains 8 bits per sample, the audio samples are unsigned values.</span></span> <span data-ttu-id="35d01-111"> (每個音訊樣本的範圍為0–255。 ) 如果音訊包含每個樣本或更高的16個位，則音訊樣本為帶正負號的值。</span><span class="sxs-lookup"><span data-stu-id="35d01-111">(Each audio sample has the range 0–255.) If the audio contains 16 bits per sample or higher, the audio samples are signed values.</span></span>

<span data-ttu-id="35d01-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="35d01-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d01-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="35d01-113">Requirements</span></span>



| <span data-ttu-id="35d01-114">需求</span><span class="sxs-lookup"><span data-stu-id="35d01-114">Requirement</span></span> | <span data-ttu-id="35d01-115">值</span><span class="sxs-lookup"><span data-stu-id="35d01-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35d01-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35d01-116">Minimum supported client</span></span><br/> | <span data-ttu-id="35d01-117">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35d01-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="35d01-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35d01-118">Minimum supported server</span></span><br/> | <span data-ttu-id="35d01-119">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35d01-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="35d01-120">標頭</span><span class="sxs-lookup"><span data-stu-id="35d01-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="35d01-121"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="35d01-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d01-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35d01-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d01-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="35d01-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="35d01-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="35d01-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="35d01-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="35d01-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="35d01-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="35d01-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="35d01-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="35d01-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
