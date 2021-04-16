---
description: 您可以使用 SWbemMethod 物件的屬性來檢查 WMI 物件的單一方法定義。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: 'SWbemMethod 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512985"
---
# <a name="swbemmethod-object"></a>SWbemMethod 物件

您可以使用 **SWbemMethod** 物件的屬性來檢查 WMI 物件的單一方法定義。 VBScript **CreateObject** 呼叫無法建立這個物件。

此物件可以用來檢查方法的定義。 若要叫用方法，您應該使用直接存取 (參閱在 [**SWbemObject**](swbemobject.md) (上 [操作類別和實例資訊](manipulating-class-and-instance-information.md)) 這是建議的機制) 物件或 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)呼叫。

> [!Note]  
> 在此版本的 API 中，不支援方法資訊的寫入權限。 如果您想要定義方法或修改現有的方法定義，可以在 MOF 檔案中定義方法變更，然後使用 [MOF 編譯器](compiling-mof-files.md)來提交變更。 或者，使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)。

 

## <a name="members"></a>成員

**SWbemMethod** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SWbemMethod** 物件具有這些屬性。



| 屬性                                                      | 存取類型          | Description                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**InParameters**](swbemmethod-inparameters.md)<br/>   | 唯讀<br/> | [**SWbemObject**](swbemobject.md)物件，其屬性會定義此方法的輸入參數。<br/>              |
| [**Name**](swbemmethod-name.md)<br/>                   | 唯讀<br/> | 方法的名稱。<br/>                                                                                                     |
| [**起源**](swbemmethod-origin.md)<br/>               | 唯讀<br/> | 方法的原始類別。<br/>                                                                                        |
| [**OutParameters**](swbemmethod-outparameters.md)<br/> | 唯讀<br/> | [**SWbemObject**](swbemobject.md)物件，其屬性會定義此方法的 out 參數和傳回型別。<br/> |
| [**限定詞\_**](swbemmethod-qualifiers-.md)<br/>    | 唯讀<br/> | [**SWbemQualifierSet**](swbemqualifierset.md)物件，其中包含這個方法的限定詞。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




