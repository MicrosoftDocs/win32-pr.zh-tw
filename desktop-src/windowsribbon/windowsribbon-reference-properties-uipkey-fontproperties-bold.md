---
title: UI_PKEY_FontProperties_Bold
description: 識別 UI \_ PKEY \_ FontProperties \_ Bold 屬性。
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444379"
---
# <a name="ui_pkey_fontproperties_bold"></a>UI \_ PKEY \_ FontProperties \_ Bold

識別 UI \_ PKEY \_ FontProperties \_ Bold 屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>備註

UI \_ PKEY \_ FontProperties \_ bold 是由應用程式用來查詢 **粗體** 按鈕的狀態。

屬性值來自 [**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) 列舉。

預設值是 `UI_FONTPROPERTIES_NOTSET`。

下表描述屬性和 UI 結果。



|      屬性                    |    UI 結果                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **粗體** 按鈕已停用，而且只能由應用程式設定。 |
| `UI_FONTPROPERTIES_NOTSET`       | 未選取 [**粗體**] 按鈕。                                    |
| `UI_FONTPROPERTIES_SET`          | 已選取 [**粗體**] 按鈕。                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 