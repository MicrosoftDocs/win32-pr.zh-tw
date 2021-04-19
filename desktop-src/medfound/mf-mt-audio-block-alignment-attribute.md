---
description: 封鎖音訊媒體類型的對齊（以位元組為單位）。 區塊對齊是音訊格式資料的最小不可部分完成單位。
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: 'MF_MT_AUDIO_BLOCK_ALIGNMENT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983705"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a><span data-ttu-id="dc5e0-104">MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊屬性</span><span class="sxs-lookup"><span data-stu-id="dc5e0-104">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT attribute</span></span>

<span data-ttu-id="dc5e0-105">封鎖音訊媒體類型的對齊（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dc5e0-105">Block alignment, in bytes, for an audio media type.</span></span> <span data-ttu-id="dc5e0-106">區塊對齊是音訊格式資料的最小不可部分完成單位。</span><span class="sxs-lookup"><span data-stu-id="dc5e0-106">The block alignment is the minimum atomic unit of data for the audio format.</span></span>

## <a name="data-type"></a><span data-ttu-id="dc5e0-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="dc5e0-107">Data type</span></span>

<span data-ttu-id="dc5e0-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dc5e0-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dc5e0-109">備註</span><span class="sxs-lookup"><span data-stu-id="dc5e0-109">Remarks</span></span>

<span data-ttu-id="dc5e0-110">針對 PCM 音訊格式，區塊對齊會等於音訊頻道數目乘以每個音訊樣本的位元組數。</span><span class="sxs-lookup"><span data-stu-id="dc5e0-110">For PCM audio formats, the block alignment is equal to the number of audio channels multiplied by the number of bytes per audio sample.</span></span>

<span data-ttu-id="dc5e0-111">這個屬性會對應至 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構的 **nBlockAlign** 成員。</span><span class="sxs-lookup"><span data-stu-id="dc5e0-111">This attribute corresponds to the **nBlockAlign** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="dc5e0-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="dc5e0-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc5e0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc5e0-113">Requirements</span></span>



| <span data-ttu-id="dc5e0-114">需求</span><span class="sxs-lookup"><span data-stu-id="dc5e0-114">Requirement</span></span> | <span data-ttu-id="dc5e0-115">值</span><span class="sxs-lookup"><span data-stu-id="dc5e0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc5e0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc5e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dc5e0-117">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc5e0-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dc5e0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc5e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dc5e0-119">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc5e0-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dc5e0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="dc5e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc5e0-121"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc5e0-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc5e0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc5e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc5e0-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="dc5e0-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dc5e0-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dc5e0-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dc5e0-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dc5e0-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dc5e0-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="dc5e0-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="dc5e0-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="dc5e0-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
