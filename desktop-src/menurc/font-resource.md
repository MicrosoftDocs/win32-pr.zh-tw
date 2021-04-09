---
title: 字型資源
description: 定義包含字型的檔案。
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- 字型資源功能表與其他資源
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678692"
---
# <a name="font-resource"></a>字型資源

定義包含字型的檔案。

``` syntax
nameID FONT filename
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別資源的唯一16位不帶正負號的整數值。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

包含資源的檔案名。 名稱必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。 路徑應該是加上引號的字串。

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="examples"></a>範例

下列範例會定義單一字型資源：

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




