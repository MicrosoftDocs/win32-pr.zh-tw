---
title: UI_PKEY_FontProperties_BackgroundColorType
description: 識別 UI \_ PKEY \_ FontProperties \_ BackgroundColorType 屬性。
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443819"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ BackgroundColorType

識別 UI \_ PKEY \_ FontProperties \_ BackgroundColorType 屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>備註

UI \_ PKEY \_ FontProperties \_ BackgroundColorType 是由應用程式搭配 [ui \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)使用，以查詢 **文字反白顯示色彩** 圖庫的設定。

屬性值來自 [**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) 列舉。

預設值是 `UI_SWATCHCOLORTYPE_RGB`。

下表描述屬性值。



|   屬性                             |   描述                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | 應用程式應該針對色彩值查詢適當的系統計量，通常是以 GetSysColor (色彩視窗) 抓取的目前 Windows 主題 **視窗背景色彩** \_ 。                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | [**FontControl**](windowsribbon-element-fontcontrol.md)不支援。                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | 應用程式應該查詢 [UI \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) 的色彩值。 [UI \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)的色彩值會顯示在 [文字 **反白顯示色彩**] 按鈕上，並在 [**文字反白顯示色彩**] 圖庫中選取。<br/> |



 

\_當您 \_ \_ 在 [**FontControl**](windowsribbon-element-fontcontrol.md) **文字反白顯示色彩** 圖庫中選取色彩樣本時，UI PKEY FontProperties BackgroundColorType 會傳遞至 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)回呼方法。

> [!Note]  
> 強烈建議應用程式只設定初始 **文字反白顯示色彩** 值，而不會在資料指標在檔內重新置放時重新設定此值。 最後一個選取專案應維持不變，以避免需要重新選取所需的色彩。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

