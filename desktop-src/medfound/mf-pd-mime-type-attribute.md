---
description: 指定內容的 MIME 類型。
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: 'MF_PD_MIME_TYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb68e9b45d51b9fe4732957ef60a4496ca57df5be0185f46a7e28204217b4ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059638"
---
# <a name="mf_pd_mime_type-attribute"></a>MF \_ PD \_ MIME \_ 類型屬性

指定內容的 MIME 類型。

## <a name="data-type"></a>資料類型

寬字元字串

## <a name="remarks"></a>備註

這個屬性會套用至展示描述項。

透過 [MIMEType](../properties/props-system-mimetype.md) 針對媒體檔案公開的 mime 類型可能會有一種偏差，可選擇適用于數位生活網路聯盟的 mime 類型， (DLNA) 。

MF \_ PD \_ MIME \_ 類型和 [MIMEType](../properties/props-system-mimetype.md) 可能不一定相符。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
