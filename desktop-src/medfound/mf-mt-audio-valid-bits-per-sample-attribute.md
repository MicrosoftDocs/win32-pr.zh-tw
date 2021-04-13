---
description: 每個音訊樣本中音訊資料的有效位數。
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: 'MF_MT_AUDIO_VALID_BITS_PER_SAMPLE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e5efb41bf3b79d4feded2872b601eea43723a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320944"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a><span data-ttu-id="32f66-103">\_ \_ \_ \_ \_ 每個 \_ 樣本屬性的 MF MT 音訊有效位數</span><span class="sxs-lookup"><span data-stu-id="32f66-103">MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="32f66-104">每個音訊樣本中音訊資料的有效位數。</span><span class="sxs-lookup"><span data-stu-id="32f66-104">Number of valid bits of audio data in each audio sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="32f66-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="32f66-105">Data type</span></span>

<span data-ttu-id="32f66-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="32f66-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="32f66-107">備註</span><span class="sxs-lookup"><span data-stu-id="32f66-107">Remarks</span></span>

<span data-ttu-id="32f66-108">每個樣本屬性的 **MF \_ MT \_ 音訊 \_ 有效 \_ 位數 \_ \_** ，會用於在每個音訊樣本之後包含填補的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="32f66-108">The **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is used for audio formats that contain padding after each audio sample.</span></span> <span data-ttu-id="32f66-109">每個音訊樣本的總大小（包括填補位）都會提供給每個範例屬性的 [**MF \_ MT \_ 音訊 \_ 位 \_ \_**](mf-mt-audio-bits-per-sample-attribute.md) 。</span><span class="sxs-lookup"><span data-stu-id="32f66-109">The total size of each audio sample, including padding bits, is given in the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="32f66-110">如果未設定 [ **\_ \_ \_ \_ \_ 每個 \_ 範例的 mf mt 音訊有效位數** ] 屬性，請使用 [ [**\_ \_ \_ \_ 每個 \_ 樣本的 mf mt 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md) ] 屬性來尋找每個樣本的有效位數數目。</span><span class="sxs-lookup"><span data-stu-id="32f66-110">If the **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is not set, use the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute to find the number of valid bits per sample.</span></span>

<span data-ttu-id="32f66-111">如果音訊格式未包含任何填補位，則不應設定這個屬性，或將其設定為與 [**\_ \_ \_ \_ 每個 \_ 範例的 MF MT 音訊位**](mf-mt-audio-bits-per-sample-attribute.md) 相同的值。</span><span class="sxs-lookup"><span data-stu-id="32f66-111">If an audio format does not contain any padding bits, then this attribute should not be set, or should be set to the same value as the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="32f66-112">這個屬性會對應至 [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)結構的 **wValidBitsPerSample** 成員。</span><span class="sxs-lookup"><span data-stu-id="32f66-112">This attribute corresponds to the **wValidBitsPerSample** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="32f66-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="32f66-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="32f66-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="32f66-114">Requirements</span></span>



| <span data-ttu-id="32f66-115">需求</span><span class="sxs-lookup"><span data-stu-id="32f66-115">Requirement</span></span> | <span data-ttu-id="32f66-116">值</span><span class="sxs-lookup"><span data-stu-id="32f66-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32f66-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32f66-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32f66-118">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32f66-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="32f66-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32f66-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32f66-120">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32f66-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="32f66-121">標頭</span><span class="sxs-lookup"><span data-stu-id="32f66-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f66-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="32f66-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32f66-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32f66-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f66-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="32f66-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="32f66-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="32f66-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="32f66-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="32f66-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="32f66-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="32f66-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="32f66-128">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="32f66-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
