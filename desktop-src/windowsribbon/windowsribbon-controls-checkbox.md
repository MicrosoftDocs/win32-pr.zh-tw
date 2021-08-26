---
title: 核取方塊
description: 核取方塊是使用者可按一下以提供應用程式輸入的控制項。 控制項提供以視覺化方式呈現的切換狀態。
ms.assetid: fe07aa5c-1818-41e2-b48d-5fefe50d733f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b68e850d86bd9b15a354cfa41789406e328a57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478884"
---
# <a name="check-box"></a>核取方塊

核取方塊是使用者可按一下以提供應用程式輸入的控制項。 控制項提供以視覺化方式呈現的切換狀態。

-   [詳細資料](#details)
-   [核取方塊屬性](#check-box-properties)
-   [相關主題](#related-topics)

## <a name="details"></a>詳細資料

此核取方塊不支援第三個或不定的狀態。

下列螢幕擷取畫面說明功能區核取方塊元素。

![microsoft 油漆功能區中核取方塊控制項的螢幕擷取畫面。](images/controls/checkbox.png)

## <a name="check-box-properties"></a>核取方塊屬性

功能區架構會為核取方塊控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

通常會在功能區 UI 中更新核取方塊屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與核取方塊控制項相關聯的屬性索引鍵。




| 屬性索引鍵 | 備註 | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a> | 支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。<blockquote>[!Note]<br />如果與控制項相關聯的命令透過呼叫 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework：： InvalidateUICommand</strong></a>而失效，則架構 <code>UI_INVALIDATIONS_VALUE</code> 會在傳遞做為 <em>旗標</em>的值時查詢此屬性。</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | 支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。 | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | 只能透過失效進行更新。 | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**CheckBox 標記元素**](windowsribbon-element-checkbox.md)
</dt> </dl>

