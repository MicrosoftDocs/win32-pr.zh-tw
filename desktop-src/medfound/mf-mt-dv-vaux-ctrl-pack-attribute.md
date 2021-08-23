---
description: 影片輔助 (VAUX 數位視訊中) 的原始檔控制套件 (DV) 媒體類型。
ms.assetid: 14098435-5033-489c-908f-cbb814a0349c
title: 'MF_MT_DV_VAUX_CTRL_PACK 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4540c693e715461334b1557231732fe4281f3b404fc1df02d0717efaad69e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722974"
---
# <a name="mf_mt_dv_vaux_ctrl_pack-attribute"></a>MF \_ MT \_ DV \_ VAUX \_ CTRL \_ PACK 屬性

影片輔助 (VAUX 數位視訊中) 的原始檔控制套件 (DV) 媒體類型。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會對應至 DirectShow [**DVINFO**](/windows/win32/api/strmif/ns-strmif-dvinfo)結構的 **dwDVVAuxCtl** 成員。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
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

 

 
