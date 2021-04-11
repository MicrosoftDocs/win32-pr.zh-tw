---
description: 指定巨大區塊內的色度量化矩陣。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: 9da6130f-c064-4b6b-b0ab-ba99118fd249
title: 'AVEncMPVQuantMatrixChromaIntra 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7253a3064acbff74ce22134a40a52d87c78113a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108625"
---
# <a name="avencmpvquantmatrixchromaintra-property"></a>AVEncMPVQuantMatrixChromaIntra 屬性

指定巨大區塊內的色度量化矩陣。 這個屬性會套用至 MPEG 視頻編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**BSTR** (**VT \_ bstr**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPVQuantMatrixChromaIntra**

## <a name="property-value"></a>屬性值

這個屬性的值是一個字串，其中包含編碼為十六進位值字串的 64 8 位係數 (128 個字元) 。

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

 

 




