---
description: 取得或設定值，這個值表示 datetime 值的小時元件。
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: 'SWbemDateTime Hours 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4ebe2cf5d25efd474268cea1459718f4741e4c4c698cbdbe65cc765cc17c2ae7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030378"
---
# <a name="swbemdatetimehours-property"></a>SWbemDateTime Hours 屬性

[**SWbemDateTime**](swbemdatetime.md)物件的 **hours** 屬性會取得或設定值，這個值表示 datetime 值的小時元件。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a>屬性值

## <a name="error-codes"></a>錯誤碼

當您取得或設定 **Hours** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B) 
</dt> <dd>

值不在0到23的範圍內。

</dd> </dl>

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

[**SWbemDateTime.HoursSpecified**](swbemdatetime-hoursspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

