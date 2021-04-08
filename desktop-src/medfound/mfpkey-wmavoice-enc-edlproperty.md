---
description: 指定要使用語音編解碼器將內容編碼為音樂的部分內容。
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: 'MFPKEY_WMAVOICE_ENC_EDL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692331"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>MFPKEY \_ WMAVOICE \_ ENC \_ EDL 屬性

指定要使用語音編解碼器將內容編碼為音樂的部分內容。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMACVoiceBuffer

## <a name="data-type"></a>資料類型

VT \_ BSTR

## <a name="default-value"></a>預設值

無預設值。 如果未設定此屬性，編解碼器將會使用 [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) 屬性的值來判斷如何編碼內容。

## <a name="remarks"></a>備註

如果編解碼器的自動模式未提供滿意的結果，您可以使用此屬性。

此值是以逗號分隔的字串，其中至少包含四個整數。 第一個整數是版本號碼;此值一律使用1。 第二個整數是需要編碼為音樂的區段數目。 在第二個整數之後，會有數個代表範圍的值（以毫秒為單位），每個內容區段的一對需要編碼為音樂。

例如，"1，2100200500600" 會通知編碼器使用第1版的音樂。 第一個 [音樂] 區段的開頭為100毫秒，結束于200毫秒。 第二個音樂區段會從500毫秒開始，並于600毫秒結束。

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

 

 




