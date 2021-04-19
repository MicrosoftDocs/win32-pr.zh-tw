---
description: 布林值，指出 CIM 日期時間值中的 year 元件是否包含間隔或萬用字元值。
ms.assetid: afac0a08-7bd0-42f1-b5a7-8664f9db8615
ms.tgt_platform: multiple
title: 'SWbemDateTime. YearSpecified 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.YearSpecified
- ISWbemDateTime.YearSpecified
- ISWbemDateTime.get_YearSpecified
- ISWbemDateTime.put_YearSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3ad6ae5b120c2b38d7b6170951ef30b3b19f5295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978878"
---
# <a name="swbemdatetimeyearspecified-property"></a>SWbemDateTime. YearSpecified 屬性

[**SWbemDateTime**](swbemdatetime.md)物件的 **YearSpecified** 屬性是一個布林值，指出 CIM datetime 值中的 year 元件是否包含間隔或萬用字元值。 如果 **YearSpecified** 為 **TRUE** 且 [**IsInterval**](swbemdatetime-isinterval.md) 為 **FALSE**，則 [**SWbemDateTime. Year**](swbemdatetime-year.md) 會包含日期時間值。 包含間隔的日期時間值不能轉換成 **VT \_ 日期** 格式或 **FILETIME** 格式。 如果 **YearSpecified** 為 **FALSE** 且 **IsInterval** 為 **TRUE**，則 **SWbemDateTime. Year** 包含間隔。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.YearSpecified As Boolean
```



## <a name="property-value"></a>屬性值

## <a name="examples"></a>範例

如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。 如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemDateTime Year**](swbemdatetime-year.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




