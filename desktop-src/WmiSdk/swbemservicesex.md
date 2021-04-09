---
description: 擴充 SWbemServices 的功能。
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: 'SWbemServicesEx 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114856"
---
# <a name="swbemservicesex-object"></a>SWbemServicesEx 物件

**SWbemServicesEx** 物件會擴充 [**SWbemServices**](swbemservices.md)的功能。 [**Put**](swbemservicesex-put.md)和 [**PutAsync**](swbemservicesex-putasync.md)方法可讓您將類別或實例儲存至多個命名空間，或儲存至與建立實例的命名空間不同的命名空間。 VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立這個物件。

## <a name="members"></a>成員

**SWbemServicesEx** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**SWbemServicesEx** 物件有這些方法。



| 方法                                       | 描述                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**把**](swbemservicesex-put.md)           | 將物件儲存至系結至 **SWbemServicesEx** 物件的命名空間，並傳回 [**SWbemObjectPath**](swbemobjectpath.md) 物件，其中包含寫入資料的物件路徑。<br/> |
| [**PutAsync**](swbemservicesex-putasync.md) | 以非同步方式將物件儲存到命名空間。<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>備註

此類別中的方法可以在半同步模式或非同步模式中呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ ISWbemServicesEx<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemServicesEx<br/>                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

