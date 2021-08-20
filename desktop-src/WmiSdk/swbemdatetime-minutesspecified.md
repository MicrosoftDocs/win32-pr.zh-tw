---
description: 指出 CIM datetime 值中的分鐘元件是否包含間隔或萬用字元值。
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: 'SWbemDateTime. MinutesSpecified 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a780d9bed3224e1b9be006a2bdf94b2b411951ceb3ef4d82a439ba5ec451fd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992188"
---
# <a name="swbemdatetimeminutesspecified-property"></a>SWbemDateTime. MinutesSpecified 屬性

[**SWbemDateTime**](swbemdatetime.md)物件的 **MinutesSpecified** 屬性是一個布林值，指出 CIM datetime 值中的分鐘元件是否包含間隔或萬用字元值。 如果 **MinutesSpecified** 為 **TRUE** ，而且 [**ISINTERVAL**](swbemdatetime-isinterval.md) 為 **FALSE** (表示 CIM datetime 值沒有萬用字元) ，則 [**SWbemDateTime. 分鐘**](swbemdatetime-minutes.md) 包含日期值。 包含間隔的日期時間值不能轉換成 **VT \_ 日期** 格式或 **FILETIME** 格式。 如果 [**HoursSpecified**](swbemdatetime-hoursspecified.md) 為 **FALSE** 且 **IsInterval** 為 **TRUE**，則 **SWbemDateTime. 分鐘** 包含間隔。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a>屬性值

## <a name="examples"></a>範例

如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。 如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemDateTime 分鐘**](swbemdatetime-minutes.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




