---
title: 圖示資源
description: 定義點陣圖，以定義要用於指定應用程式或動畫圖標的圖示形狀。
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- 圖示資源功能表與其他資源
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507879"
---
# <a name="icon-resource"></a>圖示資源

定義點陣圖，以定義要用於指定應用程式或動畫圖標的圖示形狀。

``` syntax
nameID ICON filename
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別資源的唯一名稱或16位不帶正負號的整數值。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

包含資源的檔案名。 名稱必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。 路徑應該是加上引號的字串。

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="remarks"></a>備註

圖示和游標資源可以包含一個以上的影像。

## <a name="examples"></a>範例

下列範例會定義兩個圖示資源：

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用圖示](./using-icons.md)
</dt> </dl>

 

 