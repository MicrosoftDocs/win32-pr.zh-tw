---
description: 指定用戶端電腦上的說話者設定。
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: 'MFPKEY_WMADEC_SPKRCFG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513040"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a>MFPKEY \_ WMADEC \_ SPKRCFG 屬性

指定用戶端電腦上的說話者設定。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMACSpeakerConfig

## <a name="data-type"></a>資料類型

**VT \_ UI4**

## <a name="default-value"></a>預設值

未採用任何特定的說話者設定。

## <a name="remarks"></a>備註

您應該將此值設定為下表中的其中一個常數或值。 這些常數定義于 Microsoft DirectSound 中，為了方便起見，在這裡列出。 若要為您的編譯器解析這些常數名稱，您必須包含 dsound。



| 常數             | 值      | 描述                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ DIRECTOUT | 0x00000000 | 系統會直接傳遞音訊，而不是針對喇叭進行設定。 |
| DSSPEAKER \_ 耳機 | 0x00000001 | 用戶端電腦配備耳機。                             |
| DSSPEAKER \_ MONO      | 0x00000002 | 用戶端電腦配備了 monoaural 喇叭。                    |
| DSSPEAKER \_ 四      | 0x00000003 | 用戶端電腦配備了 quadraphonic 喇叭。                  |
| DSSPEAKER \_ 身歷聲    | 0x00000004 | 用戶端電腦配備了身歷聲喇叭。                        |
| DSSPEAKER \_ 環繞  | 0x00000005 | 用戶端電腦配備四個聲道的環繞音效喇叭。   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | 用戶端電腦配備了五個喇叭和一個喇叭。          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | 用戶端電腦配備了七個喇叭和一個喇叭。         |



 

針對此屬性所設定的值會決定由編解碼器音訊之編解碼器列舉的輸出格式。

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

 

 




