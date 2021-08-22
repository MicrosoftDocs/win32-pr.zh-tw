---
description: 指定此解碼器的輸出格式。
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: 'AVDecCommonOutputFormat 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129f9a1171c5870eab243108fc0ed6992be4993b886cbd36d72fe91988f321b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586748"
---
# <a name="avdeccommonoutputformat-property"></a>AVDecCommonOutputFormat 屬性

指定此解碼器的輸出格式。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**BSTR** (**VT \_ bstr**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecCommonOutputFormat**

## <a name="property-value"></a>屬性值



| GUID                                                               | 描述                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM                        | PCM 音訊，使用任意數目的頻道                                                                                                                                                                             |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ 耳機            | 身歷聲 PCM 音訊，使用僅限左/右 (Lo/Ro) downmix                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ 身歷聲 \_ 自動          | 身歷聲 PCM 音訊，使用自動選取的身歷聲 downmix 模式 (Lo/Ro 或 Lt/Rt) 。 您可以將此值用於輸入資料流程定義慣用 downmix 模式的音訊格式，例如 [杜比 AC-3]。 |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ 身歷聲 \_ MatrixEncoded | 身歷聲 PCM 音訊，使用矩陣編碼的身歷聲 downmix (Lt/Rt)                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ 位流           | S/PDIF (索尼/Philips 數位介面格式) 壓縮位流，如 IEC-60958 所定義                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM                 | S/PDIF PCM 身歷聲，如 IEC-60958 所定義                                                                                                                                                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




