---
title: CURSOR 資源
description: 定義在顯示畫面或動畫游標上定義游標形狀的點陣圖。
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- 資料指標資源功能表與其他資源
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966033"
---
# <a name="cursor-resource"></a>CURSOR 資源

定義在顯示畫面或動畫游標上定義游標形狀的點陣圖。

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別資源的唯一名稱或16位不帶正負號的整數。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

包含資源的檔案名。 名稱必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。 路徑應該是加上引號的字串。

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="remarks"></a>備註

圖示和游標資源可以包含一個以上的影像。

## <a name="examples"></a>範例

下列範例會定義兩個數據指標資源：依名稱 (cursor1) ，另一個則依據 number (2) ：

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用資料指標](./using-cursors.md)
</dt> </dl>

 

 