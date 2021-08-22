---
description: 設定影片編碼器的影片時態圖層計數。
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: 'CODECAPI_AVEncVideoTemporalLayerCount 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81ceaf82d9d202e97927e0e141aa03a4e8e27c49a28880509aa9bb3c24f9319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743838"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a>CODECAPI \_ AVEncVideoTemporalLayerCount 屬性

設定影片編碼器的影片時態圖層計數。

## <a name="data-type"></a>資料類型

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoTemporalLayerCount**

## <a name="remarks"></a>備註

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。

CODECAPI \_ AVEncVideoTemporalLayerCount、 [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)和 [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) 是靜態編碼器屬性。 一旦設定之後，只有在相機的輸出 pin 上呼叫設定媒體類型之後，才會生效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

