---
title: 'Tab (Windows 功能區架構) '
description: 索引標籤包含相關控制項的群組。
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317076"
---
# <a name="tab-windows-ribbon-framework"></a>Tab (Windows 功能區架構) 

索引標籤包含相關控制項的 [群組](windowsribbon-controls-group.md) 。

-   [詳細資料](#details)
-   [索引標籤屬性](#tab-properties)
-   [相關主題](#related-topics)

## <a name="details"></a>詳細資料

功能區架構中有三種類型的索引標籤。



| 類型               | Description                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **核心索引標籤**       | 用來組織應用程式預設功能的核心索引標籤。                                                                                                                                                                                                                   |
| **內容索引標籤** | 在特定檔或工作區狀態期間顯示的索引標籤。 例如，如果使用者選取特定物件類型（例如資料表標頭中包含的影像），則可能會顯示各種內容索引標籤，以同時公開資料表和影像功能。 |
| **模式索引標籤**      | 在特定檔或工作區 [應用程式模式](ribbon-applicationmodes.md)期間顯示的核心索引標籤，例如 [預覽列印]。                                                                                                                                        |



 

下列螢幕擷取畫面顯示 Windows 7 繪圖的核心索引標籤。

![顯示核心索引標籤控制項的螢幕擷取畫面。](images/controls/coretab.png)

## <a name="tab-properties"></a>索引標籤屬性

功能區架構會定義索引標籤控制項的 [屬性索引鍵](windowsribbon-reference-properties.md) 集合。

通常會在功能區 UI 中更新索引標籤屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與索引標籤控制項相關聯的屬性索引鍵。



| 屬性索引鍵                                                                                     | 備註                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)                           | 只能透過失效進行更新。 |
| [UI \_ PKEY \_ 按鍵提示](windowsribbon-reference-properties-uipkey-keytip.md)                         | 只能透過失效進行更新。 |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | 只能透過失效進行更新。 |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | 只能透過失效進行更新。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**Tab 標記元素**](windowsribbon-element-tab.md)
</dt> </dl>

 

 
