---
description: 指定 DC 係數的精確度（以位為單位）。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: 'AVEncMPVIntraDCPrecision 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e50d4a6b222d9860a16216a1395b9f5a2b10d23e6242315a61e8224d37810c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276128"
---
# <a name="avencmpvintradcprecision-property"></a>AVEncMPVIntraDCPrecision 屬性

指定 DC 係數的精確度（以位為單位）。 這個屬性會套用至 MPEG 視頻編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPVIntraDCPrecision**

## <a name="property-value"></a>屬性值

這個屬性具有線性範圍的值。 若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。

## <a name="remarks"></a>備註

這個屬性的一般範圍是8到11位。 如果值為零，則編碼器會選取有效位數。

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

 

 




