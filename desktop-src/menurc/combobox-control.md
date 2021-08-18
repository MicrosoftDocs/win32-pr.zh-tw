---
title: 'COMBOBOX 控制項 (功能表和其他資源) '
description: 定義 (下拉式方塊的下拉式方塊控制項) 。
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- COMBOBOX 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2ffaa64266d9b370cca5215725eb45d0f620054c66562e3f60492441e38890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972117"
---
# <a name="combobox-control"></a>COMBOBOX 控制項

定義 (下拉式方塊的下拉式方塊控制項) 。 下拉式方塊是由靜態文字方塊或與清單方塊結合的編輯方塊所組成。 清單方塊可以隨時顯示，或由使用者向下提取。 如果下拉式方塊包含 [靜態] 文字方塊，文字方塊的清單方塊部分中的任何) ，文字方塊一律會顯示選取 (。 如果它使用編輯方塊，使用者可以輸入所需的選取專案;如果任何符合使用者在編輯方塊中輸入的) ，清單方塊會反白顯示第一個專案 (。 然後，使用者可以選取清單方塊中反白顯示的專案來完成選擇。 此外，下拉式方塊也可以是主控描繪，也可以是固定或可變高度。

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這個值可以是 COMBOBOX 類別樣式和下列任何樣式的組合： **WS \_ TABSTOP**、 **ws \_ GROUP**、 **ws \_ VSCROLL** 和 **ws \_ DISABLED**。

如果您未指定樣式，則預設樣式為 `CBS_SIMPLE | WS_TABSTOP` 。

</dd> </dl>

*Height* 參數適用于下拉式方塊的高度，且下拉式清單完全展開。

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

這個範例會定義具有垂直捲動條的下拉式方塊控制項：

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[下拉式方塊](../controls/about-combo-boxes.md)
</dt> </dl>

 

 