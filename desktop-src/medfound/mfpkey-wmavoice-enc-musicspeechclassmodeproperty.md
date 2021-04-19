---
description: 指定語音編解碼器的模式。
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: 'MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979038"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode 屬性

指定語音編解碼器的模式。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMACMusicSpeechClassMode

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

1

## <a name="remarks"></a>備註

值為1時，會通知編解碼器內容為純語音，值為2時，編解碼器會自動判斷模式，而任何其他值則會通知編解碼器使用音樂模式。

如果自動模式未正確地編碼混合語音和音樂，您可以使用 [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) 屬性指定檔案個別區段的編碼方式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




