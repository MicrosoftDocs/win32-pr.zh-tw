---
title: AmbientAttributes。已啟用
description: Enabled 屬性會指定或抓取值，指出控制項是否已啟用或停用。
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- AmbientAttributes 已啟用 Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988659"
---
# <a name="ambientattributesenabled"></a>AmbientAttributes。已啟用

**Enabled** 屬性會指定或抓取值，指出控制項是否已啟用或停用。

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述               |
|-------|---------------------------|
| true  | 預設值。 控制項已啟用。 |
| false | 控制項已停用。         |



 

## <a name="remarks"></a>備註

如果已啟用控制項，它可能會有索引標籤停止，並會接收所有環境事件。 停用時，控制項就不會有索引標籤停止，而且不會收到任何對它引發的環境滑鼠或鍵盤事件。 不過 (，它將會繼續接收所有其他引發的環境事件。 ) 

子 **視圖** 元素不支援這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> </dl>

 

 





