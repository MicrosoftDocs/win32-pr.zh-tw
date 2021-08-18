---
description: 指定解碼器如何重現雙重 mono 音訊。
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: 'AVDecAudioDualMonoReproMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9151ed6b996ec4ab92791221b7fb4c920913c818eac4a079ee6f40d04591a9db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917058"
---
# <a name="avdecaudiodualmonorepromode-property"></a>AVDecAudioDualMonoReproMode 屬性

指定解碼器如何重現雙重 mono 音訊。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecAudioDualMonoReproMode**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) 列舉的成員。

## <a name="remarks"></a>備註

只有當解碼器的輸入位資料流程包含雙重 mono 音訊時，才會套用此屬性。 若要測試這種情況，請取得 [AVDecAudioDualMono](avdecaudiodualmono-property.md) 屬性的值。

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

 

 




