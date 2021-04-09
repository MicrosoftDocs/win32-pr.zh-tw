---
title: HTML 資源
description: 定義 HTML 檔案。
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- HTML 資源功能表與其他資源
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841379"
---
# <a name="html-resource"></a>HTML 資源

定義 HTML 檔案。

``` syntax
nameID HTML filename
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別資源的唯一名稱或16位不帶正負號的整數值。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

HTML 檔案的名稱。 如果檔案不在目前的工作目錄中，則它必須是完整或相對路徑。 路徑應該是加上引號的字串。

</dd> </dl>

## <a name="examples"></a>範例

下列範例會定義 HTML 資源：

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




