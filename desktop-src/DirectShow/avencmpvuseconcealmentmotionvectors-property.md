---
description: 指定編碼器是否使用 concealment 的動作向量。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: 8b47a007-525c-4d02-8723-d6217600041e
title: 'AVEncMPVUseConcealmentMotionVectors 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d5a9316e257ebbbb8ba72ce027fe4c8c84db92b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935665"
---
# <a name="avencmpvuseconcealmentmotionvectors-property"></a>AVEncMPVUseConcealmentMotionVectors 屬性

指定編碼器是否使用 concealment 的動作向量。 這個屬性會套用至 MPEG 視頻編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPVUseConcealmentMotionVectors**

## <a name="remarks"></a>備註

如果值為 **VARIANT \_ TRUE**，編碼器會使用 concealment 的動作向量。

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

 

 




