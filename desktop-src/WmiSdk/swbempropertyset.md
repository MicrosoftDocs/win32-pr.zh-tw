---
description: 內含物件是 Swbempropertyset 物件的集合。
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: '內含物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983904"
---
# <a name="swbempropertyset-object"></a>內含物件

**內含** 物件是 [**swbempropertyset**](swbemproperty.md)物件的集合。 您可以使用 [**add**](swbempropertyset-add.md) 方法將專案加入集合、使用 [**Item**](swbempropertyset-item.md) 方法從集合取出專案，以及使用 [**remove**](swbempropertyset-remove.md) 方法從集合中移除專案。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。 VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。

組成 **內含** 集合的 [**swbempropertyset**](swbemproperty.md)物件是用來描述單一 WMI 類別或實例的屬性。

## <a name="members"></a>成員

**內含** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**內含** 物件有這些方法。



| 方法                                    | 描述                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**添加**](swbempropertyset-add.md)       | 將 [**swbempropertyset**](swbemproperty.md) 物件加入至 **內含** 集合。<br/>                        |
| [**項目**](swbempropertyset-item.md)     | 從集合中取得名為 [**swbempropertyset**](swbemproperty.md) 的。 這是這個物件的預設方法。<br/> |
| [**移除**](swbempropertyset-remove.md) | 從集合中刪除 [**swbempropertyset**](swbemproperty.md) 物件。<br/>                                        |



 

### <a name="properties"></a>屬性

**內含** 物件具有這些屬性。



| 屬性                                           | 存取類型          | Description                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [**計數**](swbempropertyset-count.md)<br/> | 唯讀<br/> | **內含** 集合中的專案數。<br/> |



 

## <a name="examples"></a>範例

下列 VBScript 範例將示範如何在屬性被覆寫時， [**內含**](swbempropertyset-remove.md) 會傳回 **wbemErrResetToDefault** 。


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ 內含<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemPropertySet<br/>                                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




