---
description: '\_SWbemLastError 物件的 Path 屬性會傳回 SWbemObjectPath 物件，此物件代表目前類別或實例的物件路徑。 這個屬性可以做為參數傳遞給需要物件路徑的方法。'
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: 'SWbemLastError.Path_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5503d11d5c73f2bf955b25da9b5dbccbc18d41b9bc9b84bc3235993562938b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612198"
---
# <a name="swbemlasterrorpath_-property"></a>SWbemLastError 路徑 \_ 屬性

[**SWbemLastError**](swbemlasterror.md)物件的 **Path \_** 屬性會傳回 [**SWbemObjectPath**](swbemobjectpath.md)物件，此物件代表目前類別或實例的物件路徑。 這個屬性可以做為參數傳遞給需要物件路徑的方法。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

只有傳回之 [**SWbemObjectPath**](swbemobjectpath.md)實例的 [**Class**](swbemobjectpath-class.md)屬性可以修改。 如果您嘗試修改任何其他屬性，或嘗試呼叫 [**SetAsClass**](swbemobjectpath-setasclass.md) 或 [**SetAsSingleton**](swbemobjectpath-setassingleton.md) 方法，則會出現 **wbemErrReadOnly** 錯誤。

因此，您無法修改 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，此物件是所傳回 [**SWbemObjectPath**](swbemobjectpath.md)實例之索引 [**鍵**](swbemobjectpath-keys.md)屬性的值。 如果您嘗試對此值呼叫 [**Add**](swbemnamedvalueset-add.md)、 [**Remove**](swbemnamedvalueset-remove.md)或 [**DeleteAll**](swbemnamedvalueset-deleteall.md) 方法，就會收到 **wbemErrReadOnly** 錯誤。 此外，您無法修改從此集合取得的任何 [**SWbemNamedValue**](swbemnamedvalue.md) 。 嘗試修改 [**Value**](swbemnamedvalue-value.md) 屬性會傳回相同的錯誤碼。

但是，如果您呼叫 [**SWbemObject \_**](swbemobject-clone-.md)來建立複本，就可以完全修改複製的 [**Path \_**](swbemobject-path-.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




