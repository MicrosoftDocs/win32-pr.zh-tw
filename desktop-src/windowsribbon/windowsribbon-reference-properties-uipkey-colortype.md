---
title: UI_PKEY_ColorType
description: 識別 UI \_ PKEY \_ ColorType 屬性。
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443889"
---
# <a name="ui_pkey_colortype"></a>UI \_ PKEY \_ ColorType

識別 UI \_ PKEY \_ ColorType 屬性。

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 UI PKEY ColorType 來查詢 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)控制項的色彩設定。

屬性值來自 [**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) 列舉。



|    屬性                            |    描述                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UI \_ SWATCHCOLORTYPE \_ NOCOLOR   | 應用程式應該將色彩設定視為透明。 通常與 [ **無色彩** 色彩] 設定搭配使用。                                                   |
| UI \_ SWATCHCOLORTYPE \_ 自動 | 應用程式應該查詢 [GetSysColor (COLOR \_ WINDOWTEXT) ](/windows/win32/api/winuser/nf-winuser-getsyscolor)。 通常與 **自動** 色彩設定一起使用。 |
| UI \_ SWATCHCOLORTYPE \_ RGB       | 應用程式應該查詢色彩設定的 [UI \_ PKEY \_ 色彩](windowsribbon-reference-properties-uipkey-color.md) 。                                                          |



 

\_ \_ 在 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)中選取色彩樣本時，UI PKEY ColorType 會傳遞至 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)回呼方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[色彩選擇器屬性](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 