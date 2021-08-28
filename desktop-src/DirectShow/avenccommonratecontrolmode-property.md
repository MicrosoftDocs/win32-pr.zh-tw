---
description: 指定速率控制模式。
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: 'AVEncCommonRateControlMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aaa914f445fcbc535ec423b41306938890d64b747258cb0159add5e4fd43c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794668"
---
# <a name="avenccommonratecontrolmode-property"></a>AVEncCommonRateControlMode 屬性

指定速率控制模式。

應用程式可以設定此屬性來指定速率控制模式。 編碼器也可以將此屬性作為功能傳回。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonRateControlMode**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) 列舉的成員。

## <a name="remarks"></a>備註

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)一起使用。

[CODECAPI \_AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount)、 [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)和 CODECAPI \_ AVEncCommonRateControlMode 是靜態編碼器屬性。 一旦設定之後，只有在相機的輸出圖釘上呼叫設定媒體類型之後，才會生效。

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

 

