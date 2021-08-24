---
title: '分組控制項 (功能表和其他資源) '
description: 定義群組框控制項。 控制項是將其他控制項群組在一起的矩形。 控制項的分組方式是在其周圍繪製框線，並在左上角顯示指定的文字。
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- 分組控制功能表和其他資源
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05fb8e795cfe483d16406f07fffd2a26df14cebc3c38a07fbef7f2cb78cc245a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602078"
---
# <a name="groupbox-control"></a>分組控制項

定義群組框控制項。 控制項是將其他控制項群組在一起的矩形。 控制項的分組方式是在其周圍繪製框線，並在左上角顯示指定的文字。

您只能在 [**DIALOGEX**](dialogex-resource.md)語句中使用的 **分組** 符號語句，會定義控制項視窗的文字、識別碼、維度和屬性。

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這個值可以是 button 類別樣式 **BS \_ 分組** 程式和 **ws \_ TABSTOP** 和 **ws \_ DISABLED** 樣式的組合。

如果您未指定樣式，則預設樣式為 **BS \_ 分組**。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="remarks"></a>備註

當樣式包含 **WS \_ TABSTOP** 或文字指定快速鍵時，請將焦點移至群組內的第一個控制項，或按下快速鍵。

## <a name="examples"></a>範例

這個範例會定義一個標示為 [選項] 的群組方塊控制項：

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[群組方塊](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




