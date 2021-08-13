---
description: Windows Vista 的發行版本包含了 [Tablet PC 輸入面板] 的新可程式性物件，可提供應用程式如何使用和與輸入面板互動的新範圍。
ms.assetid: 539f41d3-5fb8-4e20-99ba-0d5af1f0cc54
title: 適用于 PenInputPanel 使用者的 TextInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd75fddb929dfd9e0e783aefc0d3f57743d23d5c35f23c845a9745660512f52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119222159"
---
# <a name="textinputpanel-for-users-of-peninputpanel"></a>適用于 PenInputPanel 使用者的 TextInputPanel

Windows Vista 的發行版本包含了 [Tablet PC 輸入面板] 的新可程式性物件，可提供應用程式如何使用和與輸入面板互動的新範圍。 第一次，應用程式開發人員可以將 In-Place 輸入面板圖示定位至文字方塊中，或將它放在客戶筆跡表面的角落，以提供替代輸入模式的存取權。 當輸入面板圖示展開至 In-Place 輸入面板之後，開發人員就會有相同的定位控制權。 如此一來，就可以確保 In-Place 輸入面板永遠不會與應用程式佈建中的主要使用者介面元素重迭，或甚至是重新排列應用程式的使用者介面，以為 In-Place 輸入面板建立空間，然後將它放在保留空間中。 新的可程式性模型不僅支援定位，開發人員也可以自訂輸入區域、更正模式以及許多其他的輸入面板屬性，以在應用程式中量身訂做文字輸入體驗。 最後，在第一次，應用程式可能會接收使用者筆跡，除了可辨識的文字之外，還能與輸入面板中的文字插入相關聯。 這會啟用新的應用程式案例，包括變更追蹤記錄中的筆墨，以及允許使用者在應用程式中編輯或查看筆墨。 這些新的程式設計功能是 Microsoft 針對輸入面板開發人員故事所收到意見反應的直接結果，並代表更緊密地整合應用程式與輸入面板的第一步。

為了提供此擴充的輸入面板可程式化模型，現有的機制可以用程式設計方式與輸入面板互動， [**PenInputPanel**](peninputpanel-class.md) 物件會被取代，並取代為新的 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件。 除了提供新的程式設計功能之外， **TextInputPanel** 物件也提供 **PenInputPanel** 物件的所有程式設計功能。 **TextInputPanel** 物件包含在 Windows vista 和 Windows vista 軟體發展人員套件中。 **TextInputPanel** 物件只與 Windows Vista 輸入面板相容，且不能與 Windows XP Service Pack 2 或舊版的輸入面板一起使用。 先前撰寫為使用 **PenInputPanel** 物件的應用程式將繼續使用 Windows Vista 輸入面板，不過，在撰寫新的平板電腦應用程式時，強烈建議您使用新的 **TextInputPanel** 物件，而不是已被取代的 **PenInputPanel** 物件。

[**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)物件的每個可程式性選項，都可以根據每個文字欄位來套用。 使用 [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_attachededitwindow)屬性附加 **TextInputPanel** 物件的實例，即可完成這項作業。 屬性應該設定為文字欄位的視窗控制碼。

> [!Note]  
> ：當輸入面板處於就地互動模式時，以及當輸入面板處於浮動或停駐互動模式時，會套用下列幾個屬性和方法所述。 就地互動模式是將焦點放在可編輯欄位中的輸入面板行為，會導致輸入面板圖示出現在欄位旁，而按下輸入面板圖示會導致輸入面板展開。 只有當輸入面板處於就地互動模式時，才會套用的方法和屬性會在方法或屬性名稱中包含「就地」。

 

## <a name="control-of-input-panel-icon-and-input-panel-visibility"></a>輸入面板圖示和輸入面板可見度的控制權

輸入面板的第一個層面，是應用程式開發人員在 Windows Vista 中更能掌控的部分。 您可以使用 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件，以三種方式控制 In-Place 輸入面板的可見度。 使用屬性和方法的組合，應用程式可以判斷 In-Place 輸入面板是否顯示、In-Place 輸入面板顯示時，以及它是先顯示為輸入面板圖示或立即顯示展開。 藉由結合這些技術，以控制在下一節中所討論的定位技術，應用程式開發人員可以使用應用程式中的 In-Place 輸入面板來建立自訂啟動點和自訂工作流程。

> [!Note]  
> 只有當輸入面板處於 In-Place 互動模式時，本節中所討論的屬性和方法才適用。

 

首先，最重要的是，將 [**InPlaceVisibleOnFocus**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplacevisibleonfocus) 屬性設定為 **false**，就可以防止出現 In-Place 輸入面板和輸入面板圖示。 將它設定為 **true** 會將它還原為系統預設值（如果可能的話），但前提是使用者未停用它或群組原則。 此選項適用于包含自訂文字輸入解決方案的應用程式，做為輸入面板的替代方案。

其次，藉由設定 [**DefaultInPlaceState**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_defaultinplacestate) 屬性，開發人員可以指定 [**InPlaceState**](/windows/win32/api/peninputpanel/ne-peninputpanel-inplacestate) 列舉所指定的就地狀態，當焦點放在文字欄位時，In-Place 輸入面板就會出現在中。 系統預設 In-Place 值為，除非輸入面板已在展開狀態中，否則 [輸入面板] 會出現在 [暫止] 狀態中，否則 [輸入面板] 會維持展開狀態。 將 [ **DefaultInPlaceState** ] 屬性設定為 [ **\_ 展開 InPlaceState** ] 會導致 In-Place 輸入面板一律會顯示為展開狀態，而不是先出現輸入面板圖示，然後在輸入面板展開之前要求使用者先點擊輸入面板圖示。 另外兩個選項是 **InPlaceState \_ Auto**，也就是系統預設行為和 **InPlaceState \_ HoverTarget** ，一律會顯示輸入面板圖示。 指定 In-Place 輸入面板一律會一直展開的功能是 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件的新功能，而且不可能使用 [**PenInputPanel**](peninputpanel-class.md) 物件。 下圖顯示面板的 In-Place 輸入面板圖示和展開的狀態。

![就地輸入面板圖示和展開的狀態](images/8ce866b6-9a45-499f-a3d1-95a1d34d6402.jpg)

除了能夠控制就地狀態之外，開發人員也有可能藉由取得 [**CurrentInPlaceState**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentinplacestate) 屬性，在指定的時間決定就地狀態。 當輸入面板不可見時， **CurrentInPlaceState** 等於 [**DefaultInPlaceState**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_defaultinplacestate) ，除非 **DefaultInPlaceState** **InPlaceState \_ Auto** ，否則 **CurrentInPlaceState** 會變成 **InPlaceState \_ HoverTarget**。 [**InPlaceVisibilityChanging**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanging)  /  [**InPlaceVisibilityChanged**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanged)事件可以用來追蹤 In-Place 輸入面板的可見度狀態。

最後，開發人員可以強制 In-Place 的輸入面板使用 [**SetInPlaceVisibility**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacevisibility) 方法來隱藏或顯示。 如果開發人員先前已設定 [**DefaultInPlaceState**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_defaultinplacestate) 屬性，當強制顯示時，輸入面板會顯示為指定的狀態。 只有當焦點目前位於 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件所連接的視窗中，以及當使用者未在另一個互動模式（例如停駐或浮動）中開啟輸入面板時，才允許應用程式隱藏或顯示 In-Place 輸入面板。 強制 In-Place 輸入面板隱藏或顯示的功能也是 **TextInputPanel** 物件的新功能，而且不可能使用 [**PenInputPanel**](peninputpanel-class.md) 物件。

這些選項讓應用程式開發人員能在 In-Place 輸入面板出現時，以及在何種狀態中，對其進行細微的控制。 藉由自訂預設的就地狀態，並控制與焦點無關的就地可見度，應用程式開發人員可以在輸入面板回應應用程式設定或使用者輸入至應用程式時，建立自訂工作流程。

## <a name="absolute-positioning-of-input-panel-icon-and-input-panel"></a>輸入面板圖示和輸入面板的絕對位置

[**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)物件中最吸引人的新功能可能是 In-Place 輸入面板的絕對位置。 有了這項新功能，應用程式開發人員可以確保 In-Place 輸入面板不會與應用程式佈建中的一或多個重要視覺元素重迭。 您可以使用 [**PenInputPanel**](peninputpanel-class.md) 物件，根據位移將 In-Place 輸入面板放置在相對於文字欄位的位置，不過，輸入面板仍會自行調整以保持在畫面上。 第一次在 Vista 中，應用程式可以使用螢幕座標，將 In-Place 輸入面板定位於絕對位置。 此外，將輸入面板保持在螢幕上的責任是讓應用程式開發人員更有可能會自動自動重新調整輸入面板的位置。

> [!Note]  
> 只有當輸入面板處於 In-Place 互動模式時，本節中所討論的屬性和方法才適用。

 

絕對位置 In-Place 輸入面板所需的兩個主要方法是 [**SetInPlacePosition**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplaceposition) 和 [**SetInPlaceHoverTargetPosition**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacehovertargetposition)。 第一個用來指定 In-Place 輸入面板的位置，而第二個用來指定 In-Place 輸入面板的輸入面板圖示位置。 如果應用程式選擇只設定輸入面板圖示位置，而不是 In-Place 輸入面板的位置，則 In-Place 的輸入面板會顯示在系統所決定的預設位置。 同樣地，如果應用程式重新置放 In-Place 輸入面板，而不是輸入面板圖示，則輸入面板圖示會出現在預設位置。 位置是以螢幕座標指定。 實際放置的點是輸入面板圖示或輸入面板的左上角，沒有展開的校正合併數十億。 當更正合併數十億展開時，放置的點不會變更。  (請參閱下方的圖 2) In-Place 輸入面板和 In-Place 輸入面板圖示的位置都不會有限制，而呼叫這些方法的應用程式必須負責將它們保留在畫面上。 這兩種方法都是同步的，表示在方法傳回之前會發生位置。 如果已在浮動或停駐互動模式中開啟輸入面板，嘗試放置 In-Place 輸入面板或 In-Place 輸入面板圖示會失敗。 此外，如果附加至 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件的視窗目前沒有焦點，則方法會失敗。

對 [**SetInPlacePosition**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplaceposition) 或 [**SetInPlaceHoverTargetPosition**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacehovertargetposition) 的呼叫不會自動導致 In-Place 輸入面板或輸入面板圖示顯示，它只會在下一次顯示時設定位置。 呼叫 [**SetInPlaceVisibility**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacevisibility) 可以用來強制它們立即顯示。

![就地輸入面板的度量](images/0c67a77a-5d2f-489f-9357-b8a168d024d3.jpg)

在定位 In-Place 輸入面板時，計算是否會關閉畫面可能有點複雜。 為了簡化此程式，您可以使用 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件的數個屬性來簡化此程式。 這些屬性和事件可以搭配使用，以判斷 In-Place 輸入面板在其所有狀態中的確切大小：

-   [**InPlaceBoundingRectangle**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplaceboundingrectangle)–此屬性會在目前輸入語言的最大輸入區域顯示時，提供 In-Place 輸入面板的周框。 如果將書寫板或字元輸入板判斷為最大的輸入區域，則會包含插入按鈕的高度。 它不包含修正合併數十億的高度。當 In-Place 的輸入面板自動成長時 [](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanging)，  /  就會引發 InPlaceSizeChanging [**InPlaceSizeChanged**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanged)事件組，且這個屬性的值會更新為包含額外的寫入區域或書寫線。
-   [**PopUpCorrectionHeight**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_popupcorrectionheight)–此屬性指定在輸入面板上方時，插入後修正合併數十億的高度。 若要取得合併數十億彈出的 [輸入面板] 的完整 In-Place 高度，請將 [**InPlaceBoundingRectangle**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplaceboundingrectangle) 的高度新增至 **PopUpCorrectionHeight**。

以更簡單的方式設定 In-Place 輸入面板和輸入面板圖示的絕對位置，應用程式可以只指定 In-Place 輸入面板是否預設為顯示在文字輸入欄位的上方或下方。 如此一來，就能夠以更鬆散控制的方式，避免應用程式佈建中的元素重迭。 若要這樣做，應用程式會將 [**PreferredInPlaceDirection**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_preferredinplacedirection) 設定為 **InPlaceDirection \_ 底端** 或 **InPlaceDirection \_ Top**。 屬性是喜好設定，因為當必要時，In-Place 輸入面板會覆寫應用程式所設定的喜好設定，以便在螢幕上保持輸入面板。 系統預設值是在可能的情況下將 In-Place 輸入面板放置在文字欄位下方，並在上方放置。 將 **PreferredInPlaceDirection** 設定為 **InPlaceDirection 會 \_ 自動** 還原系統預設值。

[**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)物件的屬性、方法和事件，可讓開發人員對 In-Place 輸入面板進行必要的控制權，以巧妙地在應用程式佈建中放置 In-Place 輸入面板和輸入面板圖示的位置，使其不會中斷配置流程，而在某些情況下可能會顯示整合。 這種新的控制層級是 Tablet 應用程式設計的一大勝利。

## <a name="access-to-the-three-input-panel-areas-writing-pad-character-pad-and-keyboard"></a>存取三個輸入面板區域：書寫板、字元輸入板和鍵盤

輸入面板有三個輸入區域：書寫板、字元輸入板和鍵盤。 使用 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件時，應用程式可以指定輸入面板開啟時顯示給使用者的預設輸入區域。 應用程式的主要原因是要將輸入區域與特定欄位的輸入類型配對。 例如，書寫板最適合用來填滿批註欄位，但在輸入包含數位和字母的產品序號時，鍵盤可能更方便。 為了指定預設的輸入區域，應用程式會將 [**DefaultInputArea**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_defaultinputarea) 屬性設定為 [**PanelInputArea**](/windows/win32/api/peninputpanel/ne-peninputpanel-panelinputarea) 列舉所定義之三個輸入區域的其中一個。 下圖顯示三個輸入區域。

![書寫、字元和鍵盤輸入面板](images/3f1e3d03-88b9-478c-b12d-00d341bc8d5c.jpg)

系統預設輸入區域是英文、法文、德文、西班牙文、義大利文、葡萄牙文、荷蘭文和其他所有拉丁輸入語言的書寫板。 針對東亞輸入語言（包括日文、中文和韓文），預設輸入區域是字元輸入區。 不過，當使用者變更輸入區域時，它會覆寫目前輸入語言的預設輸入區域，並儲存為該輸入語言的新預設值。 鍵盤是密碼欄位的預設輸入區域，不論輸入語言為何，除非使用者或群組原則已停用密碼安全性。 在所有情況下，除非目前欄位是密碼欄位，或目前輸入語言的手寫辨識器不支援以程式設計方式選取的輸入區域，否則設定預設輸入面板區域會以程式設計方式覆寫系統預設值。 將 [**DefaultInputArea**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_defaultinputarea) 屬性設定為 **InPlaceDirection 會 \_ 自動** 還原系統預設設定。

無論預設輸入面板區域是否已設定為以程式設計方式設定，使用者都可以選擇在輸入面板開啟後變更目前的輸入面板區域。 在使用者變更目前的輸入區域之後，使用者選取會持續存在，直到輸入面板關閉或使用者再次變更選取專案為止。 輸入面板關閉並重新開啟之後，以程式設計方式設定預設輸入區域會重新顯示。

由於目前的輸入面板區域可能與預設輸入面板區域不同，因此應用程式可以查詢 [**CurrentInputArea**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentinputarea) 屬性，以判斷目前可見的輸入區域。 如果沒有顯示 [輸入面板]，目前的輸入區域等於預設的輸入區域。 **CurrentInputArea** 屬性絕不會等於 **PanelInputArea \_ Auto**。 如果 [**DefaultInputArea**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_defaultinputarea) 等於 **PanelInputArea \_ Auto**，則 **CurrentInputArea** 等於所顯示的最後一個輸入區域，如果從未顯示輸入面板，則為目前輸入語言的系統預設值。

在 [**PenInputPanel**](peninputpanel-class.md) 物件和 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件的輸入區域支援之間，主要的差異在於，應用程式現在除了書寫板和鍵盤之外，還可以選擇將預設輸入區域設定為字元輸入區。

使用上述屬性，應用程式可以控制不同欄位中所顯示的輸入面板輸入區域，並將使用者的文字輸入經驗優化。 此外，應用程式也可以維持對目前輸入區域的認知，並根據最適合目前使用者工作的輸入區域做出條件式決策。

## <a name="detailed-information-about-input-panels-interaction-mode"></a>輸入面板互動模式的詳細資訊

為了能夠偵測輸入面板的目前輸入區域，您也可以偵測目前的互動模式：就地、停駐或浮動。 應用程式可能必須知道目前的互動模式，才能瞭解使用者如何與應用程式互動，或因為 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件的某些方法和屬性只適用于 In-Place 互動模式。 例如，在應用程式中，會將現有的使用者介面專案重新排列，然後將 In-Place 輸入面板置於其使用者介面中的空白區域，以確定在進行調整之前，目前的互動模式是就地進行的。

![固定、浮動和步調輸入面板模式](images/98c8e96b-99b2-477a-9843-33b1fae7e75b.jpg)

[**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)物件的 [**CurrentInteractionMode**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentinteractionmode)屬性會儲存使用者所選擇的目前互動模式。 可能的模式是由 [**InteractionMode**](/windows/win32/api/peninputpanel/ne-peninputpanel-interactionmode) 列舉定義為：

**InteractionMode \_就地**–在 In-Place 互動模式輸入面板中，會出現在目前具有焦點的文字輸入欄位旁。 依預設，當插入點放在文字輸入欄位時，會顯示 In-Place 輸入面板] 圖示。 點擊輸入面板圖示會導致輸入面板展開。 只有當插入點位於可編輯的欄位時，才會顯示 In-Place 的輸入面板。

InteractionMode \_ 浮動：浮動互動模式類似于「就地互動」模式，但不會系結至插入點。 浮動輸入面板的開啟方式是在 [輸入面板] 索引標籤上，依預設會出現在螢幕的左邊緣。 [浮動輸入面板] 和 [輸入面板] 索引標籤都可以由使用者拖曳和重新置放。 在浮動模式中，輸入面板的位置和控制權會完全留給使用者使用。

InteractionMode \_ DockedTop –在 Docked-Top 互動模式輸入面板會顯示在畫面頂端，而使用中桌面會調整大小，因此輸入面板不會與任何其他視窗或 UI 元素重迭。 在固定模式輸入面板中，無法拖曳或四處移動。

InteractionMode \_ DockedBottom – Docked-Bottom 互動模式與 Docked-Top 模式相同，但輸入面板會顯示在畫面底部。

當輸入面板未顯示時，目前的互動模式是就地的。

發行目前的互動模型是另一種方式， [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件會提供輸入面板狀態的詳細資訊，而不是任何先前版本中的可用資訊。

## <a name="detailed-information-about-input-panels-correction-mode"></a>輸入面板的更正模式的詳細資訊

[輸入面板] 的最後一個部分是 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件提供的詳細資訊，也就是更正模式。 瞭解更正模式可協助應用程式判斷輸入面板的目前大小。 控制應用程式中的插入後修正如何展開，是在應用程式中自訂修正體驗的一種方式。

更正合併數十億可以出現的基本模式有兩種：預先插入和插入後。 預先插入更正合併數十億是用來更正文字，然後再將它插入應用程式。 它是藉由在書寫板中的基準底下顯示的暫止文字來啟動，以做為使用者筆跡。 插入後更正合併數十億是用來修正插入應用程式後的文字。 它是藉由將插入點放入或選取先前插入的文字來啟用。 除了這兩種基本模式之外，也有幾種不同的方式可顯示插入後更正合併數十億。 首先，它可以出現在輸入面板的上方或下方，而第二個則可顯示為折迭或展開。 在折迭狀態中，插入後更正合併數十億只會顯示替代清單。 在展開的狀態中，它同時包含替代項和用來重寫單字的區域。

![更正合併數十億、前置和後置插入輸入面板](images/6cc627de-fc15-4721-9f6a-7e1517d9e650.jpg)

[**CurrentCorrectionMode**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentcorrectionmode)屬性可讓應用程式判斷更正合併數十億的目前設定。這個屬性的可能值如 [**CorrectionMode**](/windows/win32/api/peninputpanel/ne-peninputpanel-correctionmode)列舉所定義： **NotVisible**、 **PreInsertion**、 **PostInsertionCollapsed** 和 **PostInsertionExpanded**。 若未顯示輸入面板或更正合併數十億，則 **CurrentCorrectionMode** 為 **NotVisible**。

根據預設，系統會顯示當您選取可更正的文字，並在插入點放置在可更正的文字中時，所展開的插入後修正合併數十億。 應用程式可以將 [**ExpandPostInsertionCorrection**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_expandpostinsertioncorrection) 屬性設定為 **true**，以指定插入後更正合併數十億應該一律顯示的位置。 系統預設值為 **false**。 當 **ExpandPostInsertionCorrection** 屬性與 [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) 介面搭配使用時，應用程式開發人員可以低廉價格將更正支援新增至不會自動取得的應用程式。

追蹤和控制輸入面板的更正狀態是 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件的許多新功能之一，可讓輸入面板和應用程式整合更緊密。

## <a name="event-notification-before-and-after-the-event-occurs"></a>事件發生前後的事件通知

在 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件中大幅改善的輸入面板可程式性的另一個層面是事件模型。 現在，在變更發生之前和之後，現在不會引發事件以在輸入面板的狀態變更時發出信號變更。 通知事件開始的事件包含目前的時態動詞，例如「變更」或「插入」，而發出事件的事件則會包含過去的時態動詞，例如「已變更」或「插入」。

此事件模型可讓應用程式在發生變更之前或發生變更時對其做出反應。 在所有事件的事件處理常式完成之前，輸入面板會遭到封鎖而無法繼續進行變更或繼續進行變更。 這些事件是同步的，因此應用程式可能會延遲變更，直到完成回應為止。 不過，事件處理常式執行輸入面板的時間會變成無法存取，而且可能會顯示為無回應，因此事件處理常式必須正常執行。 但是，應用程式不可能會阻止或取消事件。 所有事件參數都是唯讀的。 以下是 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件六個事件配對的描述：

-   [**InPlaceStateChanging**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacestatechanging)  / [**InPlaceStateChanged**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacestatechanged)-就地狀態即將離開或已從暫止切換為展開或相反的通知。 參數是新的和舊的就地狀態。 巧合，並變更 [**CurrentInPlaceState**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentinplacestate) 屬性的值。
-   [**InPlaceSizeChanging**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanging)  / [**InPlaceSizeChanged**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanged)–指出 In-Place 的輸入面板大小即將變更或因使用者調整大小、自動成長或輸入區域變更而變更時。 參數是新的和舊的周框。 巧合，並變更 [**InPlaceBoundingRectangle**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplaceboundingrectangle) 屬性的值。
-   [**InputAreaChanging**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inputareachanging)  / [**InputAreaChanged**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inputareachanged)–當輸入面板輸入區域即將變更或已從三個可能的輸入區域（書寫板、字元輸入區或鍵盤）變更為另一個時報告。 參數是新的和舊的輸入區域。 [**CurrentInputArea**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentinputarea)屬性值的變更一致
-   [**CorrectionModeChanging**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-correctionmodechanging)  / [**CorrectionModeChanged**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-correctionmodechanged)–更正模式即將變更或已變更的通知。 可能的更正模式包括：不可見、預先插入、插入後折迭，以及展開後置插入。 參數是新的和舊的更正模式。 會與 [**CurrentCorrectionMode**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentcorrectionmode) 屬性值的變更一致。
-   [**InPlaceVisibilityChanging**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanging)  / [**InPlaceVisibilityChanged**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanged)–指出 In-Place 的輸入面板可見度即將變更或已變更。 參數是新的和舊的可見度。 **False** 的新可見度表示 In-Place 輸入面板未開啟，但不會阻止在浮動或停駐互動模式中看到輸入面板。
-   [**TextInserting**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-textinserting)  / [**TextInserted**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-textinserted)–指出文字即將插入或已從輸入面板插入的時間。 參數是 [**InkDisp**](inkdisp-class.md) 物件的陣列，每個物件都包含用來組成插入的筆墨行和文字。 下一節會詳細說明此事件。

這些事件會為應用程式提供有關輸入面板中變更的重要資訊，並允許它們適當地回應。 同樣地，輸入面板事件模型中的變更代表在應用程式與輸入面板之間進行更佳互動的步驟。

## <a name="support-for-collecting-the-ink-and-text-entered-in-input-panel"></a>支援收集輸入面板中輸入的筆墨和文字

最後一點是， [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 物件中一項非常強大的新功能，就是能夠在文字插入應用程式時，透過輸入面板從輸入面板中取得輸入文字的筆墨物件。 基於變更追蹤和記錄保留的目的，這是經常要求的功能。 它也可讓應用程式以靜態元素或自訂的筆墨介面，在其 UI 中使用筆墨。

為了接收透過 [輸入面板] 輸入之文字的 [**InkDisp**](inkdisp-class.md)物件，應用程式必須註冊，才能接收 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)物件所產生的 [**TextInserting**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-textinserting)或 [**TextInserted**](/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-textinserted)事件。 **TextInserting** 事件會在文字從輸入面板插入應用程式之前立即引發，而且在所有事件處理常式完成之前，不會插入文字。 **TextInserted** 事件會在插入測試之後立即引發。 **TextInserting** 和 **TextInserted** 事件的唯一參數是 **InkDisp** 物件的陣列，其中包含從輸入面板插入的每一行文字的一個 **InkDisp** 物件。 注意：當事件處理常式正在執行時，輸入面板處於非使用中狀態，而且可能會對使用者顯示為無回應，因此請務必讓這些事件處理常式變得輕量，並確保它們能快速執行。 此外，應用程式不應該建立此事件的處理常式，除非它有特定的資訊用途，因為這樣做會有相關聯的效能成本。 輸入面板只會在有應用程式要求資料時封送處理筆墨資料，否則輸入面板可以略過這項昂貴的作業。 **TextInserting** 和 **TextInserted** 事件的參數都是唯讀的，這表示應用程式在插入應用程式之前，不可能變更插入的文字。

應用程式可以使用這種新功能執行的可能性很廣泛，而且使用起來可能不容易。 藉由應用程式收集透過輸入面板所輸入的已辨識文字和筆墨，就是在 Windows Vista 中改善輸入面板開發人員故事的另一種方式。

## <a name="conclusion"></a>結論

整體來說，[Tablet PC 輸入面板] 的可程式性案例在 Windows Vista 中引進 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)物件，大幅改進。 藉由使用 **TextInputPanel** 物件，應用程式開發人員可以更充分掌控舊版中狀態輸入面板的控制權和詳細資訊。 因此，強烈建議應用程式開發人員建立新的 Tablet PC 應用程式或更新現有的應用程式，以使用 **TextInputPanel** 物件，而不是現在已被取代的 [**PenInputPanel**](peninputpanel-class.md) 物件。 此外，支援新功能（例如輸入面板的絕對位置和輸入面板圖示），以及應用程式透過 [輸入面板] 同時接收辨識器文字和筆墨的功能，可啟用新的應用程式功能和案例。 包含這些功能和其他幾項功能，可直接回應開發人員的意見反應，並標示將輸入面板與 Tablet PC 應用程式完全整合的第一步。 最後，擴充 Tablet PC 應用程式功能對應用程式開發人員和 Tablet PC 平臺而言都是一大勝利。

 

 



