---
description: 啟用或停用 h.264 影片解碼的硬體加速。
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: 'AVDecVideoAcceleration_H264 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846680"
---
# <a name="avdecvideoacceleration_h264-property"></a>AVDecVideoAcceleration \_ H264 屬性

啟用或停用 h.264 影片解碼的硬體加速。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecVideoAcceleration \_ H264**

## <a name="remarks"></a>備註

如果值為零，則不會使用 DirectX Video 加速 (DXVA) 進行 h.264 影片解碼。 針對 DirectShow 篩選器，請在配置解碼器的輸出連接之前設定這個屬性。

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

 

 




