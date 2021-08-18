---
description: 筆跡集合的開頭是數位板。
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: 筆墨集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45988ea93aac5016391e22c352b9d0123a5e122f4a79c55e41e06834ed040e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452064"
---
# <a name="ink-collection"></a>筆墨集合

筆跡集合的開頭是數位板。 使用者將畫筆放在數位板上，然後開始撰寫。 您可以使用 API 的筆墨集合功能來管理從畫筆「流程」的筆墨資料收集。 您可以透過 [**平板**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) 電腦集合和 [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 物件存取 tablet PC 上可用硬體的相關資訊。 然後，您可以使用 [**InkCollector**](inkcollector-class.md) 物件來取得來自數位板的資料。

## <a name="tablets-and-the-tablet-object"></a>平板電腦和平板電腦物件

[**平板**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)電腦代表 tablet PC 的數位板裝置。 Tablet PC 可能會有一個以上的數位板。 您可以使用 **tablet** 物件來查詢連接到 tablet PC 的可用數位板裝置，以及其各自的硬體功能。 例如，您可以判斷您正在使用的 **平板** 電腦是否與顯示器整合，或是否為個別的外部裝置。

## <a name="inkcollector-object"></a>InkCollector 物件

[**InkCollector**](inkcollector-class.md)物件會從可用的 [**平板**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)電腦裝置捕捉筆墨輸入。 **InkCollector** 物件只會收集在特定視窗中輸入的筆墨和手勢。 非常有效率的事件接收器會即時呈現此輸入。 **InkCollector** 物件會捕捉輸入，並將它導向至 [**筆墨**](inkdisp-class.md)物件。

> [!Note]  
> 視數位板裝置的硬體功能而定，使用多個畫筆來同時配置筆墨的功能可能會或可能無法運作。

 

### <a name="how-the-ink-collector-works"></a>筆墨收集器的運作方式

[**InkCollector**](inkcollector-class.md)物件會將本身附加至已知的應用程式視窗。 然後，使用者可以運用任何可用的 Tablet PC 裝置 (包括滑鼠) ，以在該時間範圍內即時配置筆墨。 它所收集的筆墨筆觸會儲存在相關聯的 [**筆墨**](inkdisp-class.md) 物件中。 然後可以操作這些筆劃，或將它們傳送至辨識器進行辨識。 當游標進入所使用的任何 Tablet PC 裝置的範圍時， **InkCollector** 物件也會通知應用程式。

若要讓 [**InkCollector**](inkcollector-class.md) 物件將滑鼠游標正確地設定在啟用筆墨的視窗中，該視窗必須能夠接收 **WM \_ SETCURSOR** 訊息。 這對所有一般視窗都是成功的，但針對對話方塊內的控制項，控制項的對話方塊父系會篩選此訊息。 若要讓控制項接收訊息，請設定 **SS \_ 通知** 樣式。

## <a name="inkoverlay-object"></a>InkOverlay 物件

先前討論的 [**InkCollector**](inkcollector-class.md) 物件適用于應用程式提供自己的模型來選取、清除和其他使用者互動。 [**InkOverlay**](inkoverlay-class.md)物件是提供編輯支援之 **InkCollector** 物件的超集合。 這適用于應用程式使用物件提供的一組標準筆墨選取模型，將筆墨繪圖和編輯整合到自己的檔畫布中。

[**InkCollector**](inkcollector-class.md)物件和 [**InkOverlay**](inkoverlay-class.md)物件 (以及 [InkPicture](inkpicture-control.md)控制項) 使用一般的結構，例如 [**筆墨**](inkdisp-class.md)物件和 [**DrawingAttributes**](inkdrawingattributes-class.md)集合，因此變更筆跡色彩的基本方式在所有地方都相同。 這可讓您重複使用程式碼並具有一般的程式設計存取，如果您在應用程式中提供腳本支援，這可能特別重要。

[**InkOverlay**](inkoverlay-class.md) 是一種 COM 物件，適用于注釋案例，在此情況下，使用者不在意筆墨的執行辨識，而是對筆跡的大小、圖形、色彩和位置感興趣。 它非常適合用來取得筆記和基本 scribbling。 預設使用者介面是透明的矩形，其筆墨不透明。

[**InkOverlay**](inkoverlay-class.md) 以三種方式擴充 [**InkCollector**](inkcollector-class.md) 類別：

-   它會引發開始-筆劃、結束筆劃和筆墨屬性變更的事件。
-   它可讓使用者選取、清除及調整筆跡的大小。
-   它支援剪下、複製和貼上命令。

當您標示簡報投影片或影像時，很適合使用 [**InkOverlay**](inkoverlay-class.md) 的一般案例。 **InkOverlay** 物件可讓您輕鬆地執行此案例所需的筆墨和版面配置功能。

若要使用 [**InkOverlay**](inkoverlay-class.md)，您可以：

1.  具現化 [**InkOverlay**](inkoverlay-class.md) 物件。
2.  在 managed 程式碼) 中，將 hWnd (控制碼（在視窗的 managed 程式碼) ）附加至 [**InkOverlay**](inkoverlay-class.md) 物件的 [**HWnd**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) 屬性 ([處理](/previous-versions/ms582171(v=vs.100)) 屬性。
3.  將 [ [**InkOverlay**](inkoverlay-class.md) ] 物件的 [ [**已啟用**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) ] 屬性設定為 [ **TRUE**]。

[**InkOverlay**](inkoverlay-class.md)物件包含基本列印支援，但您必須執行預覽列印或其他先進的列印功能。

[**InkOverlay**](inkoverlay-class.md) 將筆墨序列化格式的筆墨保存 (ISF) 。

> [!Note]  
> 如果 [**InkOverlay**](inkoverlay-class.md) 物件的 [**system.windows.controls.inkcanvas.editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) 設定為 [ **刪除** ] 或 [ **選取**]，則會觸發其他事件 (例如 [**InkAdded**](inkdisp-inkadded.md)、 [**InkDeleted**](inkdisp-inkdeleted.md)和 [**筆觸**](inkoverlay-stroke.md)) 。 如果您想要執行自己的刪除或選取模式，這些事件會很有用。

 

### <a name="selecting-ink"></a>選取筆墨

[**InkOverlay**](inkoverlay-class.md)物件可讓使用者使用「套索」工具來選取包含在追蹤區域中的筆跡物件。 使用者也可以藉由點擊任何 [**筆墨**](inkdisp-class.md) 物件來選取筆跡。

您可以使用 [ [**選取範圍**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) ] 屬性來傳回 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合，以用來操作使用者的選取專案。

選取 [**筆墨**](inkdisp-class.md) 物件或 **筆跡** 物件集時，調整大小控點會出現在筆跡周框方塊的四個角落，以及相鄰角落之間的所有中間點。 如果使用者在所選區域內的任何位置拖曳，則筆墨會在控制項內變成可移動的。

### <a name="default-behavior"></a>預設行為

[**InkOverlay**](inkoverlay-class.md)物件預設會設定為收集筆跡。 筆墨是53筆墨空間單位範圍 (，其中1個筆墨空間單位 = 1 HIMETRIC) 。 如果使用者不是在高對比模式下執行，則筆墨為黑色。 否則，會在 managed 程式碼) 中，將筆墨設定為 **色彩 \_ WINDOWTEXT** 值 (**WINDOWTEXT** 。 [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) 為 **FALSE**。

### <a name="cursor-and-button-objects"></a>Cursor 和 Button 物件

游標對應于 Tablet PC 上使用的畫筆提示。 比方說，鉛筆有兩個端點。 通常會使用一端進行寫入，而另一端用於清除。 這兩個端點會對應至兩個數據指標。 [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)類別不會與 [**System. Windows 混淆。表單. Cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1)。

在 Tablet PC 上，通常會定義使用資料指標來寫入或清除。 如果應用程式啟用此功能，資料指標可能會變更角色。 某些 Tablet PC 裝置允許多個畫筆。 每個資料指標都有一個相關聯的資料指標識別碼，在系統上是唯一的。 資料指標可以有零或多個相關聯的按鈕。 這些按鈕會以 CursorButton 物件的形式提供給應用程式。 應用程式可以為任何給定的資料指標提供特定的 [**DrawingAttributes**](inkdrawingattributes-class.md) 物件。

### <a name="drawing-attributes-object"></a>繪圖屬性物件

[**DrawingAttributes**](inkdrawingattributes-class.md)物件說明要如何繪製任何已知的筆墨集。 **DrawingAttributes** 物件包含基本屬性，例如 [**色彩**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)、[**寬度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)和 [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)。 它也可以包含可提供有趣效果或改善筆墨可讀性的 advanced 參數，例如可變透明度和貝塞爾凹凸貼圖。

### <a name="peninputpanel-object"></a>PenInputPanel 物件

> [!Note]  
> [**PenInputPanel**](peninputpanel-class.md)類別已被取代。 **PenInputPanel** 類別已由 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)類別取代。

 

[**PenInputPanel**](peninputpanel-class.md)物件可讓您輕鬆地將就地畫筆輸入新增至您的應用程式。 **PenInputPanel** 是以可附加的物件形式提供，可讓您將 Tablet PC 輸入面板功能新增至現有的控制項。 使用者介面大多是由目前的輸入語言所規定。 您可以選擇針對 **PenInputPanel**（手寫或鍵盤）選擇預設的輸入方法。 終端使用者可以使用使用者介面上的按鈕，在輸入方法之間切換。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**InkCollector 類別 (c + +)**](inkcollector-class.md)
</dt> <dt>

[**InkOverlay 類別 (c + +)**](inkoverlay-class.md)
</dt> <dt>

[**Microsoft Ink 命名空間**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
