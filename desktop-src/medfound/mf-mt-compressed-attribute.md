---
description: 指定媒體類型是否壓縮媒體資料。
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: 'MF_MT_COMPRESSED 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afea99ffb0c9f7f9f53fb6edd0b4b87b2ecd4ff4f451e5fd0e56d47a70aee994
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060688"
---
# <a name="mf_mt_compressed-attribute"></a>MF \_ MT \_ 壓縮屬性

指定媒體類型是否壓縮媒體資料。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

如果這個屬性為 **TRUE**，則媒體類型會是壓縮的格式。 否則，可能是媒體類型未壓縮，或壓縮類型未知。

針對所有壓縮格式，這個屬性不一定會設定為 **TRUE** ，因此應用程式通常不會依賴這個屬性。 判斷格式是否壓縮的最可靠方式，是維護已知格式的清單。 如果應用程式無法辨識格式（如 [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 屬性中所指定），則不應假設任何關於格式壓縮的資訊。

若要判斷格式是否使用時態性壓縮 (表示某些範例會計算為先前範例) 的差異，請檢查 [**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**](mf-mt-all-samples-independent-attribute.md) 屬性。

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

 

 




