---
title: 關於 List-View 控制項
description: 清單視圖控制項是顯示專案集合的視窗。
ms.assetid: 163f7778-690c-4166-b0c5-c7be1a03ae98
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 592684378b4264319d790b1e2e05eb9e0ae37f28
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424328"
---
# <a name="about-list-view-controls"></a>關於 List-View 控制項

請參閱 [虛擬 listview 控制項範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)。

清單視圖控制項是顯示專案集合的視窗。 清單視圖控制項提供數種方式來排列和顯示專案，而且比簡單 [清單方塊](list-boxes.md)更有彈性。 例如，每個專案的其他相關資訊可以顯示在圖示和標籤右邊的資料行中。

-   [清單-視圖樣式和視圖](#list-view-styles-and-views)
    -   [擴充的 List-View 樣式](#extended-list-view-styles)
-   [虛擬 List-View 樣式](#virtual-list-view-style)
    -   [建立虛擬 List-View 控制項](#creating-a-virtual-list-view-control)
    -   [相容性問題](#compatibility-issues)
    -   [處理虛擬 List-View 控制通知碼](#handling-virtual-list-view-control-notification-codes)
    -   [快取管理](#cache-management)
-   [清單-查看工作區](#list-view-working-areas)
-   [清單視圖影像清單](#list-view-image-lists)
-   [清單視圖專案和子專案](#list-view-items-and-subitems)
    -   [清單視圖專案狀態](#list-view-item-states)
    -   [回呼專案和回呼遮罩](#callback-items-and-the-callback-mask)
    -   [清單視圖專案位置](#list-view-item-position)
    -   [排列、排序和尋找專案](#arranging-sorting-and-finding-items)
-   [清單-視圖資料行](#list-view-columns)
-   [清單視圖捲軸位置](#list-view-scroll-position)
-   [清單-查看標籤編輯](#list-view-label-editing)
-   [清單視圖色彩](#list-view-colors)
-   [依群組排列清單專案](#arranging-list-items-by-group)
-   [插入標記](#insertion-marks)

## <a name="list-view-styles-and-views"></a>List-View 樣式和視圖

清單視圖控制項可以在五個不同的視圖中顯示專案。 控制項的視窗樣式會指定預設視圖。 額外的視窗樣式會指定專案與控制項特定功能的對齊方式。 下表描述這些視圖。



| 檢視名稱             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 圖示視圖             | 由 [**lvs) \_ 圖示**](list-view-window-styles.md)視窗樣式或透過 [**LVM \_ SETVIEW**](lvm-setview.md)訊息傳遞 **LV \_ 視圖 \_ 圖示** 來指定。 每個項目顯示成下方附有標籤的全螢幕圖示。 使用者可以將專案拖曳到清單視圖視窗中的任何位置。                                                                                                                                                                                                                                         |
| 小圖示視圖       | 由 [**lvs) \_ SMALLICON**](list-view-window-styles.md)視窗樣式或藉由使用 [**LVM \_ SETVIEW**](lvm-setview.md)傳遞 **LV \_ VIEW \_ SMALLICON** 所指定。 每個專案都會顯示為具有其右邊標籤的小圖示。 使用者可以將專案拖曳到任何位置。                                                                                                                                                                                                                                                       |
| 清單檢視             | 由 [**lvs) \_ 清單**](list-view-window-styles.md)視窗樣式或藉由使用 [**LVM \_ SETVIEW**](lvm-setview.md)傳遞 **LV \_ 視圖 \_ 清單** 來指定。 每個專案都會顯示為一個小圖示，並在其右邊加上標籤。 專案會排列在資料行中，且使用者無法將其拖曳至任意位置。                                                                                                                                                                                                                               |
| 報表 (詳細資料) 視圖 | 由 [**lvs) \_ 報表**](list-view-window-styles.md)視窗樣式指定，或透過 [**LVM \_ SETVIEW**](lvm-setview.md)傳遞 **LV \_ 視圖 \_ 詳細資料**。 每個專案都會出現在自己的行上，並將資訊排列在資料行中。 最左邊的資料行一律會靠左對齊，並包含小圖示和標籤。 後續的資料行包含應用程式所指定的子工作。 除非您同時指定 [**lvs) \_ NOCOLUMNHEADER**](list-view-window-styles.md) 視窗樣式，否則每個資料行都有一個標頭。 |
| 並排顯示檢視             | **第6版和更新版本。** 藉由使用 [**LVM \_ SETVIEW**](lvm-setview.md)傳遞 **LV \_ VIEW \_ 磚** 來指定。 每個專案都會顯示為完整大小的圖示，其標籤旁邊有一或多行。                                                                                                                                                                                                                                                                                                                                                        |



 

下列螢幕擷取畫面使用 views 來顯示有關七個寵物的不同資訊量。 這些視圖會示範資訊可能會出現在 Windows Vista 上的方式。 控制項的視覺化樣式已使用 [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme)設定為 "Explorer" 主題。

下列螢幕擷取畫面顯示詳細資料檢視。

![顯示五個數據行和七個數據列資訊的螢幕擷取畫面](images/lv-detailsview.png)

下列螢幕擷取畫面顯示圖示視圖。

![只顯示每個寵物名稱的螢幕擷取畫面，以及表示物種的圖示](images/lv-iconview.png)

下列螢幕擷取畫面顯示清單視圖。

![顯示每個寵物的螢幕擷取畫面，接下來是寵物名稱、知名和價格文字的大型圖示](images/lv-listview.png)

下列螢幕擷取畫面顯示圖格視圖。

![並排顯示。](images/lv-tileview.png)

您可以在建立清單視圖控制項之後變更檢視類型。 若要取出並變更視窗樣式，請使用 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 和 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函式。 若要判斷目前視圖的視窗樣式，請使用 [**lvs) \_ TYPEMASK**](list-view-window-styles.md) 值。

您可以藉由指定 [**lvs) \_ ALIGNTOP**](list-view-window-styles.md) (預設) 或 [**lvs) \_ ALIGNLEFT**](list-view-window-styles.md) 視窗樣式，來控制專案在圖示或小型圖示視圖中的相片順序。

您可以在建立清單視圖控制項之後變更對齊。 若要判斷目前的對齊，請使用 [**lvs) \_ ALIGNMASK**](list-view-window-styles.md) 值。

其他視窗樣式提供其他選項，例如使用者是否可以編輯標籤，或一次選取一個以上的專案。 如需完整清單，請參閱 [清單視圖視窗樣式](list-view-window-styles.md)。

### <a name="extended-list-view-styles"></a>擴充的 List-View 樣式

擴充清單視圖控制項樣式提供選項，例如核取方塊、平面捲軸、格線和熱追蹤。 如需完整清單，請參閱 [擴充的 List-View 樣式](extended-list-view-styles.md)。 您無法使用與標準視窗樣式相同的方式來存取擴充清單視圖樣式。 您不會使用 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 和 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數來進行擴充樣式變更。

有兩個訊息可設定和取出擴充樣式資訊， [**lvm \_ SETEXTENDEDLISTVIEWSTYLE**](lvm-setextendedlistviewstyle.md) 和 [**lvm \_ GETEXTENDEDLISTVIEWSTYLE**](lvm-getextendedlistviewstyle.md)。 您可以使用下列對應的宏，而不是明確地傳送訊息： [**listview \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle)、 [**listview \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)和 [**listview \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle)。

## <a name="virtual-list-view-style"></a>虛擬 List-View 樣式

虛擬清單視圖是具有 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式的清單視圖控制項。 這種樣式可讓控制項處理數百萬個專案，因為擁有者會收到管理專案資料的負擔。 這可讓您搭配使用虛擬清單-view 控制項與大型資料庫的資訊，其中已有特定的資料存取方法。

虛擬清單控制項會維持極少的專案資訊本身。 除了專案選取和焦點資訊之外，控制項的擁有者必須管理所有專案資訊。 其他進程會使用 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 通知碼來要求擁有者的專案資訊。

因為這種類型的清單控制項適用于大型資料集，建議您快取要求的專案資料，以改善抓取效能。 清單視圖會提供快取提示機制，以協助優化快取。 提示會以 [LVN \_ ODCACHEHINT](lvn-odcachehint.md) 通知碼的形式來執行。

### <a name="creating-a-virtual-list-view-control"></a>建立虛擬 List-View 控制項

您可以使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立虛擬清單-View 控制項，將 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 視窗樣式指定為 *dwStyle* 函數參數的一部分。 不支援在 **lvs) \_ OWNERDATA** 樣式之間動態切換。

您可以使用 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式搭配大部分的視窗樣式，但 [**lvs) \_ SORTASCENDING**](list-view-window-styles.md) 或 [**lvs) \_ SORTDESCENDING**](list-view-window-styles.md) 樣式除外。 所有虛擬清單-view 控制項預設為 [**lvs) \_ AUTOARRANGE**](list-view-window-styles.md) 樣式。

若要讓專案顯示在清單中，您必須先明確地或使用 [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex)宏傳送 [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md)訊息。

下列訊息在 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) style 下不受支援： [**lvm \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md)、 [**lvm \_ GETITEMTEXT**](lvm-getitemtext.md)、 [**lvm \_ SETTILEINFO**](lvm-settileinfo.md)和 [**lvm \_ MAPIDTOINDEX**](lvm-mapidtoindex.md)。

### <a name="compatibility-issues"></a>相容性問題

所有四個清單視圖樣式（圖示、小圖示、清單和報表檢視）都支援 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式。 具有 **lvs) \_ OWNERDATA** 樣式的清單視圖控制項不會儲存任何專案特定資訊。 因此，您可以套用至專案的唯一有效專案狀態旗標，會 [**LVIS \_ 選取**](list-view-item-states.md) 並 [**LVIS \_ 焦點**](list-view-item-states.md)。 不會儲存任何其他狀態資訊。 尤其是，清單視圖控制項不會維護每個專案的狀態或重迭影像。 不過，您可以讓清單視圖控制項透過將 [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) 訊息傳送給應用程式，以查詢這些映射。

大部分的清單視圖控制訊息和相關宏都受到完整支援。 但是，當您使用 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式時，有些訊息有一些限制或不受支援。 下表摘要列出受影響的訊息。



| 訊息                                             | 限制                                                                                                                                                                                                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LVM \_ 排列**](lvm-arrange.md)                 | 不支援 **LVA \_ 網格** 線樣式。                                                                                                                                                                                                                 |
| [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md)   | 將專案計數設定為零，並清除所有內部選取變數，但不會實際刪除任何專案。 它會發出通知回撥。                                                                                                           |
| [**LVM \_ DELETEITEM**](lvm-deleteitem.md)           | 僅支援選取完整性，並不會實際刪除專案。                                                                                                                                                                                 |
| [**LVM \_ GETITEMSTATE**](lvm-getitemstate.md)       | 只傳回焦點和選取狀態 (亦即，清單視圖控制項所儲存的狀態) 。                                                                                                                                                                |
| [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md)         | 不支援 **LVNI \_ 剪** 下、 **LVNI \_ HIDDEN** 或 **LVNI \_ DROPHILITED** 的清單視圖搜尋準則。 支援所有其他準則。                                                                                                                     |
| [**LVM \_ GETWORKAREAS**](lvm-getworkareas.md)       | 不支援。                                                                                                                                                                                                                                               |
| [**LVM \_ INSERTITEM**](lvm-insertitem.md)           | 僅支援選取完整性。                                                                                                                                                                                                                      |
| [**LVM \_ SETITEM**](lvm-setitem.md)                 | 不支援。 若要設定專案狀態，請使用 [**ListView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) 訊息。                                                                                                                                               |
| [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md)       | 設定目前在清單中的專案數。 如果清單視圖控制項傳送的通知要求任何專案的資料達最大值集，則必須準備好提供該資料給擁有者。 訊息參數支援虛擬清單-view 控制項。 |
| [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) | 不支援。                                                                                                                                                                                                                                               |
| [**LVM \_ SETITEMSTATE**](lvm-setitemstate.md)       | 只允許變更專案的選取範圍和焦點狀態。                                                                                                                                                                                          |
| [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md)         | 不支援。 應用程式必須負責維護專案文字。                                                                                                                                                                            |
| [**LVM \_ SETWORKAREAS**](lvm-setworkareas.md)       | 不支援。                                                                                                                                                                                                                                               |
| [**LVM \_ SORTITEMS**](lvm-sortitems.md)             | 不支援。 應用程式必須負責以所需的順序呈現專案。                                                                                                                                                             |



 

### <a name="handling-virtual-list-view-control-notification-codes"></a>處理虛擬 List-View 控制通知碼

具有 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式的清單視圖控制項，會傳送與其他清單視圖控制項相同的通知碼，以及兩個額外的控制項： [LVN \_ ODCACHEHINT](lvn-odcachehint.md) 和 [LVN \_ ODFINDITEM](lvn-odfinditem.md)。 以下是 **lvs) \_ OWNERDATA** 樣式所傳送的清單視圖控制項最常見的通知。



|      通知                    |     描述                         |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LVN \_ GETDISPINFO](lvn-getdispinfo.md) | 虛擬清單控制項只會維護很少的專案資訊。 因此，它通常會傳送 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 通知碼來要求專案資訊。 此訊息的處理方式與標準清單控制項中的回呼專案非常類似。 由於控制項支援的專案數目可能很大，因此快取專案資料可改善效能。 處理 LVN \_ GETDISPINFO 時，控制項的擁有者會先嘗試從快取提供要求的專案資訊 (如需詳細資訊，請參閱快取 [管理](#cache-management)) 。 如果未快取要求的專案，擁有者必須做好準備，才能以其他方式提供資訊。 |
| [LVN \_ ODCACHEHINT](lvn-odcachehint.md) | 虛擬清單視圖會傳送 [LVN \_ ODCACHEHINT](lvn-odcachehint.md) 通知碼，以協助優化快取。 通知碼會針對建議快取的專案範圍提供內含的索引值。 收到通知碼時，擁有者必須做好準備，以針對要求的範圍載入具有專案資訊的快取，如此一來，當傳送 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 訊息時，即可立即取得資訊。                                                                                                                                                                                                                                   |
| [LVN \_ ODFINDITEM](lvn-odfinditem.md)   | 當控制項需要擁有者來尋找特定的回呼專案時，虛擬清單-view 控制項就會傳送 [LVN \_ ODFINDITEM](lvn-odfinditem.md) 通知碼。 當清單視圖控制項收到快速存取金鑰或收到 [**LVM \_ FINDITEM**](lvm-finditem.md) 訊息時，就會傳送通知碼。 搜尋資訊會以 [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) 結構的形式傳送，這是 [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) 結構的成員。 擁有者必須做好準備，才能搜尋符合清單視圖控制項所提供之資訊的專案。 如果成功，擁有者會傳回專案的索引; 如果找不到相符專案，則會傳回-1。               |



 

### <a name="cache-management"></a>快取管理

具有 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式的清單視圖控制項會產生大量的 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 通知碼，以及協助優化快取（ [LVN \_ ODCACHEHINT](lvn-odcachehint.md) 訊息）。 LVN \_ ODCACHEHINT 訊息提供要包含在快取中之建議專案的相關資訊。 這些訊息會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送， *LParam* 值會作為 [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) 結構的位址。

[**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint)結構包含兩個整數成員（ **iFrom** 和 **分成**），代表最可能需要之專案範圍的內含端點。 擁有者必須做好準備，以針對建議範圍內的每個專案，載入具有專案資訊的快取。

清單控制項通常需要第一個專案的專案資訊 (offset 0) 。 [LVN \_ ODCACHEHINT](lvn-odcachehint.md)通知碼可能不一定會包含專案0，但必須一律包含在快取中。

通常會存取清單中的最後一個專案。 因此，擁有者可能會想要保留第二個快取，其中包含清單結尾的專案。 從 [LVN \_ ODCACHEHINT](lvn-odcachehint.md) 所要求的範圍可以針對結尾快取進行檢查，讓它自動可用，而不是每次重載相同的結束範圍。

## <a name="list-view-working-areas"></a>List-View 工作區

清單視圖控制項支援工作區域，這些區域是清單視圖控制項用來排列其專案的矩形虛擬區域。 工作區域不是視窗，且不能有可見的框線。 依預設，清單視圖控制項沒有任何工作區域。 藉由建立工作區，您可以在專案的左邊、頂端或右邊建立空白框線，或在正常情況下，顯示水準捲軸。

建立工作區時，位於工作區域內的專案會成為工作區域的成員。 同樣地，如果將某個專案移到工作區，該專案就會變成該工作區的成員。 如果專案不在任何工作區域內，它會自動成為第一個 (索引 0) 工作區域的成員。 若要將新專案放在特定工作區中，您必須先建立專案，然後使用 [**lvm \_ SETITEMPOSITION**](lvm-setitemposition.md) 或 [**lvm \_ SETITEMPOSITION32**](lvm-setitemposition32.md) 訊息將它移至所需的工作區域。

下圖是清單視圖控制項的範例，其中包含四個工作區，每個區域都在不同的工作區象限中。

![清單視圖控制項的螢幕擷取畫面，其中有一個工作區域位於工作區的每個象限中](images/working.jpg)

多個工作區可以用來在單一視圖內建立不同的區域。 您可以在具有不同意義的單一視圖中建立區域。 例如，檔案系統的視圖可能會有讀取/寫入檔案的區域，以及唯讀檔案的另一個區域。 使用者可以將專案放在不同的工作區中，藉以分類專案。 如果檔案已移至唯讀區域，則會自動變成隻讀區域。

多個工作區可以交集，但位於交集內的任何專案都會變成具有較低索引之區域的成員。因此，最好避免這種情況。 排序多個工作區時，專案會與相同工作區域中的其他專案進行排序。

您可以使用 [**LVM \_ GETNUMBEROFWORKAREAS**](lvm-getnumberofworkareas.md) 訊息抓取工作區域數目。 工作區域會隨 [**lvm \_ SETWORKAREAS**](lvm-setworkareas.md) 訊息變更，而且可以使用 [**lvm \_ GETWORKAREAS**](lvm-getworkareas.md) 訊息來抓取。 這兩個訊息都採用 [**rect**](/previous-versions//dd162897(v=vs.85)) 結構陣列的位址做為 *LParam* ，而 **rect** 結構的數目則為 *wParam*。 這些結構的 **左邊** 和 **頂端** 成員會指定工作區域的原點)  (左上角的座標， **右邊** 和 **底部** 的成員則指定工作區域的右下角。 所有座標都是在清單視圖的用戶端座標中。 允許的工作區域數目上限是由 **LV \_ MAX \_ WORKAREAS** 值定義。

變更工作區域不會影響具有 [**lvs) \_ 清單**](list-view-window-styles.md) 或 [**lvs) \_ 報表**](list-view-window-styles.md) 視圖的清單視圖控制項，但在變更檢視類型時，將會維護工作區域。 您可以使用 [**lvs) \_ 圖示**](list-view-window-styles.md) 和 [**lvs) \_ SMALLICON**](list-view-window-styles.md) views，修改工作區以變更專案的顯示方式。 讓工作區域的寬度 (靠右左邊) 大於控制項的用戶端寬度，會導致專案以該寬度和水準捲軸來顯示。 使工作區域的寬度比控制項的工作區寬度窄，會導致專案在工作區域內換行，而不是工作區的寬度。 將 **left** 或 **top** 成員設為正值，會導致專案從工作區域開始顯示，在控制項邊緣與專案之間建立空白空間。 您也可以在控制項的右邊緣和專案之間建立空白空間，讓工作區域的寬度小於控制項的用戶端寬度。

## <a name="list-view-image-lists"></a>List-View 影像清單

依預設，清單視圖控制項不會顯示專案影像。 若要顯示專案影像，您必須建立影像清單，並將它們與控制項建立關聯。 清單視圖控制項可以有三個影像清單：

-   影像清單，其中包含當控制項在圖示視圖中時，所顯示的完整大小圖示。
-   影像清單，其中包含當控制項處於小型圖示視圖、清單視圖或報表檢視時所顯示的小圖示。
-   包含狀態影像的影像清單，會顯示在完整大小或小圖示的左邊。 您可以使用狀態影像（例如核取和清除的核取方塊）來表示應用程式定義的專案狀態。 狀態影像會顯示在圖示視圖、小型圖示視圖、清單視圖和報表檢視中。

完整大小和小型圖示影像清單也可以包含重迭 *影像*，其設計目的是要在專案圖示上以透明方式繪製。

若要在清單視圖控制項中使用覆迭影像：

1.  呼叫 [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) 函式，將重迭影像索引指派給完整大小和小型圖示影像清單中的影像。 覆迭影像是由以一為基礎的索引來識別。
2.  當您呼叫 [**listview \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) 或 [**listview \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) 宏時，可以將重迭影像索引與專案產生關聯。 使用 [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask)宏，在專案的 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **state** 成員中指定覆迭影像索引。 您也必須在 **stateMask** 成員中設定 [**LVIS \_ OVERLAYMASK**](list-view-item-states.md)位。

如果指定狀態影像清單，清單視圖控制項會在狀態影像的每個專案圖示左邊保留空間。

若要將狀態影像與專案產生關聯，請使用 [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask)宏在 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **state** 成員中指定狀態影像索引。 索引會識別控制項狀態影像清單中的影像。 雖然影像清單索引是以零為基底，但控制項會使用以一為基礎的索引來識別狀態影像。 狀態影像索引為零表示專案沒有狀態影像。

根據預設，當清單視圖控制項被終結時，它會終結指派給它的影像清單。 但是，如果清單視圖控制項有 [ [**lvs) \_ SHAREIMAGELISTS**](list-view-window-styles.md) ] 視窗樣式，則應用程式會負責在不再使用時終結影像清單。 如果您將相同的影像清單指派給多個清單視圖控制項，則應該指定此樣式;否則，有一個以上的控制項可能會嘗試終結相同的影像清單。

## <a name="list-view-items-and-subitems"></a>List-View 專案與子專案

清單視圖控制項中的每個專案都有圖示、標籤、目前的狀態，以及應用程式定義的值。 藉由使用清單視圖訊息，您可以加入、修改和刪除專案，以及取得專案的相關資訊。

每個專案都可以有一個或多個子 *專案。* 子專案是在報表檢視中，顯示在與專案的圖示和標籤分開的資料行中的字串。 若要指定子工作的文字，請使用 [**lvm \_ SETITEMTEXT**](lvm-setitemtext.md) 或 [**lvm \_ SETITEM**](lvm-setitem.md) 訊息。 清單視圖控制項中的所有專案都有相同的子專案數目。 子的數目取決於清單視圖控制項中的資料行數目。 當您將資料行加入至清單視圖控制項時，您會指定其相關聯的子索引。

[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構會定義清單視圖專案或子專案。 **IItem** 成員是專案的以零為基底的索引。 如果結構包含專案的相關資訊， **iSubItem** 成員是子專案的以一為起始的索引，或為零。 其他成員會指定項目的文字、圖示、狀態和項目資料。 *專案資料* 是與清單視圖專案相關聯的應用程式定義值。

若要將專案加入至清單視圖控制項，請使用 [**LVM \_ INSERTITEM**](lvm-insertitem.md) 訊息，並指定 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構的位址。 新增多個專案之前，您可以將 [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md) 訊息傳送給控制項，並指定控制項最終將包含的專案數目。 此訊息可讓清單視圖控制項只重新配置其內部資料結構一次，而不是每次新增專案。 您可以使用 [**LVM \_ GETITEMCOUNT**](lvm-getitemcount.md) 訊息來判斷清單視圖控制項中的專案數。 如果您要將大量專案加入至清單視圖控制項，可以在新增專案之前停用重繪來加速程式，然後在新增專案之後啟用重新繪製。 使用 [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw) 訊息來啟用和停用重繪。

若要變更清單視圖專案的屬性，請使用 [**LVM \_ SETITEM**](lvm-setitem.md) 訊息，並指定 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構的位址。 此結構的 **遮罩** 成員會指定您想要變更的專案屬性。 例如，若只要變更專案或子專案的文字，請使用 [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md) 訊息。

若要取出清單視圖專案的相關資訊，請使用 [**LVM \_ GETITEM**](lvm-getitem.md) 訊息，並指定要填入之 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構的位址。 此結構的 **遮罩** 成員會指定要取出的專案屬性。 若只要取出專案或子專案的文字，請使用 [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) 訊息。

若要刪除清單視圖專案，請使用 [**LVM \_ DELETEITEM**](lvm-deleteitem.md) 訊息。 您可以使用 [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) 訊息來刪除清單視圖控制項中的所有專案。

### <a name="list-view-item-states"></a>List-View 專案狀態

專案的狀態是一個值，可指定專案的可用性、指出使用者動作，或是反映專案的狀態。 清單視圖控制項會變更某些狀態位，例如使用者選取專案時。 應用程式可能會變更其他狀態位，以停用或隱藏專案，或指定重迭影像或狀態影像。 如需覆迭影像和狀態影像的詳細資訊，請參閱 [清單-視圖影像清單](#list-view-image-lists)。

專案的狀態是由 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **state** 成員所指定。 當您指定或變更專案的狀態時， **stateMask** 成員會指定您需要變更的狀態位。 您可以使用 [**LVM \_ SETITEMSTATE**](lvm-setitemstate.md) 訊息來變更專案的狀態。 您可以在建立專案時指定專案的狀態，或使用 [**LVM \_ SETITEM**](lvm-setitem.md) 訊息來變更其屬性。 若要判斷專案的目前狀態，請使用 [**lvm \_ GETITEMSTATE**](lvm-getitemstate.md) 或 [**lvm \_ GETITEM**](lvm-getitem.md) 訊息。

若要設定專案的重迭影像， [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **stateMask** 成員必須包含 [**LVIS \_ OVERLAYMASK**](list-view-item-states.md)值，而且 **狀態** 成員必須包含覆迭影像的以一為基礎的索引，而這個覆迭影像會使用 [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask)宏來向左移動8個位。 索引可以是零，以指定無重迭影像。

若要設定專案的狀態影像， [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **stateMask** 成員必須包含 [**LVIS \_ STATEIMAGEMASK**](list-view-item-states.md)值，而且 **狀態** 成員必須包含使用 [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask)宏將左移12個位的狀態影像之以一為起始的索引。 索引可以是零，以指定無狀態影像。

### <a name="callback-items-and-the-callback-mask"></a>回呼項目和回呼遮罩

針對每個專案，清單視圖控制項通常會儲存標籤文字、專案圖示的影像清單索引，以及專案狀態的一組位旗標。 您可以定義回呼專案或變更控制項的回呼遮罩，以指出應用程式（而不是控制項）儲存部分或全部資訊。 如果您的應用程式儲存其中一些資訊，您可能會想要使用回呼。

清單視圖控制項中的 *回呼專案* 是應用程式儲存文字或圖示索引的專案，或兩者。 您可以在傳送 [**LVM \_ INSERTITEM**](lvm-insertitem.md) 訊息時定義回呼專案，以將專案新增至清單視圖控制項。 如果應用程式儲存專案或子專案的文字，請將專案 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **pszText** 成員設定為 **LPSTR \_ TEXTCALLBACK**。 如果應用程式儲存專案的圖示索引，請將專案 **LVITEM** 結構的 **iImage** 成員設定為 **I \_ IMAGECALLBACK**。

清單視圖控制項的 *回呼遮罩* 是一組位旗標，用來指定應用程式（而非控制項）儲存目前資料的專案狀態。 回呼遮罩適用於所有控制項的項目，與套用至特定項目的回呼項目指定不同。 回呼遮罩預設為零，表示清單視圖控制項會儲存所有專案狀態資訊。 建立清單視圖控制項並初始化其專案之後，您可以傳送 [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) 訊息來變更回呼遮罩。 若要取得目前的回呼遮罩，請傳送 [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) 訊息。

當清單視圖控制項必須顯示或排序應用程式儲存回呼資訊的清單視圖專案時，控制項會將 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 通知程式碼傳送至控制項的父視窗。 這則訊息會指定 [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) 結構，其中包含所需的資訊類型，並識別要取出的專案或子專案。 父視窗必須處理 LVN \_ GETDISPINFO，以提供所要求的資料。

如果清單視圖控制項偵測到專案的回呼資訊中有變更，例如文字、圖示或狀態資訊的變更，控制項會傳送 [LVN \_ SETDISPINFO](lvn-setdispinfo.md) 通知碼來通知您變更。

如果您變更回呼專案的屬性或狀態位，則會使用 [**LVM \_ 更新**](lvm-update.md) 訊息來強制控制項重新繪製專案。 此訊息也會讓控制項在有 [**lvs) \_ AUTOARRANGE**](list-view-window-styles.md) 樣式時排列其專案。 您可以使用 [**LVM \_ REDRAWITEMS**](lvm-redrawitems.md) 訊息來使清單-view 控制項工作區的對應部分失效，以重繪某範圍的專案。

藉由有效使用回呼專案和回呼遮罩，您可以確保每個專案屬性只能在一個位置進行維護。 這麼做可以簡化您的應用程式，但唯一儲存的空間是儲存專案標籤和子專案文字所需的記憶體。

### <a name="list-view-item-position"></a>List-View 專案位置

每個清單視圖專案都有一個位置和大小，您可以使用訊息來取得和設定。 您也可以判斷哪一個專案在指定的位置（如果有的話）。 清單視圖專案的位置會指定在 *view 座標* 中，這是由捲軸位置位移的用戶端座標。

若要取出並設定專案的位置，請使用 [**lvm \_ GETITEMPOSITION**](lvm-getitemposition.md) 和 [**lvm \_ SETITEMPOSITION**](lvm-setitemposition.md) 訊息。 **LVM \_GETITEMPOSITION** 適用于所有視圖，但 **LVM \_ SETITEMPOSITION** 只適用于圖示和小型圖示視圖。

您可以使用 [**LVM \_ system.windows.media.visualtreehelper.hittest**](lvm-hittest.md) 訊息來判斷哪個專案（如果有的話）是在特定位置。

若要抓取清單專案的周框，或僅針對其圖示或標籤取得周框，請使用 [**LVM \_ GETITEMRECT**](lvm-getitemrect.md) 訊息。

### <a name="arranging-sorting-and-finding-items"></a>排列、排序和尋找專案

您可以使用清單視圖訊息來排列和排序專案，以及根據專案的屬性或位置來尋找專案。 排列重新置放專案以對齊格線，但專案的索引不會變更。 排序會變更 (的專案順序及其對應的索引) ，然後據此重新置放。 您只能在圖示和小型圖示視圖中排列專案，但是您可以在任何視圖中排序專案。 若要尋找專案，請傳送可指定專案位置或屬性的清單視圖訊息。

若要排列專案，請使用 [**LVM \_ 排列**](lvm-arrange.md) 訊息。 您可以藉由指定 [ [**lvs) \_ AUTOARRANGE**](list-view-window-styles.md) ] 視窗樣式，確保每次都能排列專案。

若要排序專案，請使用 [**LVM \_ SORTITEMS**](lvm-sortitems.md) 訊息。 當您使用這個訊息進行排序時，您會指定一個應用程式定義的回呼函式，以供清單視圖控制項呼叫來比較任何兩個專案的相對順序。 控制項會將與這兩個專案相關聯的專案資料傳遞給比較函數。 專案資料是將專案插入清單中時，在專案的 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **lParam** 成員中指定的值。 藉由指定適當的專案資料並提供適當的比較函式，您可以依標籤、任何子專案或任何其他屬性來排序專案。 請注意，排序專案不會重新排列對應的子專案。 重新排序專案時，會將專案與其對應的子專案一起攜帶;也就是說，整個資料列會保持在一起。 若要個別排序資料行，請從其專案卸離子專案，您必須在使用 [**LVM \_ SETITEM**](lvm-setitem.md)排序之後重新產生資料行。

您可以藉由指定 [ [**lvs) \_ SORTASCENDING**](list-view-window-styles.md) ] 或 [ [**lvs) \_ SORTDESCENDING**](list-view-window-styles.md) ] 視窗樣式，確保一律會排序清單視圖控制項。 具有這些樣式的控制項會使用專案的標籤文字，以遞增或遞減順序排序。 使用這些視窗樣式時，不能提供比較函數。 如果清單視圖控制項有其中一種樣式，則如果您嘗試插入具有 **LPSTR \_ TEXTCALLBACK** 的專案做為其 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **pszText** 成員， [**LVM \_ INSERTITEM**](lvm-insertitem.md)訊息將會失敗。

您可以使用 [**LVM \_ FINDITEM**](lvm-finditem.md) 訊息，尋找具有特定屬性的清單視圖專案。 您可以使用 [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) 訊息，找到處于指定狀態且與指定專案具有指定之關聯性的清單視圖專案。 例如，您可以取出指定專案右邊的下一個選取專案。

## <a name="list-view-columns"></a>List-View 資料行

資料行控制專案和其子專案在報表檢視中的顯示方式。 每個資料行都有標題和寬度，並與特定子專案相關聯;子項零是專案的圖示和標籤。 資料行的屬性是由 [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) 結構所定義。

若要將資料行新增至清單視圖控制項，請使用 [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) 訊息。 若要刪除資料行，請使用 [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) 訊息。

> [!Note]  
> 只有 ComCtl32.dll 6 版和更新版本才支援刪除清單視圖控制項中的資料行零。 第5版也支援刪除資料行零，但只有在您使用 [**CCM \_ SETVERSION**](ccm-setversion.md) 將版本設定為5或更新版本之後。 第5版之前的版本不支援刪除資料行0。

 

您可以使用 [**lvm \_ GETCOLUMN**](lvm-getcolumn.md) 和 [**lvm \_ SETCOLUMN**](lvm-setcolumn.md) 訊息來取得和變更現有資料行的屬性。 若要取出或變更資料行的寬度，請使用 [**lvm \_ GETCOLUMNWIDTH**](lvm-getcolumnwidth.md) 和 [**lvm \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) 訊息。

除非指定了 [**lvs) \_ NOCOLUMNHEADER**](list-view-window-styles.md) 視窗樣式，否則資料行標頭會出現在報表檢視中。 使用者可以按一下資料行標頭，使 [**LVN \_ COLUMNCLICK**](lvn-columnclick.md) 通知碼傳送至父視窗。 一般情況下，父視窗會在按一下時，依指定的資料行排序清單視圖控制項。 使用者也可以拖曳標頭之間的資料行輔助線來調整資料行的大小。

清單視圖控制項可以顯示資料行標題旁的影像。 若要執行這項功能，請指定 **LVCF \_ 影像** 值，並將影像的索引指派給 [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)結構中的 **iImage** 成員。

清單視圖控制項可以設定顯示資料行的順序。 若要執行這項功能，請指定 **LVCF \_ 順序** 值，並將資料行順序指派給 [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)結構中的 **iOrder** 成員。 資料行順序是以零為基底，而且是由左至右的順序。 例如，零表示最左邊的資料行。

## <a name="list-view-scroll-position"></a>List-View 捲軸位置

除非指定了 [ [**lvs) \_ NOSCROLL**](list-view-window-styles.md) ] 視窗樣式，否則清單視圖控制項可滾動顯示超過控制項工作區所能容納的專案。 您可以抓取清單視圖控制項的滾動位置和相關資訊、依指定的數量來滾動清單視圖控制項，或滾動清單視圖控制項，以顯示指定的清單專案。

在圖示視圖或小型圖示視圖中，目前的捲軸位置是由 *視圖來源* 所定義。 視圖來源是相對於清單視圖控制項可見區域的座標集合，對應于視圖座標 (0，0) 。 若要取得目前的視圖來源，請使用 [**LVM \_ GETORIGIN**](lvm-getorigin.md) 訊息。 此訊息只能用在圖示或小型圖示視圖中;它會在清單或報表檢視中傳回錯誤。

在清單或報表檢視中，目前的捲軸位置是由 *top 索引* 所定義。 頂端索引是清單視圖控制項中第一個可見專案的索引。 若要取得目前的頂端索引，請使用 [**LVM \_ GETTOPINDEX**](lvm-gettopindex.md) 訊息。 此訊息只會傳回清單或報表檢視中的有效結果;它會在圖示或小型圖示視圖中傳回零。

您可以使用 [**LVM \_ GETVIEWRECT**](lvm-getviewrect.md) 訊息來取得清單視圖控制項中所有專案的周框（相對於控制項的可見區域）。

[**LVM \_ GETCOUNTPERPAGE**](lvm-getcountperpage.md)訊息會傳回符合清單視圖控制項一頁的專案數。 此訊息只會傳回清單和報表檢視中的有效結果;在圖示和小型圖示視圖中，它會傳回專案的總數。

若要依特定數量滾動清單視圖控制項，請使用 [**LVM \_ 滾動**](lvm-scroll.md) 條訊息。 使用 [**LVM \_ ENSUREVISIBLE**](lvm-ensurevisible.md) 訊息時，您可以視需要滾動清單視圖控制項，以確保可以看見指定的專案。

## <a name="list-view-label-editing"></a>List-View 標籤編輯

具有 [ [**lvs) \_ EDITLABELS**](list-view-window-styles.md) ] 視窗樣式的清單視圖控制項，可讓使用者就地編輯專案標籤。 使用者可以按一下具有焦點之專案的標籤來開始編輯。 或者，應用程式可以使用 [**LVM \_ EDITLABEL**](lvm-editlabel.md) 訊息自動開始編輯。 當編輯開始以及取消或完成時，清單視圖控制項會通知父視窗。 編輯完成時，父視窗會負責更新專案的標籤（如果有的話）。

當標籤編輯開始時，會建立、定位和初始化 [編輯控制項](edit-controls.md) 。 在顯示之前，清單視圖控制項會將 [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) 通知程式碼傳送給其父視窗。 如果您需要修改標籤編輯程式，可以執行此通知的處理常式。

[LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md)通知處理常式的其中一個用途是控制使用者可以編輯的標籤。 若要防止編輯標籤，請傳回非零值。 若要自訂標籤編輯，請將 [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) 訊息傳送至清單視圖控制項，讓通知處理常式取出編輯控制項的控制碼。 有了該控制碼之後，您就可以傳送一般的 EM XXX 訊息來自訂編輯控制項 \_ 。 比方說，若要限制使用者可以輸入的文字數量，請將編輯控制項傳送給 [**EM \_ LIMITTEXT**](em-limittext.md) 訊息。 您可以使用 [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)來變更編輯控制項的預設文字。 您甚至可以將編輯控制項設為子類別，以攔截並捨棄不正確字元。

當標籤編輯遭到取消或完成時，清單視圖控制項會將 [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) 通知程式碼傳送給其父視窗。 *LParam* 參數是 [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)結構的位址。 此結構的 **專案** 成員是 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構，其 **iItem** 成員會識別該專案。 如果取消編輯，則 **LVITEM** 結構的 **PszText** 成員為 **Null**;否則， **pszText** 是已編輯文字的位址。 如果要保留新的標籤，父視窗會負責更新專案的標籤。

## <a name="list-view-colors"></a>List-View 色彩

應用程式可以針對清單視圖控制項，取得並設定三種色彩。



| 色彩                   | 用來取得和設定色彩的訊息                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------|
| 文字色彩              | [**LVM \_GETTEXTCOLOR**](lvm-gettextcolor.md)， [ **LVM \_ SETTEXTCOLOR**](lvm-settextcolor.md)         |
| 文字背景色彩   | [**LVM \_GETTEXTBKCOLOR**](lvm-gettextbkcolor.md)， [ **LVM \_ SETTEXTBKCOLOR**](lvm-settextbkcolor.md) |
| 視窗背景色彩 | [**LVM \_GETBKCOLOR**](lvm-getbkcolor.md)， [ **LVM \_ SETBKCOLOR**](lvm-setbkcolor.md)                 |



 

若要更明顯地自訂清單視圖控制項的外觀，請使用 [NM \_ CUSTOMDRAW (清單視圖) ](nm-customdraw-list-view.md) 或使用視覺化樣式 (查看 [視覺化樣式](themes-overview.md) 和 [啟用視覺化樣式](cookbook-overview.md)) 。

## <a name="arranging-list-items-by-group"></a>依群組排列清單專案

清單視圖控制項的群組功能可讓您以視覺化方式將相關的專案集合分組。 您可以根據專案屬性、屬性或其他特性來建立群組。 這些群組通常會以包含群組名稱的水準標頭在螢幕上分隔。 下列螢幕擷取畫面顯示群組專案。

![清單視圖控制項的螢幕擷取畫面，其中有一個群組中的狗和另一個群組中的貓](images/lv-groups.png)

您可以使用 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) 結構來儲存有關群組的資訊，例如頁首和頁尾文字、群組的目前狀態等等。 群組 API 包含的訊息可讓您藉由將專案新增至群組、將群組新增至視圖、排序群組專案，以及查詢專案大小和其他資訊的群組，來管理群組和群組元素。 例如，您可以使用 [ [**listview \_ SetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupmetrics) ] 和 [ [**listview \_ GetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupmetrics) 宏] 來設定和取出每個群組的顯示參數。

群組可在清單視圖以外的所有視圖中使用。 它無法在具有 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式的控制項上使用。

如需詳細資訊，請參閱 [使用 List-View 控制項](using-list-view-controls.md)。

## <a name="insertion-marks"></a>插入標記

插入標記會顯示將放置拖曳專案的使用者。 當使用者將專案拖曳到 [ **開始** ] 功能表或快速啟動 bar 時，目前會顯示插入標記。 插入標記也適用于設定為 autoarrange 的清單。 當使用者將項目拖曳至另外兩個項目之間的某個點時，插入標記會顯示該項目的預期新位置。 下列螢幕擷取畫面顯示插入標記。

![在清單視圖控制項中，于兩個其他兩個檔案之間拖曳一個檔案時，顯示插入標記的螢幕擷取畫面](images/insertmark.png)

插入標記 API 專案藉由提供可執行點擊偵測的訊息和旗標，來指定插入標記的位置和外觀，以及查詢目前的插入標記大小和外觀的相關資訊，藉此啟用插入標記的位置。

## <a name="see-also"></a>另請參閱

* [虛擬 listview 控制項範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)
