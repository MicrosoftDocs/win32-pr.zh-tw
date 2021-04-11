---
description: 指定編碼緩衝區的初始層級（以位為單位）。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: 'AVEncCommonBufferInLevel 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109669"
---
# <a name="avenccommonbufferinlevel-property"></a>AVEncCommonBufferInLevel 屬性

指定編碼緩衝區的初始層級（以位為單位）。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonBufferInLevel**

## <a name="property-value"></a>屬性值

這個屬性具有線性範圍的值。 若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。

## <a name="remarks"></a>備註

針對 MPEG 影片，這個屬性會定義初始的影片緩衝區驗證器 (VBV) 飽和度。 它支援在編碼期間串連資料流程。

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

 

 




