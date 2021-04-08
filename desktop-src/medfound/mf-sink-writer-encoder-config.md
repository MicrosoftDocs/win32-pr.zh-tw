---
description: 包含具有編碼屬性之屬性存放區的指標。
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: 'MF_SINK_WRITER_ENCODER_CONFIG 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693575"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>MF \_ 接收 \_ 寫入器 \_ 編碼器 \_ CONFIG 屬性

包含具有編碼屬性之屬性存放區的指標。

## <a name="data-type"></a>資料類型

**IUnknown \** _

## <a name="remarks"></a>備註

這個屬性的值是 [_ *IPropertyStore* *](/windows/win32/api/propsys/nn-propsys-ipropertystore)指標。

這個屬性可讓應用程式在使用 [接收寫入器](sink-writer.md)時設定編碼屬性。 若要設定此屬性，請執行下列步驟：

1.  呼叫 [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) 來建立新的屬性存放區。
2.  在屬性存放區上設定編碼器屬性。 可用的屬性視編碼器而定。 如需詳細資訊，請參閱 [編解碼器物件](codecobjects.md)。
3.  呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。
4.  呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) ，以在屬性存放區上設定 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標。
5.  建立接收寫入器的新實例。 將 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標傳遞至建立函數。 如需詳細資訊，請參閱 [接收寫入器屬性](sink-writer-attributes.md)。

接收寫入器會先設定編碼器上的屬性，然後再設定媒體類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[接收寫入器屬性](sink-writer-attributes.md)
</dt> </dl>

 

 
