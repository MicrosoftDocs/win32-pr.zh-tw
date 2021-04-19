---
description: 指定在解碼檔案之後，可能會傳回的額外 PCM 樣本數上限。
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: 'MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983448"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>MFPKEY \_ 解碼器 \_ MaxNumPCMSamplesWithPaddedSilence 屬性

指定在解碼檔案之後，可能會傳回的額外 PCM 樣本數上限。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

2048

## <a name="remarks"></a>備註

您可以使用這個屬性來預估在歌曲之間插入的人工無回應，這會在歌曲的另一次送入解碼器時插入。

針對 Windows Media 音訊10專業版和 Windows Media 音訊9無失真的解碼器，這個屬性一律等於0。

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

 

 
