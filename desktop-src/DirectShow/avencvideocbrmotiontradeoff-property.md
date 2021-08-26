---
description: 指定移動與靜止影像之間的取捨。 這個屬性只適用于常數的位元速率 (CBR) 控制模式。
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: 'AVEncVideoCBRMotionTradeoff 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d3db1f310de6468b57d469fbf699919ab86429e7242344622ca498b9e59f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057938"
---
# <a name="avencvideocbrmotiontradeoff-property"></a>AVEncVideoCBRMotionTradeoff 屬性

指定移動與靜止影像之間的取捨。 這個屬性只適用于常數的位元速率 (CBR) 控制模式。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoCBRMotionTradeoff**

## <a name="property-value"></a>屬性值

這個屬性的值具有下列範圍。



| 值 | 描述               |
|-------|---------------------------|
| 0     | 針對靜止影像優化 |
| 100   | 優化動作。      |



 

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

 

 




