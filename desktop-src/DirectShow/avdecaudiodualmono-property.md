---
description: AVDecAudioDualMono 屬性-指定雙聲道音訊是否編碼為身歷聲或雙 mono。
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: 'AVDecAudioDualMono 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096566"
---
# <a name="avdecaudiodualmono-property"></a>AVDecAudioDualMono 屬性

指定雙聲道音訊是否編碼為身歷聲或雙 mono。

這是唯讀的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecAudioDualMono**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) 列舉的成員。

## <a name="remarks"></a>備註

只有當解碼器的輸入位資料流程包含雙聲道音訊時，才會套用此屬性。 雙聲道音訊串流可能會編碼為身歷聲或雙 mono。 如果音訊是雙 mono，您可以設定 [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) 屬性來設定解碼器重現音訊的方式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




