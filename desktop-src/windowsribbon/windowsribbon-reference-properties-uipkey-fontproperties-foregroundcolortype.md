---
title: UI_PKEY_FontProperties_ForegroundColorType
description: 識別 UI \_ PKEY \_ FontProperties \_ ForegroundColorType 屬性。
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26b324a4e504c5ef98850f2bbcabd55b34525650b0ecfd3c201d45896e0c800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438647"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ ForegroundColorType

識別 UI \_ PKEY \_ FontProperties \_ ForegroundColorType 屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>備註

UI \_ PKEY \_ FontProperties \_ ForegroundColorType 是由應用程式搭配 [ui \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md)用來查詢 **文字顏色** 庫設定。

屬性值來自 [**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) 列舉。

預設值是 `UI_SWATCHCOLORTYPE_RGB`。

下表描述屬性值。



|     值                           |     描述                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | [**FontControl**](windowsribbon-element-fontcontrol.md)不支援。                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | 應用程式應該針對色彩值查詢適當的系統計量，通常是使用 GetSysColor (color WINDOWTEXT) 抓取的目前 Windows 主題 **文字色彩** \_ 。                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | 應用程式應該查詢 [UI \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) 的色彩值。 [ [UI \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) ] 的色彩值會顯示在 **[文字色彩] 按鈕中** ，並在 [ **文字色彩** ] 圖庫中選取。<br/> |



 

\_ \_ \_ 當在 [**FontControl**](windowsribbon-element-fontcontrol.md) **文字色彩** 圖庫中選取色彩樣本時，UI PKEY FontProperties ForegroundColorType 會傳遞至 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)回呼方法。

> [!Note]  
> 強烈建議應用程式只設定初始 **文字色彩** 值，而且不會在資料指標在檔內重新置放時重新設定此值。 最後一個選取專案應維持不變，以避免需要重新選取所需的色彩。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

