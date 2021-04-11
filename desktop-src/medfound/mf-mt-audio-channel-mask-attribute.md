---
description: 在音訊媒體類型中，指定喇叭位置的音訊通道指派。
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: 'MF_MT_AUDIO_CHANNEL_MASK 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5293f5387a2c293b97ee32db54fcfb3f3ff304d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026442"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a><span data-ttu-id="de736-103">MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩屬性</span><span class="sxs-lookup"><span data-stu-id="de736-103">MF\_MT\_AUDIO\_CHANNEL\_MASK attribute</span></span>

<span data-ttu-id="de736-104">在音訊媒體類型中，指定喇叭位置的音訊通道指派。</span><span class="sxs-lookup"><span data-stu-id="de736-104">In an audio media type, specifies the assignment of audio channels to speaker positions.</span></span>

## <a name="data-type"></a><span data-ttu-id="de736-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="de736-105">Data type</span></span>

<span data-ttu-id="de736-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="de736-106">**UINT32**</span></span>

<span data-ttu-id="de736-107">這個屬性的值是下列旗標的位 **or** ，這些旗標是在標頭檔 mmreg 中定義。</span><span class="sxs-lookup"><span data-stu-id="de736-107">The value of this attribute is a bitwise **OR** of the following flags, which are defined in the header file mmreg.h.</span></span>

<dl> <dt>

<span data-ttu-id="de736-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**講師 \_\_左** (0x1) </span><span class="sxs-lookup"><span data-stu-id="de736-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**SPEAKER\_FRONT\_LEFT** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="de736-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**講師 \_FRONT \_ 右邊** (0x2) </span><span class="sxs-lookup"><span data-stu-id="de736-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**SPEAKER\_FRONT\_RIGHT** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="de736-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**講師 \_FRONT \_ CENTER** (0x4) </span><span class="sxs-lookup"><span data-stu-id="de736-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**SPEAKER\_FRONT\_CENTER** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="de736-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**講師 \_低 \_ 頻率** (0x8) </span><span class="sxs-lookup"><span data-stu-id="de736-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**SPEAKER\_LOW\_FREQUENCY** (0x8)</span></span>
</dt> <dt>

<span data-ttu-id="de736-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**講師 \_向 \_ 左** (0x10) </span><span class="sxs-lookup"><span data-stu-id="de736-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**SPEAKER\_BACK\_LEFT** (0x10)</span></span>
</dt> <dt>

<span data-ttu-id="de736-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**講師 \_向 \_ 右** (0x20) </span><span class="sxs-lookup"><span data-stu-id="de736-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**SPEAKER\_BACK\_RIGHT** (0x20)</span></span>
</dt> <dt>

<span data-ttu-id="de736-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**講師 \_\_ \_ \_ CENTER 左方** (0x40) </span><span class="sxs-lookup"><span data-stu-id="de736-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**SPEAKER\_FRONT\_LEFT\_OF\_CENTER** (0x40)</span></span>
</dt> <dt>

<span data-ttu-id="de736-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**講師 \_\_ \_ \_ CENTER 的右上方** (0x80) </span><span class="sxs-lookup"><span data-stu-id="de736-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**SPEAKER\_FRONT\_RIGHT\_OF\_CENTER** (0x80)</span></span>
</dt> <dt>

<span data-ttu-id="de736-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**講師 \_後 \_** 置 (0x100) </span><span class="sxs-lookup"><span data-stu-id="de736-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**SPEAKER\_BACK\_CENTER** (0x100)</span></span>
</dt> <dt>

<span data-ttu-id="de736-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**講師 \_\_左邊** (0x200) </span><span class="sxs-lookup"><span data-stu-id="de736-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**SPEAKER\_SIDE\_LEFT** (0x200)</span></span>
</dt> <dt>

<span data-ttu-id="de736-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**講師 \_右邊 \_ (0x400**) </span><span class="sxs-lookup"><span data-stu-id="de736-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**SPEAKER\_SIDE\_RIGHT** (0x400)</span></span>
</dt> <dt>

<span data-ttu-id="de736-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**講師 \_\_中央** (0x800) </span><span class="sxs-lookup"><span data-stu-id="de736-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**SPEAKER\_TOP\_CENTER** (0x800)</span></span>
</dt> <dt>

<span data-ttu-id="de736-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**講師 \_左上 \_ \_ 方** (0x1000) </span><span class="sxs-lookup"><span data-stu-id="de736-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**SPEAKER\_TOP\_FRONT\_LEFT** (0x1000)</span></span>
</dt> <dt>

<span data-ttu-id="de736-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**講師 \_前幾名 \_ 前端 \_** (0x2000) </span><span class="sxs-lookup"><span data-stu-id="de736-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**SPEAKER\_TOP\_FRONT\_CENTER** (0x2000)</span></span>
</dt> <dt>

<span data-ttu-id="de736-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**講師 \_TOP \_ \_ 右邊** (0x4000) </span><span class="sxs-lookup"><span data-stu-id="de736-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**SPEAKER\_TOP\_FRONT\_RIGHT** (0x4000)</span></span>
</dt> <dt>

<span data-ttu-id="de736-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**講師 \_左上 \_ \_ 角** (0x8000) </span><span class="sxs-lookup"><span data-stu-id="de736-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**SPEAKER\_TOP\_BACK\_LEFT** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="de736-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**講師 \_ (0x10000) 的上層 \_ \_ 下載中心**</span><span class="sxs-lookup"><span data-stu-id="de736-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**SPEAKER\_TOP\_BACK\_CENTER** (0x10000)</span></span>
</dt> <dt>

<span data-ttu-id="de736-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**講師 \_右上 \_ \_ 方** (0x20000) </span><span class="sxs-lookup"><span data-stu-id="de736-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**SPEAKER\_TOP\_BACK\_RIGHT** (0x20000)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="de736-126">備註</span><span class="sxs-lookup"><span data-stu-id="de736-126">Remarks</span></span>

<span data-ttu-id="de736-127">這個屬性會對應至 [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)結構的 **dwChannelMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="de736-127">This attribute corresponds to the **dwChannelMask** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="de736-128">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="de736-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="de736-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="de736-129">Requirements</span></span>



| <span data-ttu-id="de736-130">需求</span><span class="sxs-lookup"><span data-stu-id="de736-130">Requirement</span></span> | <span data-ttu-id="de736-131">值</span><span class="sxs-lookup"><span data-stu-id="de736-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de736-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de736-132">Minimum supported client</span></span><br/> | <span data-ttu-id="de736-133">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de736-133">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="de736-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de736-134">Minimum supported server</span></span><br/> | <span data-ttu-id="de736-135">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de736-135">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="de736-136">標頭</span><span class="sxs-lookup"><span data-stu-id="de736-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="de736-137"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="de736-137"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de736-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de736-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de736-139">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="de736-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="de736-140">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="de736-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="de736-141">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="de736-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="de736-142">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="de736-142">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="de736-143">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="de736-143">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
