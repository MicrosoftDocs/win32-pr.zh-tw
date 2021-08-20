---
description: SWbemQualifierSet 物件是 SWbemQualifier 物件的集合。
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: 'SWbemQualifierSet 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ed8ec4c244c2ecc2ab2f14200744d4f6d7c78a7891638b96e0b2efb71c408ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921977"
---
# <a name="swbemqualifierset-object"></a>SWbemQualifierSet 物件

**SWbemQualifierSet** 物件是 [**SWbemQualifier**](swbemqualifier.md)物件的集合。 使用 [**Add**](swbemqualifierset-add.md) 方法將專案加入至集合，使用 [**Item**](swbemqualifierset-item.md) 方法從集合中取出，並使用 [**Remove**](swbemqualifierset-remove.md) 方法從集合中移除。 VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。

如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

組成 **SWbemQualifierSet** 集合的 [**SWbemQualifier**](swbemqualifier.md)物件會描述附加至 WMI 類別、實例、方法或方法參數的限定詞。

## <a name="members"></a>成員

**SWbemQualifierSet** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemQualifierSet** 物件有這些方法。



| 方法                                     | 描述                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**添加**](swbemqualifierset-add.md)       | 將 [**SWbemQualifier**](swbemqualifier.md) 物件加入至 **SWbemQualifierSet** 集合。<br/> |
| [**項目**](swbemqualifierset-item.md)     | 從集合傳回名為 [**SWbemQualifier**](swbemqualifier.md) 的物件。<br/>             |
| [**移除**](swbemqualifierset-remove.md) | 從集合中刪除已命名的辨識符號。<br/>                                                   |



 

### <a name="properties"></a>屬性

**SWbemQualifierSet** 物件具有這些屬性。



| 屬性                                            | 存取類型          | 描述                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**計數**](swbemqualifierset-count.md)<br/> | 唯讀<br/> | 包含 **SWbemQualifierSet** 集合中的專案數。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




