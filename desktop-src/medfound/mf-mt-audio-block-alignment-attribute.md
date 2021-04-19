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
# <a name="mf_mt_audio_block_alignment-attribute"></a>MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊屬性

封鎖音訊媒體類型的對齊（以位元組為單位）。 區塊對齊是音訊格式資料的最小不可部分完成單位。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

針對 PCM 音訊格式，區塊對齊會等於音訊頻道數目乘以每個音訊樣本的位元組數。

這個屬性會對應至 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構的 **nBlockAlign** 成員。

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

 

 
