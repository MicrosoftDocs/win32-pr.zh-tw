---
title: 關於 Tree-View 控制項
description: 樹狀檢視控制項是一種顯示專案階層式清單的視窗，例如檔中的標題、索引中的專案，或磁片上的檔案和目錄。
ms.assetid: 10cc7949-dd77-412d-bad1-db8d8a049582
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08743a7ac138a6cea5f766dd91aee2ec714acc2d4c8b98e1f2bee26c42ff9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769784"
---
# <a name="about-tree-view-controls"></a>關於 Tree-View 控制項

樹狀檢視控制項是一種顯示專案階層式清單的視窗，例如檔中的標題、索引中的專案，或磁片上的檔案和目錄。 每個項目都包含標籤和選擇性點陣圖影像，因此，每個項目都可以擁有與自己相關的子項目清單。 藉由按一下專案，使用者可以展開或折迭相關聯的子專案清單。

下圖顯示具有根節點、展開節點和折迭節點的簡單樹狀檢視控制項。 控制項會針對選取的專案使用一個點陣圖，並針對其他專案使用另一個點陣圖。

![顯示階層中五個節點的螢幕擷取畫面;系統會選取一個節點的文字，但節點不會依行彼此連結](images/tv-simple.png)

建立樹狀檢視控制項之後，您可以藉由將訊息傳送至控制項，來加入、移除、排列或其他操作專案。 每個訊息都有一個或多個您可以使用的對應宏，而不是明確地傳送訊息。

本節將討論下列主題。

-   [樹狀檢視樣式](#tree-view-styles)
-   [父專案和子專案](#parent-and-child-items)
-   [專案標籤](#item-labels)
-   [樹狀檢視標籤編輯](#tree-view-label-editing)
-   [樹狀檢視專案位置](#tree-view-item-position)
-   [樹狀檢視專案狀態總覽](#tree-view-item-states-overview)
-   [專案選取](#item-selection)
-   [專案資訊](#item-information)
-   [樹狀檢視影像清單](#tree-view-image-lists)
-   [拖放作業](#drag-and-drop-operations)
-   [樹狀檢視控制項通知訊息](#tree-view-control-notification-messages)
-   [預設 Tree-View 控制訊息處理](#default-tree-view-control-message-processing)
-   [相關主題](#related-topics)

## <a name="tree-view-styles"></a>Tree-View 樣式

樹狀檢視樣式會管理樹狀檢視控制面板的各個層面。 當您建立樹狀檢視控制項時，會設定初始樣式。 您可以使用 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 和 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函式建立樹狀檢視控制項之後，取得並變更樣式。

[**電視 \_ HASLINES**](tree-view-control-window-styles.md)樣式會繪製將子專案連結至其父專案的線條，藉以增強樹狀檢視控制項階層的圖形表示，如下圖所示。

![顯示先前相片順序的螢幕擷取畫面，其中包含加入節點的線條;從根節點遞減的第一行](images/tv-haslines.png)

這個樣式本身不會在階層的根目錄繪製線條。 若要這樣做，您必須結合 [**電視 \_ HASLINES**](tree-view-control-window-styles.md) 和 [**電視 \_ LINESATROOT**](tree-view-control-window-styles.md) 樣式。 結果如下圖所示。

![顯示先前相片順序的螢幕擷取畫面，但開頭為根節點的額外水平線](images/tv-rootlines.png)

使用者可以按兩下父專案，展開或折迭父項目的子專案清單。 具有 [**電視 \_ HASBUTTONS**](tree-view-control-window-styles.md) 樣式的樹狀檢視控制項會將按鈕加入至每個父專案的左邊。 使用者可以按一下按鈕一次，而不是按兩下父元素來展開或折迭子專案。 **電視 \_HASBUTTONS** 不會將按鈕加入至階層根目錄的專案。 若要這樣做，您必須結合 [**電視 \_ HASLINES**](tree-view-control-window-styles.md)、 [**電視 \_ LINESATROOT**](tree-view-control-window-styles.md)和 **電視 \_ HASBUTTONS**。 下圖顯示這種樣式的組合。

![顯示先前相片順序的螢幕擷取畫面，但在兩行的每個頂點具有展開/折迭按鈕](images/tv-hasbuttons.png)

[**電視 \_ 核取方塊**](tree-view-control-window-styles.md)樣式會在每個專案旁邊建立核取方塊。 如果您想要使用核取方塊樣式，必須在建立樹狀檢視控制項之後，以及填入樹狀結構之前，將 **電視 \_ 核取方塊** 樣式 (設定為 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)) 。 否則，視計時問題而定，核取方塊可能會顯示為未選取狀態。 下圖顯示覆選框樣式。

![顯示先前相片順序的螢幕擷取畫面，但每個節點旁邊都有一個核取方塊;已選取兩個核取方塊](images/tv-haschecks.png)

[**電視 \_ FULLROWSELECT**](tree-view-control-window-styles.md)樣式會使選取範圍醒目提示延伸至控制項的全形，而不只是專案本身。 下圖顯示此樣式。

![顯示五個節點的原始相片順序的螢幕擷取畫面，但選取範圍醒目提示會延伸控制項的全形](images/tv-fullrow.png)

[**電視 \_ EDITLABELS**](tree-view-control-window-styles.md)樣式讓使用者可以編輯樹狀檢視專案的標籤。 如需編輯標籤的詳細資訊，請參閱 [樹狀檢視標籤編輯](#tree-view-label-editing)。

如需這些樣式和其他樣式的詳細資訊，請參閱 [樹狀檢視控制項視窗樣式](tree-view-control-window-styles.md)。

## <a name="parent-and-child-items"></a>父專案和子專案

樹狀檢視控制項中的任何專案都可以有相關聯的子專案清單，稱為 *子專案*。 具有一個或多個子專案的專案稱為 *父專案*。 子專案會顯示在其父項目下方，並縮排以表示它是父系的從屬專案。 沒有父代的專案會出現在階層的頂端，並稱為 *根專案*。

若要將專案加入至樹狀檢視控制項，請將 [**TVM \_ INSERTITEM**](tvm-insertitem.md) 訊息傳送至控制項。 訊息會傳回 HTREEITEM 類型的控制碼，可唯一識別該專案。 加入專案時，您必須指定新專案的父專案的控制碼。 如果您在 TVINSERTSTRUCT 結構中指定 **Null** 或 TVI \_ 根目錄值，而不是父 [](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa)專案控制碼，則會將專案新增為根專案。

在任何指定時間內，父項目的子項目清單狀態可以是展開或摺疊。 當其狀態為展開時，表示子項目會顯示在父項目下方。 當它摺疊時，則不會顯示子項目。 當使用者按下父專案時，當使用者按兩下父專案時，清單會自動在展開和折迭狀態之間切換，或者，如果父系具有 [**電視 \_ HASBUTTONS**](tree-view-control-window-styles.md) 樣式，則當使用者按一下與父專案相關聯的按鈕時。 應用程式可以使用 [**TVM \_ 展開**](tvm-expand.md) 訊息來展開或折迭子專案。

當父專案的子專案清單即將展開或折迭時，樹狀檢視控制項會傳送 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 通知訊息給父視窗。 通知會讓應用程式有機會防止變更，或設定相依于子專案清單狀態的父項目的任何屬性。 變更清單的狀態之後，樹狀檢視控制項會將 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md) 通知訊息傳送至父視窗。

當子項目清單展開時，它會以相對於父項目的位置進行縮排。 您可以使用 [**TVM \_ SETINDENT**](tvm-setindent.md) 訊息來設定縮排的數量，或使用 [**TVM \_ setindent**](tvm-getindent.md) 訊息來取得目前的金額。

樹狀檢視控制項會使用從建立樹狀檢視控制項的進程堆積所配置的記憶體。 樹狀檢視中的專案數目上限是以堆積中可用的記憶體數量為基礎。

## <a name="item-labels"></a>專案標籤

當您將專案加入至樹狀檢視控制項時，通常會指定專案標籤的文字。 [**TVM \_ INSERTITEM**](tvm-insertitem.md)訊息包含定義專案屬性的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，包括包含標籤文字的字串。

樹狀檢視控制項會配置儲存每個專案的記憶體;專案標籤的文字會佔用此記憶體的重要部分。 如果您的應用程式在樹狀檢視控制項中維護字串的複本，您可以 \_ 在 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)的 **PSZTEXT** 成員中指定 LPSTR TEXTCALLBACK 值，而不是將實際字串傳遞至樹狀檢視，藉以減少控制項的記憶體需求。 使用 LPSTR \_ TEXTCALLBACK 會讓樹狀檢視控制項在每次需要重新繪製專案時，從父視窗取出專案標籤的文字。 若要取出文字，樹狀檢視控制項會傳送 [izdebski \_ GETDISPINFO](tvn-getdispinfo.md) 通知訊息，其中包含 [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) 結構的位址。 父視窗必須填滿包含結構的適當成員。

## <a name="tree-view-label-editing"></a>Tree-View 標籤編輯

使用者可以直接編輯具有 [**電視 \_ EDITLABELS**](tree-view-control-window-styles.md) 樣式之樹狀檢視控制項中的專案標籤。 按一下具有焦點的項目標籤，使用者就可以開始進行編輯。 應用程式會使用 [**TVM \_ EDITLABEL**](tvm-editlabel.md) 訊息開始編輯。 當編輯開始時，以及取消或完成時，樹狀檢視控制項會通知父視窗。 編輯完成時，父視窗會負責更新專案的標籤（如果有的話）。

當標籤編輯開始時，樹狀檢視控制項會將 [izdebski \_ BEGINLABELEDIT](tvn-beginlabeledit.md) 通知訊息傳送至父視窗。 藉由處理此通知，應用程式可以允許編輯某些標籤，並防止編輯其他標籤。 傳回零可進行編輯，並傳回非零值。

當標籤編輯遭到取消或完成時，樹狀檢視控制項會將 [izdebski \_ ENDLABELEDIT](tvn-endlabeledit.md) 通知訊息傳送至其父視窗。 *LParam* 參數是 [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa)結構的位址。 *Item* 參數是一種 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，用來識別專案並包含已編輯的文字。 如果要保留新的標籤，父視窗會負責更新專案的標籤。 如果取消編輯，則 **TVITEM** 的 **pszText** 成員為零。

在標籤編輯期間（通常是為了回應 [izdebski \_ BEGINLABELEDIT](tvn-beginlabeledit.md) 通知訊息），您可以使用 [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) 訊息來取得編輯標籤所使用之編輯控制項的控制碼。 您可以傳送 [**EM \_ SETLIMITTEXT**](em-setlimittext.md) 訊息給編輯控制項，以限制使用者可以輸入或子類別化編輯控制項來攔截和捨棄無效字元的文字數量。 不過請注意，只有在傳送 izdebski BEGINLABELEDIT *之後* ，才會顯示編輯控制項 \_ 。

## <a name="tree-view-item-position"></a>Tree-View 專案位置

使用 [**TVM \_ INSERTITEM**](tvm-insertitem.md) 訊息將專案加入至樹狀檢視控制項時，會設定專案的初始位置。 此訊息包含 [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) 結構，可指定父代專案的控制碼，以及要插入新專案的專案控制碼。 第二個控制碼必須識別指定父系或其中一個值的子專案： TVI \_ FIRST、TVI \_ LAST 或 TVI \_ SORT。

當 \_ 指定 TVI FIRST 或 TVI \_ LAST 時，樹狀檢視控制項會將新專案放在指定父專案的子專案清單的開頭或結尾。 當 \_ 指定 TVI SORT 時，樹狀檢視控制項會根據專案標籤的文字，以字母順序將新專案插入子專案清單。

您可以使用 [**TVM \_ SORTCHILDREN**](tvm-sortchildren.md) 訊息，以字母順序將父項目的子專案清單放在一起。 訊息包含參數，這個參數會指定是否也要依字母順序排序從指定的父專案遞減的所有子專案層級。

[**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md)訊息可讓您根據所定義的準則來排序子專案。 當您使用這個訊息時，您會指定一個應用程式定義的回呼函式，讓樹狀檢視控制項可以在每次需要決定兩個子專案的相對順序時呼叫。 回呼函數會針對要比較的專案，以及您在傳送 **TVM \_ SORTCHILDRENCB** 時指定的第三個32位值，接收 2 32 位應用程式定義的值。

## <a name="tree-view-item-states-overview"></a>Tree-View 專案狀態總覽

樹狀檢視控制項中的每個專案都有目前的狀態。 每個專案的狀態資訊都包含一組位旗標，以及表示專案狀態影像和重迭影像的影像清單索引。 位旗標會指出專案為已選取、已停用、已展開等等。 在大部分的情況下，樹狀檢視控制項會自動設定專案的狀態以反映使用者動作，例如專案的選取專案。 不過，您也可以使用 [**TVM \_ SETITEM**](tvm-setitem.md) 訊息來設定專案的狀態，而且您可以使用 [**TVM \_ GETITEM**](tvm-getitem.md) 訊息來取得專案的目前狀態。 如需專案狀態的完整清單，請參閱 [樹狀檢視控制項專案狀態](tree-view-control-item-states.md)。

專案的目前狀態是由 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **state** 成員所指定。 樹狀檢視控制項可能會變更專案的狀態，以反映使用者動作，例如選取專案或將焦點設定至專案。 此外，應用程式可變更項目的狀態以停用或隱藏項目，或指定重疊影像或狀態影像。

當您指定或變更專案的狀態時， [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)的 **statemask** 成員會指定要設定的狀態位，而且 **狀態** 成員會包含這些位的新值。

若要設定專案的重迭影像， **statemask** 必須包含 [**TVIS \_ OVERLAYMASK**](tree-view-control-item-states.md) 值，且 **狀態** 必須包含覆迭影像的以一為起始的索引，而這是使用 [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) 宏來向左移動8位的重迭影像。 索引可以是零，以指定無重迭影像。

狀態影像會顯示在專案的圖示旁邊，以指出應用程式定義的狀態。 狀態影像包含在透過傳送 [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md)訊息所指定的 *狀態影像清單* 中。 若要設定專案的狀態影像，請在 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **statemask** 成員中包含 [**TVIS \_ STATEIMAGEMASK**](tree-view-control-item-states.md)值。 結構 **狀態** 成員的位12到15會在要繪製之影像的狀態影像清單中指定索引。

若要設定狀態影像索引，請使用 [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask)。 此宏會接受索引，並適當地設定位12到15。 若要指出專案沒有狀態影像，請將索引設定為零。 這個慣例表示狀態影像清單中的影像零無法用作狀態影像。 若要隔離 **狀態** 成員的位12到15，請使用 [**TVIS \_ STATEIMAGEMASK**](tree-view-control-item-states.md) mask。 如需覆迭和狀態影像的詳細資訊，請參閱 [樹狀檢視影像清單](#tree-view-image-lists)。

## <a name="item-selection"></a>專案選取

樹狀檢視控制項會在選取專案從某個專案變更為另一個專案時，藉由傳送 [izdebski \_ SELCHANGING](tvn-selchanging.md) 和 [izdebski \_ SELCHANGED](tvn-selchanged.md) 通知訊息，來通知父視窗。 兩個通知均包含一個值，該值指定變更為按一下滑鼠或是按下按鍵的結果。 通知還包含取得選取範圍的項目和遺失選取範圍的項目的相關資訊。 您可以使用這項資訊來設定項目屬性，而其屬性則視項目的選取狀態而定。 傳回 **TRUE** 以回應 izdebski \_ SELCHANGING 會防止選取範圍變更，而傳回 **FALSE** 則會允許變更。

應用程式可以藉由傳送 [**TVM \_ SELECTITEM**](tvm-selectitem.md) 訊息來變更選取專案。

## <a name="item-information"></a>專案資訊

樹狀檢視控制項支援許多訊息，這些訊息會抓取控制項中專案的相關資訊。

[**TVM \_ GETITEM**](tvm-getitem.md)訊息可以取出專案的控制碼和屬性。 專案的屬性包括其目前狀態、專案的已選取專案影像清單中的索引，以及 nonselected 的點陣圖影像、指出專案是否有子專案的旗標、專案標籤字串的位址，以及專案的應用程式定義32位值。

[**TVM \_ GETNEXTITEM**](tvm-getnextitem.md)訊息會抓取具有目前專案之指定關聯性的樹狀檢視專案。 訊息可以抓取專案的父系、下一個或上一個可見的專案、第一個子專案，依此類推。

[**TVM \_ GETITEMRECT**](tvm-getitemrect.md)訊息會抓取樹狀檢視專案的周框。 [**TVM \_ GETCOUNT**](tvm-getcount.md)和 [**TVM \_ GETVISIBLECOUNT**](tvm-getvisiblecount.md)訊息會取出樹狀檢視控制項中的專案計數，以及可以在樹狀檢視控制項視窗中完整顯示的專案計數。 您可以使用 [**TVM \_ ENSUREVISIBLE**](tvm-ensurevisible.md) 訊息，確保可以看見特定的專案。

## <a name="tree-view-image-lists"></a>Tree-View 影像清單

樹狀檢視控制項中的每個專案都可以有四個相關聯的點陣圖影像。

-   選取專案時所顯示的影像，例如開啟的資料夾。
-   未選取專案時，顯示的影像（例如關閉的資料夾）。
-   以透明方式在選取的或 nonselected 的影像上繪製的重迭影像。
-   狀態影像，這是顯示在所選或 nonselected 影像左邊的額外影像。 您可以使用狀態影像（例如核取和清除的核取方塊）來表示應用程式定義的專案狀態。

根據預設，樹狀檢視控制項不會顯示專案影像。 若要顯示專案影像，您必須建立影像清單，並將它們與控制項建立關聯。 如需影像清單的詳細資訊，請參閱 [影像清單](image-lists.md)。

樹狀檢視控制項可以有兩個影像清單：一般影像清單和狀態影像清單。 一般影像清單會儲存選取的、nonselected 和重迭影像。 狀態影像清單會儲存狀態影像。 使用 [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 函式來建立影像清單，然後使用其他影像清單函式將點陣圖加入影像清單中。 然後，若要將影像清單與樹狀檢視控制項產生關聯，請使用 [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) 訊息。 [**TVM \_ GETIMAGELIST**](tvm-getimagelist.md)訊息會抓取其中一個樹狀檢視控制項影像清單的控制碼。 如果您需要在清單中新增更多影像，此訊息會很有用。

除了選取和 nonselected 的影像之外，樹狀檢視控制項的一般影像清單最多可包含四個重迭影像。 重迭影像是由以一為基礎的索引來識別，其設計目的是要在選取和 nonselected 的影像上以透明方式繪製。 若要將覆迭遮罩索引指派給標準影像清單中的影像，請呼叫 [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) 函數。

依預設，所有專案都會針對選取和 nonselected 的狀態，顯示一般影像清單中的第一個影像。 此外，根據預設，專案不會顯示重迭影像或狀態影像。 您可以藉由傳送 [**TVM \_ INSERTITEM**](tvm-insertitem.md) 或 [**TVM \_ SETITEM**](tvm-setitem.md) 訊息來變更專案的這些預設行為。 這些訊息會使用 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) 結構來指定專案的影像清單索引。

若要指定專案的已選取和 nonselected 影像，請 \_ \_ 在 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **遮罩** 成員中設定 TVIF SELECTEDIMAGE 和 TVIF 影像位，並在 **iSelectImage** 和 **iImage** 成員中指定控制項的一般影像清單中的索引。 或者，您可以 \_ 在 **ISelectImage** 和 **iImage** 中指定 I IMAGECALLBACK 值，而不是指定索引。 這會讓控制項在每次重新繪製專案時，查詢其父視窗中的影像清單索引。 此控制項會傳送 [izdebski \_ GETDISPINFO](tvn-getdispinfo.md) 通知訊息，以抓取索引。

若要將重迭影像與專案產生關聯，請使用 [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask)宏在專案的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **state** 成員中指定覆迭遮罩索引。 您也必須在 **stateMask** 成員中設定 [**TVIS \_ OVERLAYMASK**](tree-view-control-item-states.md)位。 覆迭遮罩索引是以一為基礎;索引為零表示未指定任何重迭影像。

狀態影像會儲存在個別的狀態影像清單中，並以其索引加以識別。 若要指定狀態影像清單，請傳送 [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) 訊息。 不同于清單視圖控制項（使用以一為基礎的索引來識別狀態影像），樹狀檢視控制項狀態影像會以以零為基底的索引來識別。 不過，索引為零表示該專案沒有狀態影像。 因此，不能使用影像零做為狀態影像。 如需專案狀態和狀態影像的進一步討論，請參閱 [樹狀檢視專案狀態總覽](#tree-view-item-states-overview)。

## <a name="drag-and-drop-operations"></a>拖放作業

當使用者開始拖曳專案時，樹狀檢視控制項會通知父視窗。 當使用者開始拖曳具有滑鼠左鍵的專案時，父視窗會收到 [izdebski \_ BEGINDRAG](tvn-begindrag.md) 通知訊息，而當使用者開始使用右方按鈕拖曳時，會收到 [izdebski \_ BEGINRDRAG](tvn-beginrdrag.md) 通知訊息。 您可以將 [**電視 \_ DISABLEDRAGDROP**](tree-view-control-window-styles.md) 樣式提供給樹狀檢視控制項，以防止樹狀檢視控制項傳送這些通知。

您可以使用 [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) 訊息來取得要在拖曳作業期間顯示的影像。 樹狀檢視控制項會根據所拖曳專案的標籤來建立拖曳點陣圖。 然後，樹狀檢視控制項會建立影像清單、在其中加入點陣圖，並將控制碼傳回影像清單。

您必須提供實際拖曳項目的程式碼。 這通常牽涉到使用影像清單函式的拖曳功能，以及處理 [**wm \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 和 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (或 [**wm \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) 在拖曳作業開始之後傳送至父視窗的訊息。

如果樹狀檢視控制項中的專案是拖放作業的目標，您必須知道滑鼠指標在目標專案上的時間。 您可以使用 [**TVM \_ system.windows.media.visualtreehelper.hittest**](tvm-hittest.md) 訊息來找出。 您可以指定 [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) 結構的位址，其中包含滑鼠指標目前的座標。 當 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式傳回時，結構會包含旗標，指出滑鼠指標相對於樹狀檢視控制項的位置。 如果指標位於樹狀檢視控制項中的專案上方，則結構也會包含該專案的控制碼。

您可以使用 [**TVM \_ SETITEM**](tvm-setitem.md) 訊息，將狀態設定為 [**TVIS \_ DROPHILITED**](tree-view-control-item-states.md) 值，以指出專案是拖放作業的目標。 具有這個狀態的項目會繪製為用來表示拖放目標的樣式。

## <a name="tree-view-control-notification-messages"></a>Tree-View 控制通知訊息

樹狀檢視控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式，將下列通知訊息傳送至其父視窗。



| 通知                                    | Description                                                                            |
|-------------------------------------------------|----------------------------------------------------------------------------------------|
| [IZDEBSKI \_ BEGINDRAG](tvn-begindrag.md)             | 表示拖放作業開始的信號。                                        |
| [IZDEBSKI \_ BEGINLABELEDIT](tvn-beginlabeledit.md)   | 表示就地標籤編輯的開始位置。                                           |
| [IZDEBSKI \_ BEGINRDRAG](tvn-beginrdrag.md)           | 表示滑鼠右鍵已啟動拖放操作。             |
| [IZDEBSKI \_ DELETEITEM](tvn-deleteitem.md)           | 指出刪除特定專案的信號。                                               |
| [IZDEBSKI \_ ENDLABELEDIT](tvn-endlabeledit.md)       | 表示標籤編輯結束的信號。                                                      |
| [IZDEBSKI \_ GETDISPINFO](tvn-getdispinfo.md)         | 要求樹狀檢視控制項顯示專案所需的資訊。           |
| [IZDEBSKI \_ ITEMEXPANDED](tvn-itemexpanded.md)       | 表示父專案的子專案清單已展開或折迭。            |
| [IZDEBSKI \_ ITEMEXPANDING](tvn-itemexpanding.md)     | 表示父專案的子專案清單即將展開或折迭。 |
| [IZDEBSKI \_ KEYDOWN](tvn-keydown.md)                 | 發出鍵盤事件的信號。                                                              |
| [IZDEBSKI \_ SELCHANGED](tvn-selchanged.md)           | 表示選取專案已從某個專案變更為另一個專案。                       |
| [IZDEBSKI \_ SELCHANGING](tvn-selchanging.md)         | 表示選取專案即將從某個專案變更為另一個專案。            |
| [IZDEBSKI \_ SETDISPINFO](tvn-setdispinfo.md)         | 通知父視窗，它必須更新它為專案維護的資訊。 |



 

## <a name="default-tree-view-control-message-processing"></a>預設 Tree-View 控制訊息處理

本節說明由樹狀檢視控制項所執行的視窗訊息處理。 這份檔的其他章節將討論樹狀檢視控制項特定的訊息，因此不包含在此。



| 訊息                                            | 處理已執行                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 命令**](/windows/desktop/menurc/wm-command)               | 處理 [en \_ UPDATE](en-update.md) 和 [en \_ KILLFOCUS](en-killfocus.md) 編輯控制項通知訊息，並將所有其他編輯控制項通知轉寄至父視窗。 沒有傳回值。                                                                                                                                                                                                                                                                                                |
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)                 | 配置記憶體並初始化內部資料結構。 如果成功，則會傳回零，否則會傳回-1。                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)               | 釋出與控制項相關聯的所有系統資源。 它會傳回零。                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_啟用 WM**](/windows/desktop/winmsg/wm-enable)                 | 啟用或停用控制項。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | 使用樹狀檢視控制項目前的背景色彩，清除視窗背景。 它會傳回 **TRUE**。                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | 傳回 DLGC \_ WANTARROWS 和 DLGC WANTCHARS 值的組合 \_ 。                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | 傳回目前標籤字型的控制碼。                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**WM \_ HSCROLL**](wm-hscroll.md)                  | 滾動樹狀檢視控制項。 如果發生滾動，則會傳回 **TRUE** ，否則會傳回 **FALSE** 。                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)             | 將 [izdebski \_ KEYDOWN](tvn-keydown.md) 通知訊息傳送至所有索引鍵的父視窗。 當使用者按下 ENTER 鍵時，會將 [NM \_ RETURN (樹狀檢視) ](nm-return-tree-view-.md) 通知訊息。 它會在使用者按下方向鍵或 PAGE UP、PAGE DOWN、HOME、END 或倒退鍵時移動插入號。 當使用者按下 CTRL 鍵與這些按鍵組合時，它會滾動樹狀檢視控制項。 如果已處理索引鍵，則傳回 **TRUE** ，否則傳回 **FALSE** 。 |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)         | 重新繪製焦點的專案（如果有的話），然後將 [NM \_ KILLFOCUS (樹狀檢視) ](nm-killfocus-tree-view.md) 通知訊息傳送至父視窗。                                                                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | 取消標籤編輯，如果按兩下專案，則會將 [NM \_ DBLCLK (樹狀檢視) ](nm-dblclk-tree-view.md) 通知訊息傳送至父視窗。 如果父視窗傳回0，則樹狀檢視控制項會切換專案的展開狀態，並將 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 和 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md) 通知訊息傳送至父視窗。 沒有傳回值。                                                                             |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | 如果使用者按一下與父專案相關聯的按鈕，則切換展開的狀態。 如果使用者按一下專案標籤，樹狀檢視控制項會選取焦點，並將焦點設定至專案。 如果使用者在放開滑鼠按鍵之前移動滑鼠，則樹狀檢視控制項會開始拖放作業。 沒有傳回值。                                                                                                                                                                          |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                      | 繪製樹狀檢視控制項的無效區域。 它會傳回零。 如果 *wParam* 參數不是 **Null**，則控制項會假設此值是裝置內容的控制碼 (HDC) 並且使用該裝置內容繪製。                                                                                                                                                                                                                                                                                      |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)     | 檢查是否已按一下專案，並已開始拖曳作業。 如果作業已開始，則會將 [izdebski \_ BEGINRDRAG](tvn-beginrdrag.md) 通知訊息傳送至父視窗，並反白顯示放置目標。 否則，它會將 [NM \_ RCLICK (樹狀檢視) ](nm-rclick-tree-view.md) 通知訊息傳送至父視窗。 沒有傳回值。                                                                                                                                           |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | 重新繪製焦點的專案（如果有的話），然後將 [NM \_ SETFOCUS](nm-setfocus.md) 通知訊息傳送至父視窗。                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | 使用新字型儲存指定的字型控點，並重新繪製樹狀檢視控制項。                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)              | 設定或清除重繪旗標。 在設定重繪旗標之後，會重新繪製樹狀檢視控制項。 它會傳回零。                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ 大小**](/windows/desktop/winmsg/wm-size)                     | 旁邊相依于樹狀檢視控制項工作區大小的內部變數。 它會傳回 **TRUE**。                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ STYLECHANGED**](/windows/desktop/winmsg/wm-stylechanged)     | 使用新樣式取消編輯標籤，並重新繪製樹狀檢視控制項。 它會傳回零。                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange)    | 如果已設定重繪旗標，則會使用新的色彩來重繪樹狀檢視控制項。 沒有傳回值。                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**WM \_ 計時器**](/windows/desktop/winmsg/wm-timer)                   | 開始編輯專案標籤。 如果使用者按一下焦點專案的標籤，樹狀檢視控制項會設定計時器，而不是立即進入編輯模式。 計時器讓樹狀檢視可以避免在使用者按兩下標籤時進入編輯模式。 它會傳回零。                                                                                                                                                                                                                       |
| [**WM \_ VSCROLL**](wm-vscroll.md)                  | 滾動樹狀檢視控制項。 如果發生滾動，則會傳回 **TRUE** ，否則會傳回 **FALSE** 。                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[範例： CustDTv 說明 TreeView 中的自訂繪製 (Q248496) ](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 