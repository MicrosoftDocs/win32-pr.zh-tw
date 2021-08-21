---
description: 指定編碼期間使用的緩衝區大小。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: 'AVEncCommonBufferSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69eb0c4829d30f3eff0297b7e591686f671d0d67967a65dc76695878d74b454e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794728"
---
# <a name="avenccommonbuffersize-property"></a>AVEncCommonBufferSize 屬性

指定編碼期間使用的緩衝區大小。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonBufferSize**

## <a name="property-value"></a>屬性值

這個屬性具有線性範圍的值。 若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。 UVC 1.5 攝影機編碼器不支援參數範圍。

## <a name="remarks"></a>備註

針對某些影片格式，緩衝區大小是以位指定，其他則以位元組為單位來指定。 請參閱下面的備註，以取得特定資訊。

針對 MPEG 影片，這個屬性會定義影片緩衝區驗證器 (VBV) 緩衝區大小。 緩衝區的大小是以位為單位。

針對 h.264 video 和 Windows Media 視訊，屬性會定義假設的參考解碼器 (HRD) 大小。 緩衝區的大小是以位元組為單位。

針對 UVC 1.5 H264 編碼攝影機，傳送至相機編碼器的 CPB 值必須是16位的對齊方式。 緩衝區的大小是以位元組為單位。

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)一起使用。

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

 

