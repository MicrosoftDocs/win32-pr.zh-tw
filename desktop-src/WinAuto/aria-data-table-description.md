---
title: ARIA 資料表格警告
description: ARIA 資料表格警告
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021970"
---
# <a name="aria-data-table-warning"></a>ARIA 資料表格警告

## <a name="text"></a>Text

資料表包含資料，但沒有摘要或有效的 **aria describedby** 屬性。

## <a name="type"></a>類型

警告

## <a name="description"></a>描述

這項警告適用于具有多個資料格的 HTML 資料表。 它不會套用至資料表， `role="presentation"` 因為這些會被視為版面配置資料表。

此警告表示資料表已識別為數據表，但未定義可存取的描述。

> [!Note]  
> 並非所有的資料表都需要有可存取的描述。 如果使用者需要詳細資訊來瞭解資料表結構和內容，您應該定義可存取的描述。

 

若要解決這個警告，請使用 summary 屬性或 **aria describedby** 屬性定義資料表的可存取描述。

## <a name="example"></a>範例


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




