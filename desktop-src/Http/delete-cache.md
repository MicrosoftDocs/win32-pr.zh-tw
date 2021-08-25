---
title: delete cache
description: 清除整個 URL 快取，或根據指定的 URL 刪除專案。
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- 刪除快取 HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c41f2147f0101f312a7fa76796032ec8c821fcea9c08cf89bb3174ddace43d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870558"
---
# <a name="delete-cache"></a>delete cache

清除整個 URL 快取，或根據指定的 URL 刪除專案。

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[ url = \]**_字串_
</dt> <dd>

必要。 指定完整的 URL。

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive = \] {yes \| 否}**
</dt> <dd>

如果是，則會移除指定之 URL 下的所有專案。

</dd> </dl>

## <a name="examples"></a>範例

**刪除快取 url = https://www.contoso.com:80/myresource/ 遞迴 = 是**

 

 




