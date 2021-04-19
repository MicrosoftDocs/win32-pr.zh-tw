---
title: WordWrap
description: WordWrap 屬性會指定或抓取值，指出是否啟用或停用自動換行。
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- WordWrap Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996025"
---
# <a name="textwordwrap"></a>WordWrap

**WordWrap** 屬性會指定或抓取值，指出是否啟用或停用自動換行。

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | 已啟用自動換行。                                                                             |
| false | 預設值。 已停用自動換行。 如果文字無法容納在控制項內，則會裁剪文字。 |



 

## <a name="remarks"></a>備註

文字控制項不會將單字分開。 如果單字延伸超過控制項的寬度，則會使用自動換行將單字移到下一行。 如果單一單字的長度超過控制項寬度，則會裁剪該單字，並佔用一行。

如果未指定 **width** 屬性， **wordWrap** 會被忽略，而文字控制項會調整大小，而不是換行文字。

如果特定位置需要換行，必須使用 "& \# 13;" 或 "r" 在值中明確指定 \\ 。 如果直接指定值時使用第二個表單，則字串的前面必須加上 "JScript："，且實際的值必須以單引號括住，如下所示。 如果是從事件處理常式內動態設定值，就不需要這麼做。

如果 [ **wordWrap** ] 設定為 [true]，而且未指定 [ **工具提示** ]，則工具提示會顯示 [ **值** ] 屬性的完整文字。 如果沒有任何需要的工具提示，請將 **tooltip** 設定為 "" (空白字串) 。

## <a name="examples"></a>範例


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AmbientAttributes 寬度**](ambientattributes-width.md)
</dt> <dt>

[**TEXT 元素**](text-element.md)
</dt> <dt>

[**文字。工具提示**](text-tooltip.md)
</dt> <dt>

[**TEXT。值**](text-value.md)
</dt> </dl>

 

 





