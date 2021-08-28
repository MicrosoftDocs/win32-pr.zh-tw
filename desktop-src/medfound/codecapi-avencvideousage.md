---
description: 設定影片編碼器的影片使用方式。
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: 'CODECAPI_AVEncVideoUsage 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6d3ee174fbc22ca7b1ab4e309d87112463740a075b497cc35033f8c96bbe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777708"
---
# <a name="codecapi_avencvideousage-property"></a>CODECAPI \_ AVEncVideoUsage 屬性

設定影片編碼器的影片使用方式。

## <a name="data-type"></a>資料類型

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoUsage**

## <a name="remarks"></a>備註

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。

[CODECAPI \_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md)、CODECAPI \_ AVEncVideoUsage 和 [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) 是靜態編碼器屬性。 一旦設定之後，只有在相機的輸出 pin 上呼叫設定媒體類型之後，才會生效。

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

 

