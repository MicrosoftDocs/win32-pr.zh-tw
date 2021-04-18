---
title: '動畫 (DirectComposition) '
description: 本主題討論 Microsoft DirectComposition 動畫的基本概念。
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7462a10fd83b45c1b90450fdde806ef306a2f6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965461"
---
# <a name="animation-directcomposition"></a>動畫 (DirectComposition) 

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題討論 Microsoft DirectComposition 動畫的基本概念。 它包含下列主題：

-   [什麼是動畫？](#what-is-an-animation)
-   [可以動畫顯示的屬性](#properties-that-can-be-animated)
-   [動畫函數](#animation-functions)
-   [動畫區段](#animation-segments)
    -   [三次區段](#cubic-segment)
    -   [正弦曲線區段](#sinusoidal-segment)
    -   [重複區段](#repeat-segment)
    -   [結束區段](#end-segment)
-   [與 Windows 動畫管理員的相容性](#compatibility-with-windows-animation-manager)
-   [相關主題](#related-topics)

## <a name="what-is-an-animation"></a>什麼是動畫？

*動畫* 是在每次變更之後，于一段時間內快速進行視覺效果的累加式變更時，所建立的光學假像。 由於重新繪製的速度很快，因此大腦會將累加的變更視為單一變更場景，就像在影片或實況活動影片中一樣。

下表說明一些使用動畫的典型方式。

| 動畫                 | Description                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 捲動                 | 使用動畫將功能（例如物理模擬動力）新增至滾動清單控制項。                                                                                                                                                           |
| 場景轉換         | 使用動畫來建立導覽場景轉換，以提供工作流程中工作之間的持續性。 導覽場景轉換會提供內容，顯示使用者的位置、位置，以及接下來需要前往的位置。 |
| 跨視窗互動 | 將不同應用程式的 UI 專案以動畫顯示，讓他們能夠理解它們之間的無縫持續性，以協助使用者完成工作，包括從某個應用程式切換到另一個應用程式。                                         |



 

## <a name="properties-that-can-be-animated"></a>可以動畫顯示的屬性

在 DirectComposition 中，您會將動畫套用至定義視覺效果之物件的個別屬性，以建立視覺效果的動畫。 例如，如果您想要在螢幕上水準移動視覺效果，則會將動畫套用至視覺效果的 OffsetX 屬性。 同樣地，如果您想要對視覺效果進行簡單的動畫2D 旋轉，則會將動畫套用至2D 轉換物件的 Angle 屬性，然後將2D 轉換物件套用至視覺效果的轉換屬性。

DirectComposition 可讓您將動畫套用至任何接受純量值的物件屬性。 您可以同時將動畫套用至多個屬性和多個物件。

DirectComposition 會在個別的執行緒上執行動畫。 您可以啟動一組動畫或一組動畫，然後對應用程式執行緒執行其他工作，甚至讓執行緒進入睡眠狀態，而組合引擎會以適當的畫面播放速率執行動畫。

## <a name="animation-functions"></a>動畫函數

DirectComposition 會根據您定義的動畫函式，將物件屬性動畫。 *動畫* 函式是一種結構，可指定物件屬性值在一段時間內的變更方式。 例如，您可以定義一個動畫函式，在4秒的過程中，將屬性的值從1變更為360。 然後，如果您將動畫函式套用至2D 旋轉轉換物件的 Angle 屬性，然後將轉換物件套用至視覺效果的轉換屬性，則動畫函式會在4秒的過程中，以完整的圓形旋轉視覺效果。

動畫函式是由呼叫 [**IDCompositionDevice：： CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation)方法所建立的 *動畫物件* 來表示。 您可以使用動畫物件之 [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) 介面的方法，將 *動畫區段*（一次一個）附加至定義動畫函數的陣列，以建立動畫函式。 附加區段時，您會指定以零為基底的位移，此位移會標示區段的開始時間，相對於動畫函式的開頭。 動畫區段必須以開始時間的遞增順序附加。 嘗試附加開始時間早于或等於前一個區段的動畫區段將會失敗。 動畫函式可以有指定的結束時間，表示函式應該結束的時間。

除非另有指定，否則當桌面視窗管理員 (DWM) 接收命令以執行動畫時，就會啟動動畫函式。 每個區段都會執行，直到達到下一個區段的開始時間為止。 在區段之間的動畫屬性值中發生的任何不連續變更，都會視為離散變更。

您可以將動畫函式套用至屬性，方法是將屬性值設定為代表動畫函式的動畫物件的 [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) 指標。 相同的動畫物件可以套用至相同物件的多個屬性，也可以套用至相同裝置所建立之其他物件的屬性。

## <a name="animation-segments"></a>動畫區段

動畫區段是動畫函數的基本計時定義;它們是建立更複雜和更高層級動畫函式的基本類型。 動畫區段是由一系列的參數所構成，這些參數描述函式和區段開始的時間（相對於動畫函式的開頭）。 針對每個區段，時間 (*t*) 沿著水準軸進行，並從 *t* = 0 開始。

### <a name="cubic-segment"></a>三次區段

三次區段的時間是由三個多項式所定義。 針對指定的時間輸入 (*t*) ，輸出值會由下列方程式提供：

*x* (*t*) = *at*³ + *bt*² + *ct*  +  *d*

下圖顯示包含兩個三個三個區段的動畫函數。 第一個區段會將值從0轉換為16秒，而第二個區段則會在接下來4秒將值從16變更為0。 第一個轉換會沿著這個三個多項式發生：

*x* (*t*) = *t*³-6 *t*² + 12 *t*

第二個轉換會在此執行：

*x* (*t*) =-4 *t* + 16

![有兩個三個三個區段的動畫函式圖表](images/cubicsegment.png)

您可以使用 [**IDCompositionAnimation：： AddCubic**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic) 方法，將三個區段加入至動畫函數。

### <a name="sinusoidal-segment"></a>正弦曲線區段

正弦曲線區段的時間是由下列方程式所定義：

*x* (*t*) =*偏差*  +  *幅度* \* sin (*t* \* *頻率* \* 2 \* PI +*階段* \* PI/180.0) 

您可以使用 [**IDCompositionAnimation：： AddSinusoidal**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal) 方法，將正弦曲線區段新增至動畫函數。

### <a name="repeat-segment"></a>重複區段

重複區段會重複動畫函式的先前指定部分。 重複區段會導致動畫函式的指定部分無限期地迴圈，直到遇到下一個區段或到達動畫的指定結束為止。 動畫先前的部分是由其他區段組成，包括其他重複區段。 重複區段無法用作動畫函式中的第一個區段。

下圖顯示的動畫函式包含四個三秒期間的三個三區段，後面接著重複的區段，持續12秒。 重複區段會在動畫中開始8秒，並重複兩次動畫的前6秒，直到到達結束區段20秒為止。

![包含兩個三個三個區段和一個重複區段的動畫函式圖表](images/repeatsegment.png)

若要將重複區段加入至動畫函式，請使用 [**IDCompositionAnimation：： AddRepeat**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat) 方法。

### <a name="end-segment"></a>結束區段

從區段中建立動畫函式之後，您可以附加結束區段，讓動畫函式在特定時間結束。 如果您未附加結束區段，則動畫函式的最後一個區段會無限期執行。

您可以藉由呼叫 [**IDCompositionAnimation：： end**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) 方法，指定從動畫函式的開頭算起的位移（表示函式的結束點），以附加結束區段。 位移必須大於前一個區段的開始位移。 此外，結束區段無法當做動畫函式中的第一個基本函數使用。

當您呼叫 [**End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end)時，也會針對要製作動畫的屬性指定最後一個值。 當到達動畫函式的結束點時，屬性會設定為指定的最後一個值。

附加結束區段之後，您就無法將任何其他區段附加至動畫函數。 也就是說，除了 [**IDCompositionAnimation：： Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset)之外，在動畫物件上的所有方法呼叫都會失敗。 呼叫 **Reset** 會傳回動畫物件以清除狀態，其中動畫函式不包含任何區段，此時您可以再次加入區段。

## <a name="compatibility-with-windows-animation-manager"></a>與 Windows 動畫管理員的相容性

Windows 動畫管理員 (Windows 動畫) 以與 DirectComposition API 相容的格式輸出動畫基本專案。 這表示 DirectComposition 可以根據 Windows 動畫建立的動畫基本專案來建立動畫。

如需詳細資訊，請參閱 [Windows 動畫管理員](/windows/desktop/UIAnimation/-main-portal)、 [**IUIAnimationVariable2：： GetCurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) 方法，以及 [使用 Windows 動畫管理員 v2 管理 DirectComposition 動畫](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectComposition 概念](directcomposition-concepts.md)
</dt> </dl>

 

 
