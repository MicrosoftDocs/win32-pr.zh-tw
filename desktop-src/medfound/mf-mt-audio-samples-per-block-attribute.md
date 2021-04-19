---
description: 一個壓縮的音訊資料區塊中包含的音訊樣本數。 這個屬性可用於每個區塊中具有固定樣本數的壓縮音訊格式。
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: 'MF_MT_AUDIO_SAMPLES_PER_BLOCK 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988306"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a><span data-ttu-id="dc711-104">\_ \_ \_ \_ 每個 \_ 區塊屬性的 MF MT 音訊範例</span><span class="sxs-lookup"><span data-stu-id="dc711-104">MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK attribute</span></span>

<span data-ttu-id="dc711-105">一個壓縮的音訊資料區塊中包含的音訊樣本數。</span><span class="sxs-lookup"><span data-stu-id="dc711-105">Number of audio samples contained in one compressed block of audio data.</span></span> <span data-ttu-id="dc711-106">這個屬性可用於每個區塊中具有固定樣本數的壓縮音訊格式。</span><span class="sxs-lookup"><span data-stu-id="dc711-106">This attribute can be used in compressed audio formats that have a fixed number of samples within each block.</span></span>

## <a name="data-type"></a><span data-ttu-id="dc711-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="dc711-107">Data type</span></span>

<span data-ttu-id="dc711-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dc711-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dc711-109">備註</span><span class="sxs-lookup"><span data-stu-id="dc711-109">Remarks</span></span>

<span data-ttu-id="dc711-110">這個屬性會對應至 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))結構的 **wSamplesPerBlock** 成員。</span><span class="sxs-lookup"><span data-stu-id="dc711-110">This attribute corresponds to the **wSamplesPerBlock** member of the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="dc711-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="dc711-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc711-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc711-112">Requirements</span></span>



| <span data-ttu-id="dc711-113">需求</span><span class="sxs-lookup"><span data-stu-id="dc711-113">Requirement</span></span> | <span data-ttu-id="dc711-114">值</span><span class="sxs-lookup"><span data-stu-id="dc711-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc711-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc711-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dc711-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc711-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dc711-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc711-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dc711-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc711-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dc711-119">標頭</span><span class="sxs-lookup"><span data-stu-id="dc711-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc711-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc711-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc711-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc711-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc711-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="dc711-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dc711-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dc711-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dc711-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dc711-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dc711-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="dc711-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="dc711-126">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="dc711-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
