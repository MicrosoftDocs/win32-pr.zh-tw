---
title: 說明按鈕
description: '[說明] 按鈕是一種控制項，可讓使用者按一下以顯示應用程式說明系統。'
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933257"
---
# <a name="help-button"></a>說明按鈕

[說明] 按鈕是一種控制項，可讓使用者按一下以顯示應用程式說明系統。

-   [詳細資料](#details)
-   [說明按鈕屬性](#help-button-properties)
-   [相關主題](#related-topics)

## <a name="details"></a>詳細資料

下列螢幕擷取畫面說明功能區的 [說明] 按鈕。

![顯示 [說明] 按鈕的螢幕擷取畫面。](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>說明按鈕屬性

功能區架構會針對 [說明] 按鈕控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

一般來說，功能區 UI 中的 [說明] 按鈕屬性會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法，使與控制項相關聯的命令失效。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與 [說明] 按鈕控制項相關聯的屬性索引鍵。



| 屬性索引鍵                                                                                     | 備註                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UI \_ PKEY \_ 按鍵提示](windowsribbon-reference-properties-uipkey-keytip.md)                         | 只能透過失效進行更新。 |
| [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)                           | 只能透過失效進行更新。 |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | 只能透過失效進行更新。 |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | 只能透過失效進行更新。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**HelpButton 元素**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 