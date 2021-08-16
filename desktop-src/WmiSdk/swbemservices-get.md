---
description: 根據物件路徑，抓取屬於類別定義或實例的物件。
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: 'SWbemServices： Get 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d448d92cddf24e98f05cf023116e7087ad8cc3dcd310b7ccd3657571ee7650ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312657"
---
# <a name="swbemservicesget-method"></a>SWbemServices. Get 方法

[**SWbemServices**](swbemservices.md)物件的 **Get** 方法會根據物件路徑，來抓取物件（也就是類別定義或實例）。 這個方法只會從與目前 **SWbemServices** 物件相關聯的命名空間中，抓取物件。

方法是在同步模式中呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strObjectPath* \[選\]
</dt> <dd>

字串，包含要取得之物件的物件路徑。 如果這個值是空的，則傳回的空物件可以成為新的類別。 如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

判斷查詢行為的整數。 此參數可接受下列值。

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * (131072 (0x20000) ) 


</dt> <dd>

讓 WMI 以基類定義傳回類別修訂資料。 如需修改過的限定詞的詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，這個方法會傳回代表所要求之物件的 [**SWbemObject**](swbemobject.md) 物件。

## <a name="error-codes"></a>錯誤碼

完成 **Get** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者沒有存取該物件的許可權。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrInvalidObjectPath** -2147749946 (0x8004103A) 
</dt> <dd>

指定的路徑無效。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

找不到要求的物件。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="remarks"></a>備註

不同于 [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) 和 [**InstancesOf**](swbemservices-instancesof.md) 方法，Get 方法一律會傳回代表受 WMI 管理之資源的特定實例的 [**SWbemObject**](swbemobject.md) 。 若要使用 Get 方法取得受 WMI 管理之資源的特定實例，您必須藉由將方法傳遞給物件路徑，來指示要取得的實例，如下列腳本所示。


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



您可以使用這個方法來取得 [*單一*](gloss-s.md)物件（例如 [**\_ \_ CIMOMIdentification**](--cimomidentification.md)），其中包含執行之 WMI 安裝的版本資訊。

您可以使用 [CIM Studio](further-information.md) 之類的查看工具來檢查存放庫，以確認新的類別和實例出現。 如需從存放庫中移除類別和實例的範例，請參閱 [**SWbemServices。刪除**](swbemservices-delete.md)或 [**\_ SWbemObject。**](swbemobject-delete-.md)

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

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

 




