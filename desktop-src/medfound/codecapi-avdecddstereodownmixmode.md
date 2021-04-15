---
description: 指定杜比數位音訊解碼器的身歷聲 downmix 模式。
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: 'CODECAPI_AVDecDDStereoDownMixMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7caaed1af804e22b3ec6085241746bdf01eb7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386046"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a>CODECAPI \_ AVDecDDStereoDownMixMode 屬性

指定杜比數位音訊解碼器的身歷聲 downmix 模式。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecDDStereoDownMixMode**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) 列舉的成員。

## <a name="remarks"></a>備註

當對解碼器的輸入是多通道 PCM 音訊，且輸出為身歷聲音訊時，會套用此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

