---
title: UI_PKEY_FontProperties_VerticalPositioning
description: 識別 UI \_ PKEY \_ FontProperties \_ VerticalPositioning 屬性。
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2461aff2aab819304ffd3db0240f18786422f575f7a2d45bb737c0863ad378a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031576"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>UI \_ PKEY \_ FontProperties \_ VerticalPositioning

識別 UI \_ PKEY \_ FontProperties \_ VerticalPositioning 屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a>備註

UI \_ PKEY \_ FontProperties \_ VerticalPositioning 是由應用程式用來查詢 **上標** 和 **下標** 控制項的值。

屬性值來自 [**UI \_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) 列舉。

預設值是 `UI_FONTVERTICALPOSITION_NOTSET`。

下列螢幕擷取畫面顯示功能區 [**FontControl**](windowsribbon-element-fontcontrol.md)的 **上標** 和 **下標** 按鈕。

![fontcontrol 專案的螢幕擷取畫面，其中 richfont 屬性設定為 true。](images/markup/fontcontrol-subsuper.png)

下表描述屬性和 UI 結果。



|     屬性                           |          UI 結果                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | **上標** 和 **下標** 按鈕已停用，而且只能由應用程式設定。 |
| `UI_FONTVERTICALPOSITION_NOTSET`       | 未選取 **上標** 和 **下標** 按鈕。                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | 選取 [**上標**] 按鈕。                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | 已選取 [注 **標**] 按鈕。                                                              |



 

> [!Note]  
> 無法同時選取 **上標** 和 **下標** 按鈕。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 