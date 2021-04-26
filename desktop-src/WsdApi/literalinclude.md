---
description: 將 C 或 IDL include 語句放在產生的程式碼中。
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: literalInclude 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995125"
---
# <a name="literalinclude-element"></a>literalInclude 元素

將 C 或 IDL include 語句放在產生的程式碼中。

## <a name="usage"></a>使用方式

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td><strong>語言</strong><br/></td>
<td>語言字串<br/></td>
<td>No<br/></td>
<td>要包含的頭檔案類型。 <br/> <br/>
<dt><strong>C</strong></dt> <dd> 包含 C 標頭檔。<br/> </dd> <dt><strong>Idl</strong></dt> <dd> 包含 IDL 檔案。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>本機</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>只有當 <strong>語言</strong> 設定為 C 時，才會使用這個屬性 &quot; &quot; 。<br/> <br/>
<dt><strong>真</strong></dt> <dd> 搜尋系統目錄之前，先在目前的目錄中搜尋指名的標頭。<br/> </dd> <dt><strong>假</strong></dt> <dd> 僅搜尋已命名標頭的系統目錄。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="remarks"></a>備註

下列範例顯示從不同的 **literalInclude** 元素產生的程式碼。

### <a name="example-1---generating-a-c-include-statement"></a>範例 1-產生 C include 語句

輸入 XML：

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

輸出碼：

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>範例 2-產生 C include 語句

輸入 XML：

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

輸出碼：

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>範例 3-產生 IDL 匯入語句

輸入 XML：

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

輸出碼：

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




