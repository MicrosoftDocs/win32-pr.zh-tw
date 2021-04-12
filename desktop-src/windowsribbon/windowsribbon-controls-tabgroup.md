---
title: Tab 群組
description: 索引標籤群組是在執行時間根據檔或工作區狀態隱藏或顯示的內容控制項。 此索引標籤群組包含一組內容相關的索引標籤控制項。
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316009"
---
# <a name="tab-group"></a>Tab 群組

索引標籤群組是在執行時間根據檔或工作區狀態隱藏或顯示的內容控制項。 此索引標籤群組包含一組內容相關的 [選項卡](windowsribbon-controls-tab.md) 控制項。

-   [詳細資料](#details)
-   [索引標籤群組屬性](#tab-group-properties)
-   [相關主題](#related-topics)

## <a name="details"></a>詳細資料

一般而言，在特定檔或工作區狀態期間，例如當使用者選取特定物件類型時，會顯示索引標籤群組。 例如，選取包含在資料表標頭中的影像時，可能需要顯示各種內容索引標籤，以同時公開資料表和影像功能。

> [!IMPORTANT]
> 索引標籤群組不支援 [應用程式模式](ribbon-applicationmodes.md)。 不過，您可以在索引標籤群組內 [的個別索引](windowsribbon-controls-tab.md) 標籤控制項。

 

下列螢幕擷取畫面顯示 Windows 7 繪圖 [的內容](windowsribbon-controls-tab.md) 索引標籤。

![顯示內容索引標籤控制項的螢幕擷取畫面。](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a>索引標籤群組屬性

功能區架構會為索引標籤群組控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

一般而言，功能區 UI 中的索引標籤群組屬性會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法，使與控制項相關聯的命令失效。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與 [索引標籤] 群組控制項相關聯的屬性索引鍵。



| 屬性索引鍵                                                                                     | 備註                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI \_ PKEY \_ CoNtextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md)     | 支援 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 和 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)。 |
| [UI \_ PKEY \_ 按鍵提示](windowsribbon-reference-properties-uipkey-keytip.md)                         | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)                           | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | 只能透過失效進行更新。                                                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**TabGroup 標記元素**](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 