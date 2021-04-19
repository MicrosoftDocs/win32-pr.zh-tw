---
description: 音訊輔助 (AAUX 數位視訊中第一個音訊區塊的) 來源套件 (DV) 媒體類型。
ms.assetid: a37d9371-0d9f-44a8-b8b3-9fbfcfad1a51
title: 'MF_MT_DV_AAUX_SRC_PACK_0 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f37f7f6110f6a04f025864e95488782b855128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982321"
---
# <a name="mf_mt_dv_aaux_src_pack_0-attribute"></a>MF \_ MT \_ DV \_ AAUX \_ SRC \_ PACK \_ 0 屬性

音訊輔助 (AAUX 數位視訊中第一個音訊區塊的) 來源套件 (DV) 媒體類型。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會對應至 DirectShow [**DVINFO**](/windows/win32/api/strmif/ns-strmif-dvinfo)結構的 **dwDVAAuxSrc** 成員。

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

 

 
