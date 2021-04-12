---
description: '\_SWbemObject 物件的 Path 屬性會傳回 SWbemObjectPath 物件，此物件代表目前類別或實例的物件路徑。 這個屬性可以做為參數傳遞給需要物件路徑的方法。'
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: 'SWbemObject.Path_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193446"
---
# <a name="swbemobjectpath_-property"></a>SWbemObject 路徑 \_ 屬性

[**SWbemObject**](swbemobject.md)物件的 **Path \_** 屬性會傳回 [**SWbemObjectPath**](swbemobjectpath.md)物件，此物件代表目前類別或實例的物件路徑。 這個屬性可以做為參數傳遞給需要物件路徑的方法。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

只有傳回之 [**SWbemObjectPath**](swbemobjectpath.md)實例的 [**Class**](swbemobjectpath-class.md)屬性可以修改。 如果您嘗試修改任何其他屬性，或嘗試呼叫 [**SetAsClass**](swbemobjectpath-setasclass.md) 或 [**SetAsSingleton**](swbemobjectpath-setassingleton.md)方法，您將會收到 **wbemErrReadOnly** 錯誤。

因此，您無法修改 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，此物件是所傳回 [**SWbemObjectPath**](swbemobjectpath.md)實例之索引 [**鍵**](swbemobjectpath-keys.md)屬性的值。 如果您嘗試對此值呼叫 [**Add**](swbemnamedvalueset-add.md)、 [**Remove**](swbemnamedvalueset-remove.md)或 [**DeleteAll**](swbemnamedvalueset-deleteall.md) 方法，將會收到 wbemErrReadOnly 錯誤。 此外，您無法修改從此集合取得的任何 [**SWbemNamedValue**](swbemnamedvalue.md) 。 嘗試修改 **Value** 屬性會傳回相同的錯誤碼。

但是，如果您呼叫 [**SWbemObject \_**](swbemobject-clone-.md)來建立複本，則複本的 [**SWbemObjectPath. Path**](swbemobjectpath-path.md)屬性可完全修改。

## <a name="examples"></a>範例

下列程式碼範例取自 TechNet 資源庫中的 [所有 Wmi Cimv2 類別](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) ，並使用 Path \_ 屬性列出所有 wmi cimv2 類別。


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




