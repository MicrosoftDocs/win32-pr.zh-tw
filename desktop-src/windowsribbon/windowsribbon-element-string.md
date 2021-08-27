---
title: String 元素
description: 表示字串資源。
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Windows 功能區的字串元素
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a34a417b6ad4d57bea83fcae13d810b22114271
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630954"
---
# <a name="string-element"></a>String 元素

表示字串資源。

## <a name="usage"></a>使用方式

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>類型</th>
<th>必要</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>內容</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 由任何字元序列組成的字串，包括空白字元和分行符號字元。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>識別碼</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>否<br/></td>
<td>唯一的資源識別碼。 <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 介於2和59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。 <br/> 最大長度為10個字元，包括選擇性前置零。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>符號</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>字串的資源符號。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 字母或底線，後面接著任何一連串的字母、數位或底線。<br/> 長度上限為100個字元。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                                   | 描述                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**字串。內容**](windowsribbon-element-string-content.md)<br/> | 最多可能發生一次<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | 最多可能發生一次<br/> <br/> |
| [**字串. 符號**](windowsribbon-element-string-symbol.md)<br/>   | 最多可能發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**命令。快速鍵**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>備註

選擇性。

每個命令最多隻能出現一次 [**。 LabelTitle**](windowsribbon-element-command-labeltitle.md)、 [**LabelDescription**](windowsribbon-element-command-labeldescription.md)、 [**命令提示**](windowsribbon-element-command-keytip.md)、 [**命令 TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)或 [**TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) 元素。

字串定義會加入至功能區標頭檔中，例如 `#define strSave 59999` 。

如果未宣告任何宣告，則會將字串加入功能區資源檔中的字串資料表，其中的名稱和識別碼是由功能區架構產生的。

## <a name="examples"></a>範例

下列範例示範 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 專案的標記與 **字串** 宣告。


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a>項目資訊

- **最低支援系統**： Windows 7 
- **可以是空** 的：否



 

 





