---
title: 最近的項目
description: '[最近使用的專案] 清單是應用程式功能表中的一個窗格，會顯示應用程式最近使用的 (MRU) 專案。'
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1d67c38e1eb9014cfd3349881ed2849755ebc89489cc925052aa690f54adc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810874"
---
# <a name="recent-items"></a>最近的項目

[最近使用的專案] 清單是 [應用程式功能表](windowsribbon-controls-applicationmenu.md) 中的一個窗格，會顯示應用程式最近使用的 (MRU) 專案。

-   [詳細資料](#details)
-   [最近使用的專案屬性](#recent-items-properties)
-   [備註](#remarks)
-   [相關主題](#related-topics)

## <a name="details"></a>詳細資料

下列螢幕擷取畫面說明 [WordPad] 的 [最近的專案] 清單，Windows 7) 。

![microsoft 油漆功能區中 [最近使用的專案] 清單的螢幕擷取畫面。](images/controls/recentitems.png)

[應用程式功能表](windowsribbon-controls-applicationmenu.md)最多隻能有一個 [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)清單（以 **ApplicationMenu. RecentItems** 元素表示），以顯示最近使用過的檔、圖片、電影和其他使用者正在處理的專案。 所列專案的數目範圍從零到標記中指定的最大數目，預設值為10。 最近的專案會顯示為字串的編號清單，表示檔案名。 建議使用 [**LabelDescription**](windowsribbon-element-command-labeldescription.md) 屬性來提供檔案位置的完整路徑，如下列螢幕擷取畫面所示。

![[應用程式] 功能表中 [最近使用的專案] 清單的螢幕擷取畫面。](images/overviews/applicationmenu-menurecentitems.png)

[**RecentItems**](windowsribbon-element-recentitems.md)元素具有 *EnablePinning* 屬性，如果設定為 `true` ，會在清單中的每個專案右邊顯示釘選圖示，如下列螢幕擷取畫面所示。

> [!Note]  
> 如果未指定 *EnablePinning* 屬性，預設會啟用釘選。

 

![最近專案釘選在應用程式功能表中的螢幕擷取畫面。](images/overviews/applicationmenu-menurecentitemspinned.png)

釘選演算法的目的是要防止專案從 [ **最近的專案** ] 清單中下降。 此演算法會產生下列行為：

-   在 [ **最近使用的專案** ] 清單的頂端，一律會加入新專案。
-   專案會在一段時間內于清單中下移。 一旦清單填滿 (達到 [標記) 中指定的最大專案數，當新專案新增至清單頂端時，較舊的專案就會落在清單底部。
-   如果專案已出現在清單中的某處，但再次存取，則會移回清單的最上方。
-   如果專案已釘選，它仍會往下移動清單，但不會落在底部。 相反地，當清單填滿之後，當新專案新增至清單時，釘選的專案上方第一個取消釘選的專案會下降。
-   如果已釘選的專案數目達到專案數上限，則在取消固定專案之前，不會將任何新專案新增至清單。

## <a name="recent-items-properties"></a>最近使用的專案屬性

功能區架構會為最近的 Items 控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

一般來說，功能區 UI 中的 [最近的專案] 屬性會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效，藉此更新。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與 [最近的專案] 控制項相關聯的屬性索引鍵。



| 屬性索引鍵                                                                       | 備註                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [UI \_ PKEY \_ 按鍵提示](windowsribbon-reference-properties-uipkey-keytip.md)           | 只能透過失效進行更新。 |
| [UI \_ PKEY \_ RecentItems](windowsribbon-reference-properties-uipkey-recentitems.md) | 只能透過失效進行更新。 |



 

## <a name="remarks"></a>備註

[IApplicationDocumentLists：： GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)方法可以用來取得功能區應用程式的 Windows Shell MRU 清單。 然後，應用程式可以使用這個方法所抓取的物件來建立功能區架構所需的資料，以填入 [應用程式功能表](windowsribbon-controls-applicationmenu.md)的 [**最近的專案**] 清單。

> [!Note]  
> 使用這個方法時， *listtype* 應該具有值 `ADLT_RECENT` 。

 

如需如何在功能區架構應用程式中執行 MRU 專案清單的範例，請參閱 [HTMLEditRibbon 範例](windowsribbon-htmleditribbonsample.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**最近使用的專案標記元素**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 