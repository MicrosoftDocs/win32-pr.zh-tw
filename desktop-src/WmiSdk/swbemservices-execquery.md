---
description: SWbemServices.ExecQuery 方法-執行查詢來取出物件。
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecQuery 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3009d2dc88e9987a3559da91eed1aa5aa1b248f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098329"
---
# <a name="swbemservicesexecquery-method"></a>SWbemServices.ExecQuery 方法

[**SWbemServices**](swbemservices.md)物件的 **ExecQuery** 方法會執行查詢來取出物件。 您可以透過傳回的 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合取得這些物件。

這個方法會在半同步模式中呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strQuery* 
</dt> <dd>

必要。 包含查詢文字的字串。 此參數不可以是空白。 如需建立 WMI 查詢字串的詳細資訊，請參閱 [使用 Wql 查詢](querying-with-wql.md) 和 [wql](wql-sql-for-wmi.md) 參考。

</dd> <dt>

*strQueryLanguage* \[選\]
</dt> <dd>

字串，包含要使用的查詢語言。 如果有指定，此值必須是 "WQL"。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

判斷查詢行為的整數，並判斷此呼叫是否立即傳回。 此參數的預設值為 **wbemFlagReturnImmediately**。 此參數可接受下列值。

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * (32 (0x20) ) 


</dt> <dd>

使順向列舉值傳回。 順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional * * * (0 (0x0) ) 


</dt> <dd>

讓 WMI 保留列舉物件的指標，直到用戶端釋放列舉值為止。

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * (16 (0x10) ) 


</dt> <dd>

導致呼叫立即返回。

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * (0 (0x0) ) 


</dt> <dd>

導致此呼叫封鎖，直到查詢完成為止。 此旗標會在同步模式中呼叫方法。

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype * * * (2 (0x2) ) 


</dt> <dd>

用於原型設計。 此旗標會停止進行查詢，並傳回看起來像一般結果物件的物件。

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * (131072 (0x20000) ) 


</dt> <dd>

讓 WMI 以基類定義傳回類別修訂資料。 如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果沒有發生錯誤，這個方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。 這是包含查詢結果集的物件集合。 呼叫端可以使用您所使用之程式設計語言的集合執行來檢查集合。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

## <a name="error-codes"></a>錯誤碼

**ExecQuery** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可以包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者沒有許可權可查看結果集。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017) 
</dt> <dd>

查詢語法無效。

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018) 
</dt> <dd>

不支援要求的查詢語言。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="remarks"></a>備註

**ExecQuery** 是抓取 WMI 資訊最常使用的其中一項呼叫。 **ExecQuery** 的標準呼叫看起來如下所示：


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



請注意，您會使用表示適當命名空間和安全性的標記來建立 [**SWbemServices**](swbemservices.md) 物件，然後透過服務進行 **ExecQuery** 呼叫。 如需更完整的討論，請參閱 [建立 Wmi 腳本](creating-a-wmi-script.md) 和 [列舉 wmi](enumerating-wmi.md)。

如同 [**InstancesOf**](swbemservices-instancesof.md) 方法， **ExecQuery** 方法一律會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合。 因此，您的 WMI 腳本必須列舉集合 ExecQuery 傳回，才能存取集合中的每個受控資源實例，如下所示：


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md)的其他 [**SWbemServices**](swbemservices.md)方法包括 [**AssociatorsOf**](swbemservices-associatorsof.md)、 [**ReferencesTo**](swbemservices-referencesto.md)和 [**SubclassesOf**](swbemservices-subclassesof.md)。

查詢傳回空的結果集並不會發生錯誤。 **ExecQuery** 方法會傳回索引鍵屬性，不論是否在 *strQuery* 引數中要求索引鍵屬性。 如果執行此方法時發生錯誤，而且您未使用 **wbemFlagReturnImmediately** 旗標，則在您嘗試存取傳回的物件集之前，不會設定 [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件。 但是，如果您使用 **wbemFlagReturnWhenComplete** 旗標，則會在呼叫 **ExecQuery** 方法時設定 Err 物件。

WQL 查詢中可使用的 **和** 和 **或** 關鍵字數目有一些限制。 複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 將 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼傳回為 **HRESULT** 值。 WQL 關鍵字的限制取決於查詢的複雜程度。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會尋找本機電腦上的所有磁片磁碟機，並顯示裝置識別碼和磁片磁碟機的類型。


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemServices。 Get**](swbemservices-get.md)
</dt> <dt>

[使用 WQL 查詢](querying-with-wql.md)
</dt> <dt>

[建立 WMI 腳本](creating-a-wmi-script.md)
</dt> <dt>

[列舉 WMI](enumerating-wmi.md)
</dt> </dl>

 

