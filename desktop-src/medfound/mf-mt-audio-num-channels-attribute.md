---
description: 音訊媒體類型中的音訊聲道數目。
ms.assetid: 524283fb-d046-4f8c-a30f-4fe7ddb43174
title: 'MF_MT_AUDIO_NUM_CHANNELS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09020ef540b6a3b02eecc6a6d788c18d07358ce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999911"
---
# <a name="mf_mt_audio_num_channels-attribute"></a><span data-ttu-id="087e4-103">MF \_ MT \_ 音訊 \_ NUM channel \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="087e4-103">MF\_MT\_AUDIO\_NUM\_CHANNELS attribute</span></span>

<span data-ttu-id="087e4-104">音訊媒體類型中的音訊聲道數目。</span><span class="sxs-lookup"><span data-stu-id="087e4-104">Number of audio channels in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="087e4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="087e4-105">Data type</span></span>

<span data-ttu-id="087e4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="087e4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="087e4-107">備註</span><span class="sxs-lookup"><span data-stu-id="087e4-107">Remarks</span></span>

<span data-ttu-id="087e4-108">這個屬性會對應至 [WAVEFORMATEX](mf-mt-audio-prefer-waveformatex-attribute.md)結構的 **nChannels** 成員。</span><span class="sxs-lookup"><span data-stu-id="087e4-108">This attribute corresponds to the **nChannels** member of the [WAVEFORMATEX](mf-mt-audio-prefer-waveformatex-attribute.md) structure.</span></span>

<span data-ttu-id="087e4-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="087e4-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="087e4-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="087e4-110">Requirements</span></span>



| <span data-ttu-id="087e4-111">需求</span><span class="sxs-lookup"><span data-stu-id="087e4-111">Requirement</span></span> | <span data-ttu-id="087e4-112">值</span><span class="sxs-lookup"><span data-stu-id="087e4-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="087e4-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="087e4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="087e4-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="087e4-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="087e4-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="087e4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="087e4-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="087e4-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="087e4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="087e4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="087e4-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="087e4-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="087e4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="087e4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="087e4-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="087e4-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="087e4-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="087e4-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="087e4-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="087e4-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="087e4-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="087e4-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="087e4-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="087e4-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




