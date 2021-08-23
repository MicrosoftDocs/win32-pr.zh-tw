---
description: 指定編碼品質與速度之間的取捨。 此屬性在所有速率控制模式中都是有效的。
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: 'AVEncCommonQualityVsSpeed 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9def8fc53a6cf88384a42870ef695294a0117ab3bfdd26ba69c95bd2b02a63b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540878"
---
# <a name="avenccommonqualityvsspeed-property"></a>AVEncCommonQualityVsSpeed 屬性

指定編碼品質與速度之間的取捨。 此屬性在所有速率控制模式中都是有效的。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonQualityVsSpeed**

## <a name="property-value"></a>屬性值

這個屬性的值具有下列範圍。



| 值 | 描述                      |
|-------|----------------------------------|
| 0     | 較低的品質、更快速的編碼方式。  |
| 100   | 品質較高、速度較慢的編碼。 |



 

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

 

 




