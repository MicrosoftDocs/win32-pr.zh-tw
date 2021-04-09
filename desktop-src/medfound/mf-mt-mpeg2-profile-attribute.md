---
description: 指定影片媒體類型中的 MPEG-2 或 h.264 設定檔。
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: 'MF_MT_MPEG2_PROFILE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850455"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a>MF \_ MT \_ MPEG2 \_ 配置檔案屬性

指定影片媒體類型中的 MPEG-2 或 h.264 設定檔。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

針對 MPEG-2 video，這個屬性的值是 [**AM \_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) 列舉的成員。

若為 h.264 video，此值為 [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) 列舉的成員。

這個屬性會對應至 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)結構的 **dwProfile** 成員。

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

 

 
