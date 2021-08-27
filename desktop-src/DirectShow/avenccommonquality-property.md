---
description: 指定編碼的品質等級。
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: 'AVEncCommonQuality 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99202391e919fa1da9028a15a57154834feddd3039160b9b0562a713fe59ddaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087668"
---
# <a name="avenccommonquality-property"></a>AVEncCommonQuality 屬性

指定編碼的品質等級。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonQuality**

## <a name="property-value"></a>屬性值

這個屬性的值具有下列範圍。



| 值 | 描述                           |
|-------|---------------------------------------|
| 0     | 最小品質、較小的輸出大小。 |
| 100   | 品質上限，較大的輸出大小。  |



 

## <a name="remarks"></a>備註

當編碼器未使用限制的位元速率時，此屬性會控制品質層級。 [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)屬性可判斷位元速率是否受限制。

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

 

 




