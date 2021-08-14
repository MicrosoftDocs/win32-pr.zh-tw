---
description: 多重文件介面中的每份檔 (MDI) 應用程式會顯示在應用程式主視窗工作區的個別子視窗中。
ms.assetid: 35dff281-3b11-4954-85cf-a0f1c9ed346a
title: 關於多重文件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071d3bebad8e6aba48b69b66fd41f9f7933c1d9785ae38512003aaf1bd9a19e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705996"
---
# <a name="about-the-multiple-document-interface"></a>關於多重文件介面

多重文件介面中的每份檔 (MDI) 應用程式會顯示在應用程式主視窗工作區的個別子視窗中。 一般的 MDI 應用程式包括文字處理應用程式，可讓使用者使用多個文字檔，以及允許使用者使用多個圖表和試算表的試算表應用程式。 如需詳細資訊，請參閱下列主題。

-   [框架、用戶端和子 Windows](#frame-client-and-child-windows)
-   [子視窗建立](#child-window-creation)
-   [子視窗啟用](#child-window-activation)
-   [多個檔功能表](#multiple-document-menus)
-   [多個檔加速器](#multiple-document-accelerators)
-   [子視窗大小和相片順序](#child-window-size-and-arrangement)
-   [圖示標題 Windows](#icon-title-windows)
-   [子視窗資料](#child-window-data)
    -   [視窗結構](#window-structure)
    -   [視窗屬性](#window-properties)

## <a name="frame-client-and-child-windows"></a>框架、用戶端和子 Windows

MDI 應用程式有三種視窗：框架視窗、MDI 用戶端視窗，以及許多子視窗。 *框架視窗* 就像是應用程式的主視窗：它具有調整大小框線、標題列、視窗功能表、最小化按鈕，以及最大化按鈕。 應用程式必須為框架視窗註冊視窗類別，並提供視窗程式來支援它。

MDI 應用程式不會在框架視窗的工作區中顯示輸出。 相反地，它會顯示 MDI 用戶端視窗。 *MDI 用戶端視窗* 是一種特殊類型的子視窗，屬於預先註冊視窗類別 **MDICLIENT**。 用戶端視窗是框架視窗的子系;它是子視窗的背景。 它也提供建立和操作子視窗的支援。 例如，MDI 應用程式可以藉由將訊息傳送至 MDI 用戶端視窗，來建立、啟動或最大化子視窗。

當使用者開啟或建立檔時，用戶端視窗會建立檔的子視窗。 用戶端視窗是應用程式中所有 MDI 子視窗的父視窗。 每個子視窗都有調整框線、標題列、視窗功能表、最小化按鈕，以及最大化按鈕。 因為子視窗被裁剪，所以會限制在用戶端視窗之外，而且不能出現在其外部。

MDI 應用程式可以支援一種以上的檔。 例如，一般試算表應用程式可讓使用者同時使用圖表和試算表。 針對每一種支援的檔案類型，MDI 應用程式必須註冊子視窗類別，並提供視窗程式來支援屬於該類別的 windows。 如需視窗類別的詳細資訊，請參閱 [視窗類別](window-classes.md)。 如需視窗程式的詳細資訊，請參閱 [視窗程式](window-procedures.md)。

以下是一般的 MDI 應用程式。 它會命名為 Multipad。

![multipad mdi 應用程式框架視窗和用戶端視窗](images/csmdi-01.png)

## <a name="child-window-creation"></a>子視窗建立

若要建立子視窗，MDI 應用程式可以呼叫 [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) 函式，或將 [**WM \_ MDICREATE**](wm-mdicreate.md) 訊息傳送至 MDI 用戶端視窗。 更有效率的建立 MDI 子視窗的方式是呼叫 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式，並指定 **WS \_ EX \_ MDICHILD** 延伸樣式。

為了終結子視窗，MDI 應用程式會將 [**WM \_ MDIDESTROY**](wm-mdidestroy.md) 訊息傳送至 mdi 用戶端視窗。

## <a name="child-window-activation"></a>子視窗啟用

任何數目的子視窗都可以在用戶端視窗中一次出現，但只能有一個作用中。 作用中的子視窗位於所有其他子視窗的前方，而且其框線會反白顯示。

使用者可以按一下非使用中的子視窗來加以啟用。 MDI 應用程式會將 [**WM \_ MDIACTI加值稅E**](wm-mdiactivate.md) 訊息傳送至 MDI 用戶端視窗，以啟動子視窗。 當用戶端視窗處理此訊息時，它會將 **WM \_ MDIACTI加值稅E** 訊息傳送至要啟動之子視窗的視窗程式，以及要停用之子視窗的視窗程式。

若要防止子視窗啟動，請傳回 **FALSE**，以將 [**WM \_ NCACTI加值稅E**](wm-ncactivate.md)訊息處理至子視窗。

系統會在重迭視窗的堆疊中追蹤每個子視窗的位置。 此堆疊稱為 [Z 順序](window-features.md)。 使用者可以從使用中視窗中的 [視窗] 功能表按一下 [ **下一步** ]，以 Z 順序啟動下一個子視窗。 應用程式會藉由將 [**WM \_ MDINEXT**](wm-mdinext.md) 訊息傳送至用戶端視窗，來啟動 Z 順序中的下一個 (或先前) 子視窗。

為了取得作用中子視窗的控制碼，MDI 應用程式會將 [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md) 訊息傳送至用戶端視窗。

## <a name="multiple-document-menus"></a>多個檔功能表

MDI 應用程式的框架視窗應該包含具有視窗功能表的功能表列。 [視窗] 功能表應該包含在用戶端視窗中排列子視窗，或關閉所有子視窗的專案。 一般 MDI 應用程式的 [視窗] 功能表可能包含下表中的專案。



| 功能表項目         | 目的                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **磚**          | 以磚格式排列子視窗，使其在用戶端視窗中全部出現。                       |
| **級 聯**       | 以 cascade 格式排列子視窗。 子視窗彼此重迭，但每個的標題列都是可見的。 |
| **排列圖示** | 在用戶端視窗底部排列最小化子視窗的圖示。                                     |
| **全部關閉**     | 關閉所有子視窗。                                                                                                |



 

每當建立子視窗時，系統會自動將新的功能表項目附加至 [視窗] 功能表。 功能表項目的文字與新子視窗的功能表列上的文字相同。 藉由按一下功能表項目，使用者可以啟動對應的子視窗。 當子視窗損毀時，系統會自動從 [視窗] 功能表中移除對應的功能表項目。

系統最多可將十個功能表項目新增至 [視窗] 功能表。 當第十個子視窗建立時，系統會將 **更 Windows** 的專案加入至 [視窗] 功能表。 按一下這個專案，就會顯示 [ **選取視窗** ] 對話方塊。 此對話方塊包含清單方塊，其中包含目前可用的所有 MDI 子視窗的標題。 使用者可以在清單方塊中按一下其標題，以啟用子視窗。

如果您的 MDI 應用程式支援數種類型的子視窗，請調整功能表列，以反映與使用中視窗相關聯的作業。 若要這樣做，請為應用程式支援的每個子視窗類型提供個別的功能表資源。 當啟用新的子視窗類型時，應用程式應該將 [**WM \_ MDISETMENU**](wm-mdisetmenu.md) 訊息傳送至用戶端視窗，並將控制碼傳遞至對應的功能表。

當沒有子視窗存在時，功能表列應該只包含用來建立或開啟檔的專案。

當使用者使用游標按鍵流覽 MDI 應用程式的功能表時，索引鍵的行為會與使用者流覽一般應用程式功能表時的行為不同。 在 MDI 應用程式中，控制權會從應用程式的 [視窗] 功能表移至 [作用中子視窗] 的 [視窗] 功能表，然後再傳遞至功能表列上的第一個專案。

## <a name="multiple-document-accelerators"></a>多個檔加速器

若要接收和處理其子視窗的快速鍵，MDI 應用程式必須在其訊息迴圈中包含 [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) 函式。 迴圈必須先呼叫 **TranslateMDISysAccel** ，然後再呼叫 [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) 或 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 函數。

MDI 子視窗的 [視窗] 功能表上的快速鍵會與非 MDI 子視窗的快速鍵不同。 在 MDI 子視窗中，ALT + – (減號) 按鍵組合會開啟 [視窗] 功能表、CTRL + F4 按鍵組合會關閉作用中的子視窗，而 CTRL + F6 按鍵組合會啟動下一個子視窗。

## <a name="child-window-size-and-arrangement"></a>子視窗大小和相片順序

MDI 應用程式會藉由將訊息傳送至 MDI 用戶端視窗，來控制其子視窗的大小和位置。 為了最大化作用中的子視窗，此應用程式會將 [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md) 訊息傳送至用戶端視窗。 當子視窗最大化時，其用戶端區域就會完全填滿 MDI 用戶端視窗。 此外，系統會自動隱藏子視窗的標題列，並將子視窗的 [視窗] 功能表圖示和 [還原] 按鈕加入至 MDI 應用程式的功能表列。 應用程式可以將用戶端視窗還原至其原始 (premaximized) 大小和位置，方法是將用戶端視窗傳送至 [**WM \_ MDIRESTORE**](wm-mdirestore.md) 訊息。

MDI 應用程式可以使用 cascade 或圖格格式來排列其子視窗。 當子視窗進行串聯時，視窗會出現在堆疊中。 堆疊底部的視窗會佔用畫面的左上角，其餘視窗則會垂直和水準位移，讓每個子視窗的左邊框線和標題列都可以看見。 為了以串聯格式排列子視窗，MDI 應用程式會傳送 [**WM \_ MDICASCADE**](wm-mdicascade.md) 訊息。 一般情況下，當使用者按一下 [視窗] 功能表上的 [ **Cascade** ] 時，應用程式就會傳送此訊息。

將子視窗並排顯示時，系統會將每個子視窗全部顯示，而不會重迭任何視窗。 所有視窗都是根據需要調整，以符合用戶端視窗的大小。 為了排列磚格式的子視窗，MDI 應用程式會將 [**WM \_ MDITILE**](wm-mditile.md) 訊息傳送至用戶端視窗。 一般來說，當使用者按一下 [視窗] 功能表上的 [ **圖** 格] 時，應用程式就會傳送此訊息。

MDI 應用程式應該為其支援的每個子視窗類型提供不同的圖示。 應用程式會在註冊子視窗類別時，指定一個圖示。 當子視窗最小化時，系統會自動在用戶端視窗的下半部顯示子視窗的圖示。 MDI 應用程式會將 [**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md) 訊息傳送至用戶端視窗，以指示系統排列子視窗圖示。 一般情況下，應用程式會在使用者按一下 [視窗] 功能表上的 [ **排列圖示** ] 時傳送此訊息。

## <a name="icon-title-windows"></a>圖示標題 Windows

由於 MDI 子視窗可能會最小化，因此 MDI 應用程式必須避免將圖示標題視窗視為一般的 MDI 子視窗來操作。 當應用程式列舉 MDI 用戶端視窗的子視窗時，就會出現圖示標題視窗。 圖示標題視窗與其他子視窗不同，但它們是由 MDI 子視窗所擁有。

若要判斷子視窗是否為圖示標題視窗，請使用 [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) 函式搭配 GW \_ 擁有者索引。 非標題視窗傳回 **Null**。 請注意，此測試不適用於最上層視窗，因為功能表和對話方塊是擁有的視窗。

## <a name="child-window-data"></a>子視窗資料

由於子視窗的數目視使用者開啟的檔數目而異，因此 MDI 應用程式必須能夠將資料 (例如，目前檔案的名稱與每個子視窗) 。 作法有二：

-   將子視窗資料儲存在視窗結構中。
-   使用視窗屬性。

### <a name="window-structure"></a>視窗結構

當 MDI 應用程式註冊視窗類別時，它可能會在視窗結構中保留額外的空間，以供此特定 windows 類別專用的應用程式資料使用。 若要在這個額外的空間中儲存和取出資料，應用程式會使用 [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) 和 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函數。

若要維護子視窗的大量資料，應用程式可以配置資料結構的記憶體，然後將此控制碼儲存在與子視窗相關聯的額外空間中，包含結構的記憶體。

### <a name="window-properties"></a>視窗屬性

MDI 應用程式也可以使用視窗屬性來儲存每一份檔的資料。 *每一檔資料* 是特定子視窗中包含之檔案類型的特定資料。 屬性與視窗結構中的額外空間不同，因為在註冊視窗類別時，您不需要配置額外的空間。 視窗可以有任意數目的屬性。 此外，使用位移來存取視窗結構中的額外空間時，屬性是由字串名稱所參考。 如需有關視窗屬性的詳細資訊，請參閱 [視窗屬性](window-properties.md)。

 

 
