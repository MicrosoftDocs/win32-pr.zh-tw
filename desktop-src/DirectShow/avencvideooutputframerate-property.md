---
description: 指定編碼器輸出資料流程的畫面播放速率（以每秒畫面格數為單位）。
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: 'AVEncVideoOutputFrameRate 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687792"
---
# <a name="avencvideooutputframerate-property"></a>AVEncVideoOutputFrameRate 屬性

指定編碼器輸出資料流程的畫面播放速率（以每秒畫面格數為單位）。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT64** (**VT \_ UI8**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoOutputFrameRate**

## <a name="property-value"></a>屬性值

這個屬性的值是定義畫面播放速率的比率。 上方的32位包含分子，而較低的32位則包含分母。 下表顯示一般畫面播放速率（以每秒畫面格數為單位）。



| 畫面播放速率 | 外觀比例      |
|------------|------------|
| 23.97      | 24000/1001 |
| 24         | 24/1       |
| 25         | 25/1       |
| 29.97      | 30000/1001 |
| 30         | 30/1       |
| 50         | 50/1       |
| 59.94      | 60000/1001 |
| 60         | 60/1       |



 

## <a name="remarks"></a>備註

應用程式可以設定此屬性來指定輸出畫面播放速率。 編碼器也可以將此屬性作為功能傳回。 根據編碼器，值可能會限制為輸入畫面播放速率。 如果沒有，則編碼器能夠在內部轉換畫面播放速率。 請參閱 [**AVEncVideoOutputFrameRateConversion 屬性**](avencvideooutputframerateconversion-property.md)。

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)一起使用。

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

 

