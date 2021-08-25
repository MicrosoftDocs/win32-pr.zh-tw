---
title: show urlacl
description: 列出指定之保留的 URL 或所有保留的 Url 的 Dacl。
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- 顯示 urlacl HTTP
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f6e2443f4cdb489f8deb6e8b61d3a808e8a0711ce13c8d71edc57001787617
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900618"
---
# <a name="show-urlacl"></a>show urlacl

列出指定之保留的 URL 或所有保留的 Url 的 Dacl。

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[ url = \]**_字串_
</dt> <dd>

指定完整的 URL。 如果未指定，即表示所有 Url。

</dd> </dl>

## <a name="examples"></a>範例

**顯示 urlacl url =https://+:80/MyUrl**

**顯示 urlacl url =https://www.contoso.com:80/MyUrl**

 

 




