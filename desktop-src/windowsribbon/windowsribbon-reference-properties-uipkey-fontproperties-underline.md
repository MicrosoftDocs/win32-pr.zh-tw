---
title: UI_PKEY_FontProperties_Underline
description: 識別 UI \_ PKEY \_ FontProperties 底線 \_ 屬性。
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75142e08549c2084ebcd37e82943ed63fdfb5b278faef01c4ad79441fa36915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706716"
---
# <a name="ui_pkey_fontproperties_underline"></a>UI \_ PKEY \_ FontProperties \_ 波浪線

識別 UI \_ PKEY \_ FontProperties 底線 \_ 屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>備註

\_ \_ \_ 應用程式會使用 UI PKEY FontProperties 底線來查詢底線按鈕的狀態。 

屬性值來自 [**UI \_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) 列舉。

預設值是 `UI_FONTUNDERLINE_NOTSET`。

下列螢幕擷取畫面顯示功能區 [**FontControl**](windowsribbon-element-fontcontrol.md)**的底線按鈕。**

![fontcontrol 專案的螢幕擷取畫面，其中 richfont 屬性設定為 true。](images/markup/fontcontrol-underline.png)

下表描述屬性和 UI 結果。



|      屬性                   |       UI 結果                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | 底線 **按鈕已** 停用，而且只能由應用程式設定。 |
| `UI_FONTUNDERLINE_NOTSET`       | 未選取 [底線 **] 按鈕。**                                    |
| `UI_FONTUNDERLINE_SET`          | 已選取 [底線 **] 按鈕。**                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 