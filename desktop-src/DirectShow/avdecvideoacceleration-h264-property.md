---
description: 啟用或停用 h.264 影片解碼的硬體加速。
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: 'AVDecVideoAcceleration_H264 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84279c49e65586d07dbf1efa4c372a1b1f8770e19bd00eb827ba44b6ad43bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663962"
---
# <a name="avdecvideoacceleration_h264-property"></a>AVDecVideoAcceleration \_ H264 屬性

啟用或停用 h.264 影片解碼的硬體加速。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecVideoAcceleration \_ H264**

## <a name="remarks"></a>備註

如果值為零，則不會使用 DirectX Video 加速 (DXVA) 進行 h.264 影片解碼。 針對 DirectShow 篩選準則，請在配置解碼器的輸出連接之前設定這個屬性。

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

 

 




