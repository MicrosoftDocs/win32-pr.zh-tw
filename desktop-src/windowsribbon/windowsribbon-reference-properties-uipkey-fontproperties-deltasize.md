---
title: UI_PKEY_FontProperties_DeltaSize
description: 識別 UI \_ PKEY \_ FontProperties \_ DeltaSize 屬性。
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023492"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>UI \_ PKEY \_ FontProperties \_ DeltaSize

識別 UI \_ PKEY \_ FontProperties \_ DeltaSize 屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>備註

\_ \_ \_ 如果應用程式無法指定 **字型大小** 值（例如選取了 [執行 heterogeneously 大小的文字]），應用程式就會使用 UI PKEY FontProperties DeltaSize。 **字型大小** 控制項設為空白，而 UI \_ PKEY \_ FontProperties \_ DeltaSize 用來捕捉使用者與 **字型成長** 和 **字型壓縮** 按鈕的互動。

Ui \_ PKEY \_ FontProperties \_ DeltaSize 包含在 [ui \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md)中。

下列螢幕擷取畫面顯示功能區 [**FontControl**](windowsribbon-element-fontcontrol.md)的 **字型成長** 和 **字型壓縮** 按鈕。

![fontcontrol 上字型成長和字型壓縮按鈕的螢幕擷取畫面。](images/markup/fontcontrol-incdec.png)

下表描述屬性值。



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | 已按下 [**放大] 字型** 按鈕。   |
| `UI_FONTDELTASIZE_SHRINK` | 按一下 [**縮小字型**] 按鈕。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTDELTASIZE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 