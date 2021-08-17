---
title: '按鈕 (Windows 功能區架構) '
description: 按鈕是使用者可以按一下來提供應用程式輸入的控制項。
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82a1a71181b3478e065922b5a1836f6cd0f47bf9b3f2e497f45564118449b95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707789"
---
# <a name="button-windows-ribbon-framework"></a>按鈕 (Windows 功能區架構) 

按鈕是使用者可以按一下來提供應用程式輸入的控制項。

-   [簡介](#introduction)
-   [按鈕屬性](#button-properties)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

下列螢幕擷取畫面包含功能區按鈕元素的三個範例。

![microsoft wordpad 功能區中按鈕控制項的螢幕擷取畫面。](images/controls/button.png)

## <a name="button-properties"></a>按鈕屬性

功能區架構會為按鈕控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

通常會在功能區 UI 中更新按鈕屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與按鈕控制項相關聯的屬性索引鍵。



| 屬性索引鍵                                                                                             | 備註                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI \_ PKEY \_ 已啟用](windowsribbon-reference-properties-uipkey-enabled.md)                               | 支援 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 和 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)。 |
| [UI \_ PKEY \_ 按鍵提示](windowsribbon-reference-properties-uipkey-keytip.md)                                 | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)                                   | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)             | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)                         | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)                         | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | 只能透過失效進行更新。                                                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**按鈕標記元素**](windowsribbon-element-button.md)
</dt> </dl>

 

 
