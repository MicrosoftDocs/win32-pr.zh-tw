---
title: UI_PKEY_FontProperties_Strikethrough
description: 識別 UI \_ PKEY \_ FontProperties \_ 刪除線屬性。
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382537"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>UI \_ PKEY \_ FontProperties \_ 刪除線

識別 UI \_ PKEY \_ FontProperties \_ 刪除線屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>備註

\_ \_ \_ 應用程式會使用 UI PKEY FontProperties 刪除線來查詢 **刪除線** 按鈕的狀態。

屬性值來自 [**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) 列舉。

預設值是 `UI_FONTPROPERTIES_NOTSET`。

下列螢幕擷取畫面顯示功能區 [**FontControl**](windowsribbon-element-fontcontrol.md)的 **刪除線** 按鈕。

![fontcontrol 專案的螢幕擷取畫面，其中 richfont 屬性設定為 true。](images/markup/fontcontrol-strikethrough.png)

下表描述屬性和 UI 結果。



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **刪除線** 按鈕已停用，而且只能由應用程式設定。 |
| `UI_FONTPROPERTIES_NOTSET`       | 未選取 **刪除線** 按鈕。                                    |
| `UI_FONTPROPERTIES_SET`          | 已選取 **刪除線** 按鈕。                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 