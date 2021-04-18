---
title: ScriptFile
description: ScriptFile 屬性會指定隨附 JScript 檔案的檔案名。
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- ScriptFile Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976179"
---
# <a name="viewscriptfile"></a>ScriptFile

**ScriptFile** 屬性會指定隨附 JScript 檔案的檔案名。

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>可能的值

這個屬性是僅限寫入的 **字串** ，沒有預設值。 多個 JScript 檔案的檔案名會以分號分隔。 開頭和後面不應出現空格和分號。

## <a name="remarks"></a>備註

指定檔案中的程式碼可供視圖中的任何事件處理常式使用。 多個視圖中的事件處理常式所使用的程式碼，可以放在與面板定義檔同名的檔案中，但是使用 .js 副檔名，而不是 wms 副檔名。 此檔案會自動載入，且不需要在外觀定義檔中指定。

## <a name="examples"></a>範例


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VIEW 元素**](view-element.md)
</dt> </dl>

 

 





