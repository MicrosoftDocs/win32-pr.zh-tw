---
description: 音訊媒體類型中每秒的平均位元組數。
ms.assetid: 0ee371fb-d980-44de-a9bd-201e2b72e874
title: 'MF_MT_AUDIO_AVG_BYTES_PER_SECOND 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca86276e816ea1ef058946bad29f1565fe1c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193377"
---
# <a name="mf_mt_audio_avg_bytes_per_second-attribute"></a><span data-ttu-id="fce72-103">MF \_ MT \_ 音訊 \_ \_ 每秒平均位元組數 \_ \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="fce72-103">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND attribute</span></span>

<span data-ttu-id="fce72-104">音訊媒體類型中每秒的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="fce72-104">Average number of bytes per second in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="fce72-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="fce72-105">Data type</span></span>

<span data-ttu-id="fce72-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fce72-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fce72-107">備註</span><span class="sxs-lookup"><span data-stu-id="fce72-107">Remarks</span></span>

<span data-ttu-id="fce72-108">這個屬性會對應至 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構的 **nAvgBytesPerSec** 成員。</span><span class="sxs-lookup"><span data-stu-id="fce72-108">This attribute corresponds to the **nAvgBytesPerSec** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="fce72-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="fce72-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce72-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="fce72-110">Requirements</span></span>



| <span data-ttu-id="fce72-111">需求</span><span class="sxs-lookup"><span data-stu-id="fce72-111">Requirement</span></span> | <span data-ttu-id="fce72-112">值</span><span class="sxs-lookup"><span data-stu-id="fce72-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fce72-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fce72-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fce72-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fce72-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="fce72-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fce72-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fce72-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fce72-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fce72-117">標頭</span><span class="sxs-lookup"><span data-stu-id="fce72-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce72-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fce72-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce72-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fce72-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce72-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="fce72-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fce72-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="fce72-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="fce72-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="fce72-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="fce72-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="fce72-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="fce72-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="fce72-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
