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
ms.openlocfilehash: f86f7856e70a1be327297bb3fd4b892b3bf39789
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "103932769"
---
# <a name="show-urlacl"></a>show urlacl

列出指定之保留的 URL 或所有保留的 Url 的 Dacl。

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[url = \] * * * 字串*
</dt> <dd>

指定完整的 URL。 如果未指定，即表示所有 Url。

</dd> </dl>

## <a name="examples"></a>範例

**顯示 urlacl url =https://+:80/MyUrl**

**顯示 urlacl url =https://www.contoso.com:80/MyUrl**

 

 




