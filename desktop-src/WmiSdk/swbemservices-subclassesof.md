---
description: 傳回 Swbemobjectset 搭配使用物件。
ms.assetid: cfe08956-7215-4e2e-a279-6e86f14e5c27
ms.tgt_platform: multiple
title: 'SWbemServices. SubclassesOf 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 49b89b011b8e6933511de220473a0562ebda439bc2a080bf9082db1b5b84e49a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794418"
---
# <a name="swbemservicessubclassesof-method"></a>SWbemServices. SubclassesOf 方法

[**SWbemServices**](swbemservices.md)物件的 **SubclassesOf** 方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md)物件。 此物件是指定類別的子類別集合。 傳回之集合中的專案可以使用標準的收集方法來取得。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

這個方法僅適用于類別物件。

方法會在半同步模式中呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObjectSet = .SubclassesOf( _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strSuperclass* \[選\]
</dt> <dd>

指定父類別名稱。 只有這個類別的子類別會在列舉值中傳回。 如果您將此參數保留空白，而且如果 *iFlags* 為 **wbemQueryFlagShallow**，則只會傳回最上層類別 (也就是沒有父類別的類別) 。 如果這個參數是空白的，而且 *iFlags* 是 **wbemQueryFlagDeep** ，則會傳回命名空間內的所有類別。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

決定呼叫列舉的詳細程度。 此參數的預設值為 **wbemFlagReturnImmediately** 和 **wbemQueryFlagDeep**。 此參數可接受下列值。

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow * * * (1 (0x1) ) 


</dt> <dd>

強制列舉只包含指定之父類別的直屬子類別。

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep * * * (0 (0x0) ) 


</dt> <dd>

此參數的預設值。 此值會強制遞迴列舉至所有衍生自指定父類別的子類別。 列舉中不會傳回父類別。

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * (16 (0x10) ) 


</dt> <dd>

導致呼叫立即返回。

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * (0 (0x0) ) 


</dt> <dd>

導致此呼叫封鎖，直到呼叫完成為止。 此旗標會在同步模式中呼叫方法。

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * (131072 (0x20000) ) 


</dt> <dd>

讓 WMI 以基類定義傳回類別修訂資料。 如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表可由提供者服務來處理要求的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。

## <a name="error-codes"></a>錯誤碼

**SubclassesOf** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

> [!Note]  
> 具有零個元素的傳回集合不是錯誤。

 

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010) 
</dt> <dd>

指定的類別不存在。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="examples"></a>範例

下列 PowerShell 範例示範如何在遠端系統上取出類別的子類別。


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
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

[**Swbemobjectset 搭配使用**](swbemobjectset.md)
</dt> </dl>

 

 




