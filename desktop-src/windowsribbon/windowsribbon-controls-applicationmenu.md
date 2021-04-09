---
title: 應用程式功能表
description: '[應用程式] 功能表是執行 Windows 功能區架構之應用程式的主功能表。'
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842308"
---
# <a name="application-menu"></a>應用程式功能表

[應用程式] 功能表是執行 Windows 功能區架構之應用程式的主功能表。

-   [簡介](#introduction)
-   [應用程式功能表的元件](#components-of-the-application-menu)
    -   [應用程式功能表 MenuGroup](#application-menu-menugroup)
-   [調整應用程式功能表的大小](#sizing-the-application-menu)
-   [應用程式功能表屬性](#application-menu-properties)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

[應用程式] 功能表是由下拉式按鈕控制項所組成，它會顯示一個功能表，其中包含的命令會公開與完整專案相關的功能，例如整個檔、圖片或影片。 範例包括 [**新增**]、[**開啟**]、[**儲存**] 和 [結束 **] 命令。**

下列螢幕擷取畫面顯示應用程式功能表。

![windows 7 功能區的 [應用程式] 功能表和 [最近使用的專案] 清單的螢幕擷取畫面。](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a>應用程式功能表的元件

應用程式功能表是任何功能區應用程式中的必要元素。 [應用程式 []](windowsribbon-controls-tab.md) 功能表中的進入點是一種特殊按鈕，會顯示為索引標籤資料列中的第一個專案，如下列螢幕擷取畫面所示。

> [!Note]  
> Windows 8 和更新版本：應用程式功能表按鈕影像已變更為 label： **File**。 建議您不要使用 [檔案] 作為任何您自己的索引標籤的標籤。

 

![適用于 windows 7 之 wordpad 的 [應用程式] 功能表按鈕的螢幕擷取畫面。](images/overviews/applicationmenu-button.png)

按一下時，此按鈕會顯示在下列螢幕擷取畫面中顯示的豐富功能表 (從 WordPad for Windows 7) 的應用程式功能表。

![適用于 windows 7 之 wordpad 的 [應用程式] 功能表功能表的螢幕擷取畫面。](images/overviews/applicationmenu-menu.png)

> [!Note]  
> 按一下 [應用程式] 功能表按鈕時，不會影響索引標籤設定;相反地，焦點會進入功能表。

 

[應用程式] 功能表包含兩個窗格：一或多個 [**MenuGroup**](windowsribbon-element-menugroup.md)專案所代表的命令清單，以及由 [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)元素表示的 [最新專案](windowsribbon-controls-recentitems.md)清單。

### <a name="application-menu-menugroup"></a>應用程式功能表 MenuGroup

[**ApplicationMenu**](windowsribbon-element-applicationmenu.md)元素必須包含至少一個 [**MenuGroup**](windowsribbon-element-menugroup.md)子項目，以公開應用層級命令的清單。 如果宣告多個 **MenuGroup** 元素，則會在群組之間繪製分隔線，如下列螢幕擷取畫面所示。

![應用程式功能表 menugroup 的螢幕擷取畫面。](images/overviews/applicationmenu-menugroup.png)

以下是應用程式功能表中 [**MenuGroup**](windowsribbon-element-menugroup.md) 元素的條件約束清單：

-   所有的 [**MenuGroup**](windowsribbon-element-menugroup.md) 專案都必須使用的 *類別* 屬性值進行宣告 `MajorItems` 。
-   應用程式功能表  [**MenuGroup**](windowsribbon-element-menugroup.md) 僅支援 [按鈕](windowsribbon-controls-button.md)、 [切換按鈕](windowsribbon-controls-togglebutton.md)、 [下拉式按鈕](windowsribbon-controls-dropdownbutton.md)、 [分割按鈕](windowsribbon-controls-splitbutton.md)、 [下拉式清單庫](windowsribbon-controls-dropdowngallery.md)和 [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md) 控制項。
    > \[!重要\]  
    > 命令資源庫是應用程式功能表中唯一支援的資源庫類型。 如需資源庫控制項的詳細資訊，請參閱使用資源 [庫](./ribbon-controls-galleries.md)。

     

在 [**MenuGroup**](windowsribbon-element-menugroup.md)中使用 [按鈕](windowsribbon-controls-button.md)或 [切換按鈕](windowsribbon-controls-togglebutton.md)時， [**LabelTitle**](windowsribbon-element-command-labeltitle.md)的值會顯示在功能表中，而 [**TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)和 [**TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)命令的值會顯示為工具提示，如下列螢幕擷取畫面所示。

![應用程式功能表中按鈕控制項的螢幕擷取畫面。](images/overviews/applicationmenu-menubutton.png)

在 [應用程式] 功能表中使用 [下拉式](windowsribbon-controls-dropdownbutton.md)按鈕、 [分割按鈕](windowsribbon-controls-splitbutton.md)、 [下拉式清單庫](windowsribbon-controls-dropdowngallery.md)或 [分割按鈕庫](windowsribbon-controls-splitbuttongallery.md) 時，功能表部分會顯示為包含和隱藏 [ **最近使用的專案** ] 窗格的飛出視窗。

針對 [分割按鈕](windowsribbon-controls-splitbutton.md) 和 [下拉式按鈕](windowsribbon-controls-dropdownbutton.md) 控制項， [**LabelDescription**](windowsribbon-element-command-labeldescription.md) 的值會以內嵌方式顯示在飛出視窗功能表中，以視覺化方式協助使用者探索命令功能。 **LabelDescription** 的顯示值會以程式設計方式在兩行範圍內中斷，並嘗試將值完全放在下方的 [**最近的專案**] 窗格中。 如果 **LabelDescription** 值不符合，就會展開飛出視窗以容納最長的 [**命令。**](windowsribbon-element-command-comment.md) [**MenuGroup**](windowsribbon-element-menugroup.md)中的批註值。

下列螢幕擷取畫面說明 [分割按鈕](windowsribbon-controls-splitbutton.md) 飛出視窗中的這些行為。

![應用程式功能表中清單控制項飛出視窗的螢幕擷取畫面。](images/overviews/applicationmenu-menuflyout.png)

使用 [下拉式程式庫](windowsribbon-controls-dropdowngallery.md) 和 [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md)時，只會顯示標籤和影像。

## <a name="sizing-the-application-menu"></a>調整應用程式功能表的大小

功能區架構會處理應用程式功能表的大小。 如果為 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 或 [**LabelDescription**](windowsribbon-element-command-labeldescription.md)的值提供非常長的字串，或使用一長串的命令，則功能表會調整其大小以容納內容。 某些形式的調整包括擴充 flyouts 或功能表窗格的大小，以及在需要滾動時加入平移檢視器。

## <a name="application-menu-properties"></a>應用程式功能表屬性

功能區架構會針對應用程式功能表控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

一般而言，應用程式功能表屬性會在功能區 UI 中更新，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。 會處理「失效」事件，而屬性更新則由 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 回呼方法定義。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式不會針對更新的屬性值進行查詢，直到架構需要該屬性為止。 例如，當啟用索引標籤，且在功能區 UI 中顯示控制項，或顯示工具提示時，架構會要求屬性。



| 屬性索引鍵                                                                                     | 備註                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | 只能透過失效進行更新。 |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | 只能透過失效進行更新。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**ApplicationMenu 標記元素**](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 