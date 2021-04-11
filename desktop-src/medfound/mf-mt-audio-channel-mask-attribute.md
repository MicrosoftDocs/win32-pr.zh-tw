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
# <a name="mf_mt_audio_channel_mask-attribute"></a>MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩屬性

在音訊媒體類型中，指定喇叭位置的音訊通道指派。

## <a name="data-type"></a>資料類型

**UINT32**

這個屬性的值是下列旗標的位 **or** ，這些旗標是在標頭檔 mmreg 中定義。

<dl> <dt>

<span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**講師 \_\_左** (0x1) 
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**講師 \_FRONT \_ 右邊** (0x2) 
</dt> <dt>

<span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**講師 \_FRONT \_ CENTER** (0x4) 
</dt> <dt>

<span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**講師 \_低 \_ 頻率** (0x8) 
</dt> <dt>

<span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**講師 \_向 \_ 左** (0x10) 
</dt> <dt>

<span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**講師 \_向 \_ 右** (0x20) 
</dt> <dt>

<span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**講師 \_\_ \_ \_ CENTER 左方** (0x40) 
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**講師 \_\_ \_ \_ CENTER 的右上方** (0x80) 
</dt> <dt>

<span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**講師 \_後 \_** 置 (0x100) 
</dt> <dt>

<span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**講師 \_\_左邊** (0x200) 
</dt> <dt>

<span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**講師 \_右邊 \_ (0x400**) 
</dt> <dt>

<span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**講師 \_\_中央** (0x800) 
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**講師 \_左上 \_ \_ 方** (0x1000) 
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**講師 \_前幾名 \_ 前端 \_** (0x2000) 
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**講師 \_TOP \_ \_ 右邊** (0x4000) 
</dt> <dt>

<span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**講師 \_左上 \_ \_ 角** (0x8000) 
</dt> <dt>

<span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**講師 \_ (0x10000) 的上層 \_ \_ 下載中心**
</dt> <dt>

<span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**講師 \_右上 \_ \_ 方** (0x20000) 
</dt> </dl>

## <a name="remarks"></a>備註

這個屬性會對應至 [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)結構的 **dwChannelMask** 成員。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 
