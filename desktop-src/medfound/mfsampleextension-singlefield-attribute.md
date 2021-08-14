---
description: 指定影片範例是否包含單一欄位或兩個交錯欄位。 這個屬性會套用至媒體範例。
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: 'MFSampleExtension_SingleField 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747dbeebb9bcc8e773b59467f460b12645ed50ebfbddf5bbf6845119c2bba81d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462898"
---
# <a name="mfsampleextension_singlefield-attribute"></a>MFSampleExtension \_ SingleField 屬性

指定影片範例是否包含單一欄位或兩個交錯欄位。 這個屬性會套用至媒體範例。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

如果值為 **TRUE**，此範例就會包含一個欄位。 如果值為 **FALSE** 或未設定屬性，則範例包含完整的框架。 如果交錯式或漸進式框架， (兩個欄位。 ) 

如果媒體類型是漸進式框架或交錯的欄位，這個屬性必須為 **FALSE** 或保持未設定。

如果媒體類型是單一欄位，則此屬性必須為 **TRUE**。 設定範例上的 [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) 屬性，以指出它是上方欄位或較低的欄位。

目前增強型影片轉譯器 (EVR) 不支援在交錯式框架和單一欄位之間切換的內容。

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

[範例屬性](sample-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> <dt>

[影片交錯](video-interlacing.md)
</dt> </dl>

 

 




