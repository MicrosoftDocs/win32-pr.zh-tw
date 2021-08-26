---
title: 引數元素
description: 引數元素包含條件字串的其中一個部分。
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- 引數元素 Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f5a689b74bd18138361d9377358ddee5cf5979f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630189"
---
# <a name="argument-element"></a>引數元素

**引數** 元素包含條件字串的其中一個部分。 條件字串通常有條件部分和值部分。 例如，在條件字串「演出者等於 Joe」中，條件部分是「等於」，而值部分是「Joe」。

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>屬性

需要 (**名稱**) 

條件字串之一部分的名稱。

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                         |
|-----------|----------------------------------|
| 父代    | [片段](fragment-element.md) |
| 子系     | 無                             |



 

## <a name="remarks"></a>備註

當 **片段** 專案的 **name** 屬性是媒體專案特性（如專輯演出者或內容類型）時，**片段** 專案必須包含兩個 **引數** 元素：一個指定條件，另一個指定值。 下表顯示 **name** 屬性的兩個可能值，以及如何使用 **引數** 元素來指定條件和值。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>條件</td>
<td><strong>引數</strong>元素的內容是條件字串的條件部分。 例如，在條件字串 &quot; 演出者等於 Joe &quot; ，條件部分 &quot; 等於 &quot; 。 條件字串的條件部分必須是下列其中一項： Equals、不等於、Contains、不包含、小於、大於、是、不是、早于、大於、小於、大於、小於、小於或等於、小於、不超過、小於、等於、小於、小於。</td>
</tr>
<tr class="even">
<td>值</td>
<td><strong>引數</strong>元素的內容是條件字串的值部分。 例如，在條件字串 &quot; 演出者等於 joe &quot; ，值部分為 &quot; joe &quot; 。例子：<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

當 **片段** 專案的 **name** 屬性為 "limit total Size To" 或 "limit total Duration to" 時，**片段** 元素必須包含兩個 **引數** 元素：一個指定格式，另一個則指定數位。 下表顯示 [ **名稱** ] 屬性的兩個可能值，以及如何使用 **引數** 元素來限制播放清單的大小或持續時間。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>格式</td>
<td>當<strong>片段</strong>專案的 [<strong>名稱</strong>] 屬性是 [ &quot; 限制大小總計] 時 &quot; ，<strong>引數</strong>元素的內容必須是下列其中一項： kb、mb 或 gb。當<strong>片段</strong>專案的<strong>name</strong>屬性是 [ &quot; 限制的總持續時間] 時 &quot; ，<strong>引數</strong>元素的內容必須是下列其中一項：秒、分鐘、小時或天。<br/></td>
</tr>
<tr class="even">
<td>數字</td>
<td><strong>引數</strong>元素的內容是一個數位，可限制播放清單的大小或持續時間。例子：<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

當 **片段** 元素的 **name** 屬性為 "Limit items of items" 時，**片段** 元素必須包含一個指定專案數目的 **引數** 元素。 下表說明如何使用 **name** 屬性的數值。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>數字</td>
<td><strong>引數</strong>元素的內容是一個數位，可限制播放清單中的專案數。例子：<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**片段元素**](fragment-element.md)
</dt> <dt>

[**WindowsMedia 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





