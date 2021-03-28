---
title: if 陳述式
description: 根據條件運算式的評估，有條件地執行一連串的語句。
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- if 語句 HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104022976"
---
# <a name="if-statement"></a>if 陳述式

根據條件運算式的評估，有條件地執行一連串的語句。



|                                                               |
|---------------------------------------------------------------|
| \[*屬性* \]如果 (*條件* 式 ) {*語句區塊*;} |



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*
</dt> <dd>

可控制如何編譯語句的選擇性參數。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>分支</td>
<td>根據指定的條件，只評估 if 語句的其中一個端。
<blockquote>
[!Note]<br />
當您使用 <a href="dx-graphics-hlsl-sm2.md">著色器模型</a> 2.X 或 <a href="dx-graphics-hlsl-sm3.md">著色器模型 3.0</a>時，每次使用動態分支都會耗用資源。 因此，如果您在以這些設定檔為目標時，過度使用動態分支，您可能會收到編譯錯誤。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>扁平化</td>
<td>評估 if 語句的兩邊，並在兩個結果值之間選擇。</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*條件*
</dt> <dd>

條件 [運算式](dx-graphics-hlsl-expressions.md)。 運算式會進行評估，若為 true，則會執行語句區塊。

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*語句區塊*
</dt> <dd>

一或多個 [HLSL 語句](dx-graphics-hlsl-statement-blocks.md)。

</dd> </dl>

## <a name="remarks"></a>備註

當編譯器使用分支方法來編譯 if 語句時，它會產生程式碼，根據指定的條件，只會評估 if 語句的一端。 例如，在 if 語句中：


```
[branch] if(x)
{
    x = sqrt(x);
}
```



**If** 語句具有隱含的 else 區塊，相當於 x = x。 因為我們已告知編譯器將分支方法與先前的分支屬性搭配使用，所以已編譯的程式碼將會評估 x，並只執行應該執行的端;如果 x 為零，則會執行 **else** 端，如果不是零，則會執行 **then** 端。

相反地，如果使用簡 **維屬性，則編譯的程式** 代碼將會評估 **if** 語句的兩邊，並使用 x 的原始值，在兩個結果值之間進行選擇。 以下是簡維屬性使用方式的範例：


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



在某些情況下，使用分支或壓平合併屬性可能會產生編譯錯誤。 如果 if 語句的任一邊包含漸層函式（例如 [**tex2D**](dx-graphics-hlsl-tex2d.md)），分支屬性可能會失敗。 如果 if 語句的任一邊包含 stream append 語句或任何其他具有副作用的語句，則簡維屬性可能會失敗。

**If** 語句也可以使用選擇性的 else 區塊。 如果 **if** 運算式為 true，則會處理與 if 語句相關聯之語句區塊中的程式碼。 否則，會處理與選用的 else 區塊相關聯的語句區塊。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[流程式控制制](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





