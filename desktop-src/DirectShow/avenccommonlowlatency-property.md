---
description: 指定是否應將輸出資料流程結構化，以便編碼的資料流程具有低解碼延遲。
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: 'AVEncCommonLowLatency 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187556"
---
# <a name="avenccommonlowlatency-property"></a>AVEncCommonLowLatency 屬性

指定是否應將輸出資料流程結構化，以便編碼的資料流程具有低解碼延遲。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonLowLatency**

## <a name="remarks"></a>備註

解碼延遲會定義為必須緩衝的資料量。 例如，在 MPEG 影片編碼器上將此屬性設定為 **VARIANT \_ TRUE** 會限制編碼器可使用的 GOP 結構類型。

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

 

 




