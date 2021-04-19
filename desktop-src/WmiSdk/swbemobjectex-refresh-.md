---
description: 更新具有效能提供者所提供之資料的物件資料，例如效能計數器類別。 您可以更快速地取得更新的資料，而不需要呼叫 SWbemServices。 Get \_ 。
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: 'SWbemObjectEx.Refresh_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974188"
---
# <a name="swbemobjectexrefresh_-method"></a>SWbemObjectEx \_ 方法

[**SWbemObjectEx**](swbemobjectex.md)的 **Refresh \_** 方法會更新具有效能提供者所提供之資料的物件資料，例如 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)。 您可以更快速地取得更新的資料，而不需要呼叫 [**SWbemServices \_ 。 Get**](swbemservices-get.md)。

如需此語法的詳細資訊，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

保留的作業旗標（如果有指定）必須是 0 (零) 。

</dd> <dt>

*objWbemNamedValueSet* \[在中，選擇性\]
</dt> <dd>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，它會設定作業的內容。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **Refresh \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

提供者在內部失敗，即使作業有效也一樣。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

找不到要求的格式。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

呼叫的其中一個參數不正確。

</dd> <dt>

**wbemErrRefresherBusy** -2147749975 (0x80041057) 
</dt> <dd>

重新整理器專注於進行其他作業。

</dd> <dt>

**wbemPartialResults** -2147745808 (0x80040010) 
</dt> <dd>

並非所有的物件、列舉值或嵌套的刷新器都已成功更新。 這項傳回不是錯誤，而是表示作業不完整。

</dd> </dl>

## <a name="examples"></a>範例

下列腳本程式碼範例示範如何取得系統進程的原始和處理後效能計數器。 物件會每兩秒重新整理一次，並顯示內容。


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> </dl>

 

