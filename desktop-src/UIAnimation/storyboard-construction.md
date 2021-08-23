---
title: 分鏡腳本總覽
description: 本總覽著重在 Windows 動畫中如何使用轉換和分鏡腳本。
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Windows動畫 Windows 動畫、分鏡腳本總覽
- 分鏡腳本 Windows 動畫，說明
- Windows 動畫的轉換，描述
- 轉換 Windows 動畫，自訂
- interpolators Windows 動畫，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca78e4638ad7c3930be25b9ff826e5fa533d2af62cc4907b7a17d4c5b636f239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514090"
---
# <a name="storyboard-overview"></a>分鏡腳本總覽

本總覽著重在 Windows 動畫中如何使用轉換和分鏡腳本。 如需 Windows 動畫元件的總覽，請參閱[Windows 動畫總覽](scenic-animation-api-overview.md)。

本主題包含下列幾節：

-   [轉換](#custom-transitions)
    -   [轉換程式庫](#transition-library)
    -   [自訂轉換](#custom-transitions)
-   [Storyboard](#storyboards)
    -   [建立簡單的分鏡腳本](#building-a-simple-storyboard)
    -   [使用 Context-Sensitive 持續時間](#using-a-context-sensitive-duration)
    -   [建立更複雜的分鏡腳本](#building-a-more-complex-storyboard)
    -   [使用主要畫面格](#using-keyframes)
    -   [保留變數](#holding-variables)
    -   [排程分鏡腳本](#scheduling-a-storyboard)
-   [相關主題](#related-topics)

## <a name="transitions"></a>轉換

轉換會定義單一動畫變數在特定時間間隔內的變更方式。 Windows動畫包含一般轉換的程式庫，可讓開發人員將其套用至一或多個動畫變數。 不同類型的轉換具有不同的參數集，這些參數可能會在轉換完成時包括變數的值、轉換的持續時間，或是基礎數學函數的唯一數量（例如加速或震盪的範圍）。

所有轉換都會共用兩個隱含參數：數學函式的初始值和初始速度 (斜率) 。 這些可以由應用程式明確指定，但通常會在轉換開始時，由動畫管理員設定為動畫變數的值和速度。

-   [轉換程式庫](#transition-library)
-   [自訂轉換](#custom-transitions)

### <a name="transition-library"></a>轉換程式庫

轉換程式庫目前提供下列轉換。 如果應用程式需要無法使用轉換程式庫指定的效果，開發人員可以藉由為應用程式執行自訂插即用，或使用協力廠商的轉換程式庫，來建立其他類型的轉換。



| 轉換名稱                        | 描述                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 加速-減速<br/>       | 動畫變數會加速，並在指定的期間內減緩。<br/>                                                                                                               |
| 常數<br/>                    | 動畫變數會在整個轉換期間維持其初始值。<br/>                                                                                                            |
| 三次方<br/>                       | 動畫變數在指定的持續期間內，會以指定的最終速度，從其初始值變更為指定的最後一個值。<br/>                                                 |
| 離散<br/>                    | 動畫變數在指定的延遲時間仍維持其初始值，然後立即切換到指定的最終值，並針對指定的保留時間維持在該值的值。<br/> |
| 暫態<br/>               | 動畫變數會立即從其目前的值變更為指定的最後一個值。<br/>                                                                                               |
| linear<br/>                      | 動畫變數會在指定的持續期間，以線性方式從其初始值轉換為指定的最終值。<br/>                                                                      |
| 線性的速度<br/>           | 動畫變數會從其初始值以線性方式轉換為指定的最終值（具有指定的速度）。<br/>                                                                     |
| 從加速拋物線<br/> | 動畫變數會從其初始值轉換為指定的最後一個值，並使用指定的加速來變更其速度。<br/>               |
| 逆轉<br/>                    | 變數會在指定的期間內變更方向。 最後一個值將會與初始值相同，最後的速度將會是初始速度的負數值。<br/>          |
| 從範圍正弦曲線<br/>       | 在指定的期間內，oscillates 指定的值範圍內的變數（具有指定的震盪期間）。<br/>                                                                     |
| 從速度正弦曲線<br/>    | 在指定的期間內，變數 oscillates 具有指定的震盪期間。 震盪的波幅取決於變數的初始速度。<br/>                      |
| 順利停止<br/>                 | 動畫變數在時間的最長持續時間內，會在指定的最終值上變成平滑停止。<br/>                                                                              |



 

下表包含每個轉換的圖例。



|    插圖                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![瞬間轉換的圖例](images/instantaneoustransition.png)  ![常數轉換的圖例](images/constanttransition.png)  ![線性轉換的圖例](images/lineartransition.png)  ![從速度 lineat 轉換的圖例](images/lineartransitionfromspeed.png)  ![離散轉換的圖例](images/discretetransition.png) |
| ![從加速拋物線轉換的圖例](images/parabolictransitionfromacceleration.png)  ![三次轉換的圖例](images/cubictransition.png)  ![平滑停止轉換的圖例](images/smoothstoptransition.png)                                                                                                                                       |
| ![反轉轉換的圖例](images/reversaltransition.png)  ![從速度正弦曲線轉換的圖例](images/sinusolidaltransitionfromvelocity.png)  ![從範圍正弦曲線轉換的圖例](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![accellerate 和減速轉換的圖例](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a>自訂轉換

*插* 即用會定義數學函式，以決定動畫變數在從其初始值移至最後一個值時，如何隨著時間變更。 轉換程式庫中的每個轉換都有一個相關聯的插隨插即用，該物件是由系統所提供並會執行插即插 如果應用程式需要無法使用轉換程式庫指定的效果，則可以藉由針對每個新轉換來執行插即用物件，來執行一或多個自訂轉換。 插即用物件不能直接用於應用程式，而必須改為包裝在相關聯的轉換中。 *轉換 factory* 用來從插即用物件產生轉換。 如需詳細資訊，請參閱 [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) 和 [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory) 。

請注意，大部分的應用程式都有使用轉換程式庫所需的所有轉換，因此不需要執行插即用。

## <a name="storyboards"></a>Storyboard

分鏡腳本是一組隨時間套用至一或多個動畫變數的轉換集合。 分鏡腳本中的轉換保證會彼此保持同步，而且分鏡腳本已排程或取消為一個單位。 建立所需的轉換之後，應用程式會使用動畫管理員來建立分鏡腳本、將轉換新增至腳本、適當地設定分鏡腳本，並將它排程為盡可能播放。 動畫管理員會決定分鏡腳本的實際開始時間，因為可能會有與其他分鏡腳本的競爭，且目前會以動畫顯示相同的變數。

分鏡腳本的整體持續時間取決於分鏡腳本內轉換的持續時間。 轉換的持續時間不需要固定;轉換開始時，可以由動畫變數的值和速度來決定。 因此，分鏡腳本的持續時間也可能取決於其動畫的變數狀態。

下列範例假設已建立動畫管理員、轉換程式庫和計時器。 如需詳細資訊，請參閱 [建立主要動畫物件](adding-animation-to-an-application.md)。 範例也假設應用程式已使用 [**IUIAnimationManager：： CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) 方法建立三個動畫變數 (X、Y 和 Z) ，而五個轉換 (T1、T2、T3、T4 和 T5) 使用 [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary) 介面的其中一個方法。

-   [建立簡單的分鏡腳本](#building-a-simple-storyboard)
-   [使用 Context-Sensitive 持續時間](#using-a-context-sensitive-duration)
-   [建立更複雜的分鏡腳本](#building-a-more-complex-storyboard)
-   [使用主要畫面格](#using-keyframes)
-   [保留變數](#holding-variables)
-   [排程分鏡腳本](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a>建立簡單的分鏡腳本

若要建立簡單的分鏡腳本，請使用 [**IUIAnimationManager：： CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) 方法來建立新的分鏡腳本、 [**IUIAnimationTransitionLibrary：： CreateLinearTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) 方法來建立線性轉換、T1 和 [**IUIAnimationStoryboard：： AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) 方法，以將 T1 轉換套用至變數 X，並將產生的轉換加入至腳本。

此程式會產生簡單的分鏡腳本，如下圖所示。 分鏡腳本包含一個轉換 T1，讓變數 X 的值在固定的時間內以線性方式變更。

![顯示簡單分鏡腳本有固定持續時間的圖例](images/simplestoryboardfixedduration.png)

請注意，在這種簡單的案例中，替代選項是使用 [**IUIAnimationManager：： ScheduleTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition) 方法。

### <a name="using-a-context-sensitive-duration"></a>使用 Context-Sensitive 持續時間

雖然某些轉換有固定的持續時間，但其他的持續時間取決於轉換開始時的動畫變數初始值或速度。 例如， [**IUIAnimationTransitionLibrary：： CreateLinearTransitionFromSpeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) 方法會建立一個持續期間的轉換，與動畫變數的初始值和指定的最後一個值之間的差異成正比。 在此圖中，和其餘的圖例（具有任意持續時間的轉換）會顯示一個問號 (？ ) ，而且實際的持續時間會在腳本播放時決定。

![圖例顯示具有未知持續時間的簡單分鏡腳本](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a>建立更複雜的分鏡腳本

建立分鏡腳本並加入單一轉換 T1 之後，您可以再次呼叫 [**IUIAnimationStoryboard：： AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) 方法，但使用 T2 而不是 T1，來附加 X 變數的第二個轉換。

假設 T2 轉換具有內容相關的持續時間，則腳本現在會包含影響變數 X 之任意持續時間的兩個反向轉換。

![顯示分鏡腳本的圖例，其中包含兩個在相同變數上的轉換](images/appendingwithaddtransition.png)

使用變數 Y 和轉換 T3 再次呼叫 [**AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) ，會在腳本的開頭新增第三個轉換。 根據在腳本播放時的 X 和 Y 值，T3 可能會在 T1 之後結束，甚至在 T2 之後結束。

![顯示分鏡腳本包含跨多個變數之轉換的圖例](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a>使用主要畫面格

若要在腳本開頭的位移加入轉換，您必須先新增主要畫面格。 主要畫面格代表時刻的時間，而且本身不會影響分鏡腳本的行為。 每個分鏡腳本都有一個隱含的主要畫面格，代表腳本的開頭、Ui 動畫主要畫面格 [**\_ \_ \_ \_ 開始**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85)); 您可以透過呼叫 [**IUIAnimationStoryboard：： AddKeyframeAtOffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) 方法與 UI 動畫主要畫面格 **\_ \_ \_ \_ 開始**，從一開始的位移加入新的主要畫面格。

您新增主要畫面格的位移一律相對於另一個主要畫面格。 下圖顯示加入 keyframe1 和轉換 T4 的結果，此結果會套用至變數 Z、與 keyframe1 對齊，並以固定期間建立。 當然，因為其他轉換的持續時間尚未得知，所以 T4 可能不是最後一個轉換完成。

![圖例顯示在主要畫面格對齊的轉換](images/addtransitionatkeyframe.png)

您也可以使用 [**IUIAnimationStoryboard：： AddKeyframeAfterTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) 方法，將主要畫面格放在轉換的結尾。 下圖顯示在 T2 之後新增 keyframe2 的結果，以及 T2 之後的 keyframe3。

![此圖顯示各種轉換之後的主要畫面格加法](images/addkeyframeaftertransition.png)

由於在分鏡腳本播放之前，T1 和 T2 的持續時間是未知的，因此在那之前，keyframe2 和 keyframe3 的位移也不會決定。 因此，keyframe2 甚至 keyframe3 可能會在 keyframe1 之前發生。

轉換的開始和結束都可以使用 [**IUIAnimationStoryboard：： AddTransitionBetweenKeyframes**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) 方法來與主要畫面格對齊。 下圖顯示在變數 Y 上新增第五個轉換（T5）在 keyframe2 和 keyframe3 之間的結果。 這會改變 T5 的持續時間，取決於 keyframe2 和 keyframe3 的相對位移，使其更長或更短。

![顯示在主要畫面格之間轉換 additon 的圖例](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a>保留變數

如果 T4 在 T2 和 T5 之後結束，腳本會停止將變數 X 和 Y 建立動畫，讓其他分鏡腳本能以動畫顯示。 不過，應用程式可以呼叫 [**IUIAnimationStoryboard：： HoldVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) 方法，要求腳本在腳本完成之前，保留其最終值的部分或所有變數。 下圖顯示 T4 最後完成時，保留 X 和 Z 的結果。 請注意，分鏡腳本會在腳本完成之前，保留其最終值的 X。 此保留對 Z 沒有任何作用，因為在 T4 完成時，腳本會結束。

![圖例顯示在完成腳本完成之前將變數保留在最後的值](images/holdvariable.png)

雖然此腳本未持有 Y，但在 T5 完成之後，其值不會變更，除非有另一個分鏡腳本的動畫。 因為沒有保留 Y，所以任何其他分鏡腳本（不論優先權為何）都可以在 T5 完成之後建立 Y 的動畫。 相反地，因為會保留 X，所以較低優先順序的分鏡腳本無法在此腳本完成之前建立 X 的動畫。

當分鏡腳本開始播放時，所有這些圖例都會假設變數有任意一組目前的值。 如果遇到其他值，內容相關轉換的持續時間可能會不同，如下圖所示。

![圖例顯示變更上圖所使用之初始條件的結果](images/holdvariablez.png)

在此案例中，T5 會在 T3 完成之前開始，T3 則會被修剪。 因為 T4 的完成時間早于 T2 和 T5，所以 Z 的值會保留到腳本的結尾。 一般來說，當腳本開始播放時，變數的值和速度可能會影響主要畫面格的順序以及分鏡腳本的整體長度和圖形。

### <a name="scheduling-a-storyboard"></a>排程分鏡腳本

排程分鏡腳本時，其開始時間是由其外框和目前在排程中的分鏡腳本大綱所決定。 具體而言，當分鏡腳本繪製每個個別變數的第一個和最後一點時，會決定兩個分鏡腳本是否會發生衝突，但內轉換的內部詳細資料並不重要。

下圖顯示分鏡腳本的大綱，其中有五個轉換以動畫顯示三個變數。

![顯示分鏡腳本的圖，其中有五個轉換動畫三個變數](images/storyboardwithoutline.png)

Windows 動畫平臺的基石是支援在需要時，讓一個動畫先完成，再開始進行。 雖然這可排除許多邏輯問題，但它也會在 UI 中引進任意延遲。 若要解決此情況，應用程式可以使用 [**IUIAnimationStoryboard：： SetLongestAcceptableDelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay)方法指定可接受的分鏡腳本 *最長延遲* 時間，而動畫管理員會使用此資訊，在經過指定的延遲期間之前，排程腳本。 當您排定分鏡腳本時，動畫管理員會決定是否必須先取消、修剪、結束和/或壓縮其他的分鏡腳本。

應用程式可以註冊一個處理常式，當腳本的狀態變更時，就會呼叫此處理程式。 這可讓應用程式在分鏡腳本開始播放、執行完成、完全從排程中移除，或防止因較高優先順序的腳本中斷而無法完成時回應。 若要識別傳遞給分鏡腳本事件處理常式 (或優先順序比較) 的分鏡腳本，應用程式可以使用 [**IUIAnimationStoryboard：： SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) 方法，將標記套用至分鏡腳本，類似于可用來識別變數的範例。 如同使用分鏡腳本重複使用，開發人員在使用標記來識別分鏡腳本時必須特別小心，並確定當使用者動作導致許多分鏡腳本排入佇列時，不會發生多義性。

下列範例會示範兩種嘗試排程在本主題先前章節中所建立之分鏡腳本的變化。

在此案例中，已排程6個分鏡腳本（A 到 F），以建立變數 W、X、Y 和 Z 的動畫，但只有 A 和 B 已開始播放。 標示為 G 的新分鏡腳本，可接受的最長延遲設定為下圖所示的持續時間。

![顯示將新的腳本新增至現有排程的圖例](images/existingschedule1withlines.png)

應用程式已註冊優先順序比較，包括下列邏輯：

-   G 只能取消 C 和 E，而且只可以防止失敗。
-   G 只能修剪 A、C、E 和 F，而只會避免失敗。
-   任何分鏡腳本都可以壓縮任何其他分鏡腳本 (壓縮一律是為了避免) 失敗。

> [!Note]  
> 「僅為了防止失敗」的辨識符號表示 \_ 只有當 *priorityEffect* 參數是 **UI \_ 動畫 \_ 優先權 \_ 效果 \_ 失敗** 時，註冊的優先順序比較才會傳回 S OK。 如需詳細資料，請參閱 [**IUIAnimationPriorityComparison：： HasPriority**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority) 方法。

 

若要在經過最長可接受的延遲之前開始，動畫管理員必須執行下列動作：

-   修剪 F
-   取消 E

當 E 取消時，會發現 D 和 F，並還原為其原始大綱：

![顯示原始大綱的圖例](images/existingschedule1bwithlines.png)

動畫管理員不需要先取消或修剪 C，就能在其可接受的延遲時間最長之前進行排程，因此 C 和 G 的會議會決定 G 的開始時間。

![圖例顯示已修剪 f 以允許 c 和 g 符合](images/schedule1withgwithlines.png)

成功排程 G 之後，可以判斷其轉換的持續時間，並因此其外框的其餘部分是已知的。 但是，如果後續已從排程中移除另一個腳本，則大綱可能會變更。

作為第二個範例，請考慮上述案例，但以較短的最長可接受延遲指定給 G。

![顯示上一個案例的圖例，以較短的最長可接受延遲為 g](images/existingschedule2withlines.png)

在此情況下，會採取下列動作：

-   修剪 F
-   取消 E
-   取消 C

此外，動畫管理員必須以顯示的數量來壓縮 D，讓 G 在可接受的最長延遲時間後啟動，而不會在稍後進行。

![圖例顯示 d 必須壓縮以讓 g 以最長可接受的延遲啟動](images/trimmedandcancelledwithlines.png)

為了保留其相對時間，A、B 和 F 也會進行壓縮。

![顯示 a、b、d 和 f 壓縮的圖例](images/schedule2withgwithlines.png)

不過，不相關變數 (的分鏡腳本不會顯示) 不會被壓縮。

同樣地，G 的大綱現在是已知的，與第一個案例中的結果不同，因為當 G 開始時，變數會有不同的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationPriorityComparison**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)
</dt> <dt>

[**IUIAnimationStoryboard**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> </dl>

 

