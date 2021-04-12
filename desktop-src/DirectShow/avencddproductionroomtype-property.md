---
description: 指定杜比數位音訊串流的房間類型。 此屬性適用于杜比數位音訊編碼器。
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: 'AVEncDDProductionRoomType 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109633"
---
# <a name="avencddproductionroomtype-property"></a>AVEncDDProductionRoomType 屬性

指定杜比數位音訊串流的房間類型。 此屬性適用于杜比數位音訊編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncDDProductionRoomType**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) 列舉的成員。

## <a name="remarks"></a>備註

*房間類型* 指的是在生產期間使用的空間大小。 如果設定此屬性，請將 [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) 屬性設定為 **TRUE**。

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

 

