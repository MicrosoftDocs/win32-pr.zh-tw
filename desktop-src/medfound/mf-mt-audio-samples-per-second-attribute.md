---
description: 音訊媒體類型的每秒音訊樣本數。
ms.assetid: f640016d-595e-4b20-8ce8-23a029c2b064
title: 'MF_MT_AUDIO_SAMPLES_PER_SECOND 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5080f6df87bafe8d4ee86e7b25332a12214ff3cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848525"
---
# <a name="mf_mt_audio_samples_per_second-attribute"></a><span data-ttu-id="91d71-103">\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="91d71-103">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND attribute</span></span>

<span data-ttu-id="91d71-104">音訊媒體類型的每秒音訊樣本數。</span><span class="sxs-lookup"><span data-stu-id="91d71-104">Number of audio samples per second in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="91d71-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="91d71-105">Data type</span></span>

<span data-ttu-id="91d71-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="91d71-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="91d71-107">備註</span><span class="sxs-lookup"><span data-stu-id="91d71-107">Remarks</span></span>

<span data-ttu-id="91d71-108">這個屬性會對應至 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構的 **nSamplesPerSec** 成員。</span><span class="sxs-lookup"><span data-stu-id="91d71-108">This attribute corresponds to the **nSamplesPerSec** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="91d71-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="91d71-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="91d71-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="91d71-110">Requirements</span></span>



| <span data-ttu-id="91d71-111">需求</span><span class="sxs-lookup"><span data-stu-id="91d71-111">Requirement</span></span> | <span data-ttu-id="91d71-112">值</span><span class="sxs-lookup"><span data-stu-id="91d71-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91d71-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91d71-113">Minimum supported client</span></span><br/> | <span data-ttu-id="91d71-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91d71-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="91d71-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91d71-115">Minimum supported server</span></span><br/> | <span data-ttu-id="91d71-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91d71-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="91d71-117">標頭</span><span class="sxs-lookup"><span data-stu-id="91d71-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d71-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="91d71-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91d71-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91d71-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d71-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="91d71-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="91d71-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="91d71-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="91d71-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="91d71-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="91d71-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="91d71-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="91d71-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="91d71-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="91d71-125">**\_每秒的 MF MT \_ 音訊 \_ FLOAT \_ 樣本 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d71-125">**MF\_MT\_AUDIO\_FLOAT\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-float-samples-per-second-attribute.md)
</dt> </dl>

 

 
