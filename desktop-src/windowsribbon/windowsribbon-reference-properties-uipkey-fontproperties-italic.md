---
title: UI_PKEY_FontProperties_Italic
description: 識別 UI \_ PKEY \_ FontProperties \_ 斜體屬性。
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375597"
---
# <a name="ui_pkey_fontproperties_italic"></a>UI \_ PKEY \_ FontProperties \_ 斜體

識別 UI \_ PKEY \_ FontProperties \_ 斜體屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>備註

UI \_ PKEY \_ FontProperties \_ 斜體是由應用程式用來查詢 **斜體** 按鈕的狀態。

屬性值來自 [**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) 列舉。

預設值是 `UI_FONTPROPERTIES_NOTSET`。

下表描述屬性和 UI 結果。



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **斜體** 按鈕已停用，而且只能由應用程式設定。 |
| `UI_FONTPROPERTIES_NOTSET`       | 未選取 [**斜體**] 按鈕。                                    |
| `UI_FONTPROPERTIES_SET`          | 已選取 [**斜體**] 按鈕。                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 