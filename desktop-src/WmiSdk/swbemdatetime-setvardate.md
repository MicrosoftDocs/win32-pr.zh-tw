---
description: 將 VT 日期格式的日期轉換 \_ 為 CIM 日期時間格式。
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: 'SWbemDateTime. SetVarDate 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 56d193bd2faffd51507ec4a913c7ee068b055dcf45ca756e801431659768c47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050096"
---
# <a name="swbemdatetimesetvardate-method"></a>SWbemDateTime. SetVarDate 方法

[**SWbemDateTime**](swbemdatetime.md)物件的 **SetVarDate** 方法會將 **VT \_ 日期** 格式的日期轉換為 [CIM 日期時間](date-and-time-format.md)格式。

**VT \_ 日期** 值是 Visual Basic 和 ActiveX 使用的 variant datetime 值。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vdate* \[在\]
</dt> <dd>

要設定物件的變異日期值。 此參數必須是 **VT \_ 日期** 格式。

</dd> <dt>

*bIsLocal* \[在中，選擇性\]
</dt> <dd>

若為 **TRUE**，則會將 *vdate* 視為當地時間，而國際標準時間 (UTC) 屬性包含轉換成正確 UTC 位移的當地時間。 當 *bIsLocal* 為 **FALSE** 時，會將 *vdate* 直接轉換為 UTC 值，且位移為零 (0) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **SetVarDate** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列清單中的錯誤碼。

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021) 
</dt> <dd>

*Vdate* 的格式無效。

</dd> </dl>

## <a name="remarks"></a>備註

成功呼叫 **SetVarDate** 之後，會將 [**DATETIME**](datetime.md) 值視為絕對 datetime 值，而不是間隔，而 [**IsInterval**](swbemdatetime-isinterval.md) 屬性會設定為 **FALSE**。

內建 Visual Basic 或 VBScript 函數 [CDate](/previous-versions//2dt118h2(v=vs.85))以 **VT \_ 日期** 格式提供 [**日期時間**](datetime.md)值給 **SetVarDate** 輸入。

## <a name="examples"></a>範例

如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。 如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。

在 TechNet 資源庫中將 [日期轉換為 WMI Date-Time 格式](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript 程式碼範例使用 SetVarDate，將一般日期時間值轉換成 UTC 日期時間格式。

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

[**SWbemDateTime.SetFileTime**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

