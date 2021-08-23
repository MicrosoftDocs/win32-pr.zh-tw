---
description: 指定編碼器是否產生開啟的圖片群組 (Gop) 或已關閉的 Gop。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: 'AVEncMPVGOPOpen 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6be085bde5588fecd5a2274d442f38d4198702475f3ed13c7bb3a5569687375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540898"
---
# <a name="avencmpvgopopen-property"></a>AVEncMPVGOPOpen 屬性

指定編碼器是否產生開啟的圖片群組 (Gop) 或已關閉的 Gop。 這個屬性會套用至 MPEG 視頻編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPVGOPOpen**

## <a name="property-value"></a>屬性值



| 值          | 描述 |
|----------------|-------------|
| VARIANT \_ FALSE | 封閉式 Gop |
| VARIANT \_ TRUE  | 開啟 Gop   |



 

## <a name="remarks"></a>備註

開啟的 GOP 包含從上一個 GOP 參考框架的差異框架。 封閉的 GOP 不包含任何參考先前 GOP 的 delta 框架。

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

 

 




