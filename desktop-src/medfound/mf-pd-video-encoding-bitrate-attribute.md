---
description: 指定標記法的影片編碼位元速率（以每秒位數為單位）。 這個屬性會套用至展示描述項。
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: 'MF_PD_VIDEO_ENCODING_BITRATE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985369"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a>MF \_ PD \_ VIDEO \_ 編碼 \_ 位元速率屬性

指定標記法的影片編碼位元速率（以每秒位數為單位）。 這個屬性會套用至展示描述項。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

此屬性是選擇性的。 某些格式有更複雜的編碼配置，無法使用這個屬性來匯總。 若為 Advanced Systems Format (ASF) 檔案，下列屬性統稱為編碼位元速率：

-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 最大 \_ 位元速率**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ 位元速率**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 最大 \_ 資料 \_ 位元速率**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ 位元速率**](mf-sd-asf-streambitrates-bitrate-attribute.md)

協力廠商格式可能會使用其他自訂屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




