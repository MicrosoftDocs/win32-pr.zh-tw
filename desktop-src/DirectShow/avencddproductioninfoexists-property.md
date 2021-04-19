---
description: 指定杜比數位音訊串流中的音訊生產資訊旗標。 此屬性適用于杜比數位音訊編碼器。
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: 'AVEncDDProductionInfoExists 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973357"
---
# <a name="avencddproductioninfoexists-property"></a>AVEncDDProductionInfoExists 屬性

指定杜比數位音訊串流中的音訊生產資訊旗標。 此屬性適用于杜比數位音訊編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncDDProductionInfoExists**

## <a name="remarks"></a>備註

如果值為 **VARIANT \_ TRUE**，混合層級和房間型別設定都有效。 使用 [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) 和 [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) 屬性來指定這些設定。

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

 

 




