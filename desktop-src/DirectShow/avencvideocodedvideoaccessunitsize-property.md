---
description: 指定影片存取單位的大小（以位元組為單位）。 這個屬性只適用于變數的位元速率 (VBR) 控制項模式。
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: 'AVEncVideoCodedVideoAccessUnitSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be3a6e499749d862fdcc63f28b1a9a02f476d1c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935640"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a>AVEncVideoCodedVideoAccessUnitSize 屬性

指定影片存取單位的大小（以位元組為單位）。 這個屬性只適用于變數的位元速率 (VBR) 控制項模式。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**

## <a name="property-value"></a>屬性值

這個屬性會以值範圍的形式傳回。 若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。

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

 

 




