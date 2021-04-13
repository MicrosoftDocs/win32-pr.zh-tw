---
description: 將字串 FILETIME 格式的日期轉換為 CIM 日期時間格式。
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: 'SWbemDateTime. SetFileTime 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114877"
---
# <a name="swbemdatetimesetfiletime-method"></a>SWbemDateTime. SetFileTime 方法

[**SWbemDateTime**](swbemdatetime.md)物件的 **SetFileTime** 方法會將字串 **FILETIME** 格式的日期轉換為 [CIM 日期時間](date-and-time-format.md)格式。

**FILETIME** 格式是64位的日期時間結構，表示自1月 1 1601 日開始起算的 100-毫微秒單位數。 Windows Management Instrumentation (WMI) 會將 **FILETIME** 值視為不帶正負號64位數位的字串表示。

如需語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strFileTime* \[在\]
</dt> <dd>

用來設定物件的 **FILETIME** 值。

</dd> <dt>

*bIsLocal* \[在中，選擇性\]
</dt> <dd>

若 **為 TRUE**，則會將 *strFileTime* 視為當地時間。 國際標準時間 (UTC) 屬性包含轉換成正確 UTC 位移的本地時間。 當 *bIsLocal* 為 **FALSE** 時，會將 *strFileTime* 直接轉換為 UTC 值，位移為 0 (零) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **SetFileTime** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列清單中的錯誤碼。

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021) 
</dt> <dd>

*StrFileTime* 的格式無效。

</dd> </dl>

## <a name="remarks"></a>備註

成功呼叫 **SetFileTime** 之後， [**日期時間**](datetime.md) 值一律會轉譯為絕對 (**Datetime**) 值，而且 [**IsInterval**](swbemdatetime-isinterval.md) 會設定為 **FALSE**。

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

[**SWbemDateTime.SetVarDate**](swbemdatetime-setvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

