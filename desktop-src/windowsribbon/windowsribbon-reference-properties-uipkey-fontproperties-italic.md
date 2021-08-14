---
title: UI_PKEY_FontProperties_Italic
description: 識別 UI \_ PKEY \_ FontProperties \_ 斜體屬性。
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bb72e1ba43b29f5e3815fe42d0ace454ff0219a188a128b422e4a621af210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438533"
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



|    屬性                      |       UI 結果                                                       |
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

 

 