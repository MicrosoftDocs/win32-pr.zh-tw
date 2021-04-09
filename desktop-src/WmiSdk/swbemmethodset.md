---
description: SWbemMethodSet 物件是 SWbemMethod 物件的集合。 使用 Item 方法抓取專案。 如需詳細資訊，請參閱存取集合。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: 'SWbemMethodSet 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849563"
---
# <a name="swbemmethodset-object"></a>SWbemMethodSet 物件

**SWbemMethodSet** 物件是 [**SWbemMethod**](swbemmethod.md)物件的集合。 使用 [**Item**](swbemmethodset-item.md) 方法抓取專案。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。 VBScript **CreateObject** 呼叫無法建立這個物件。

> [!Note]  
> 在此版本的 API 中，不支援方法資訊的寫入權限。 如果您想要定義方法或修改現有的方法定義，可以在 MOF 檔案中定義方法變更，然後使用 MOF 編譯器來提交變更。 或者，使用 WMI COM API。

 

## <a name="members"></a>成員

**SWbemMethodSet** 物件具有下列類型的成員：

-   [方法](#swbemmethodset-object)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemMethodSet** 物件有這些方法。



| 方法                              | 描述                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Item**](swbemmethodset-item.md) | 從集合中捕獲 [**SWbemMethod**](swbemmethod.md) 物件。 這是這個物件的預設自動化方法。<br/> |



 

### <a name="properties"></a>屬性

**SWbemMethodSet** 物件具有這些屬性。



| 屬性                                         | 存取類型          | Description                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**計數**](swbemmethodset-count.md)<br/> | 唯讀<br/> | 集合中的項目數目<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethodSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemMethodSet<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




