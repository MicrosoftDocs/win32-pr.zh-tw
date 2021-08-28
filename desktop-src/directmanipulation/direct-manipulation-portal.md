---
description: 直接操作 Api 可讓您建立絕佳的平移、縮放和拖曳使用者體驗。 若要這樣做，它會在區域或物件上處理觸控輸入、產生輸出轉換，然後將轉換套用至 UI 元素。
ms.assetid: 26358bc5-71e9-40f0-9243-9bddd961a0e5
title: 直接操作
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f449079a1772fd6dd43b51a2e5af3920ab3e173e1dc8590567ed4555b6deaf31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022581"
---
# <a name="direct-manipulation"></a>直接操作

直接操作 Api 可讓您建立絕佳的平移、縮放和拖曳使用者體驗。 若要這樣做，它會在區域或物件上處理觸控輸入、產生輸出轉換，然後將轉換套用至 UI 元素。 您可以使用直接操作，透過執行緒輸入處理、選擇性的非執行緒輸入點擊測試，以及輸入/輸出預測，來將回應優化並降低延遲。

任何使用直接操作來處理觸控互動的應用程式，都會顯示符合[一般使用者互動方針](/windows/uwp/design/input/)的流暢 Windows 8 動畫與互動意見反應行為。

## <a name="developer-audience"></a>開發人員讀者

直接操作 API 適用于熟悉 C/c + + 的有經驗的開發人員，對於[元件物件模型 (的 COM) ](../com/component-object-model--com--portal.md)有充分的瞭解，並熟悉 Windows 程式設計概念。

## <a name="run-time-requirements"></a>執行階段需求求

直接操作是在 Windows 8 引進。 它包含在32位和64位版本中。

## <a name="why-use-directmanipulation"></a>為何要使用 DirectManipulation

### <a name="handles-interactions-in-a-straightforward-and-consistent-manner"></a>以簡單且一致的方式處理互動

直接操作的運作方式是預先宣告區域或物件的行為和互動。 例如，網頁通常會設定為平移和縮放。 在執行時間，輸入會透過簡單的 API 呼叫，與此區域/物件產生關聯。 從這個點開始，向前操作會執行所有處理輸入、套用條件約束和特性，以及產生輸出轉換的繁重工作。

### <a name="build-responsive-touch-applications"></a>打造回應式觸控應用程式

為了將回應優化並將延遲降到最低，直接操作處理會在與 UI 執行緒不同的獨立執行緒上進行。 因此，輸出轉換可以平行執行至 UI 執行緒上的活動。 UI 執行緒活動可能包含應用程式邏輯、轉譯、配置，以及在處理器上使用迴圈的任何其他作業。

### <a name="implementation-flexibility"></a>實作為彈性

直接操作包含的介面可提供輸入處理、互動辨識、意見反應通知和 UI 更新的完整支援。 這些介面也會納入系統服務（例如 [DirectComposition](../directcomp/directcomposition-portal.md)）。

## <a name="basic-concepts"></a>基本概念

最基本的直接操作實行包含一個 *區*、 *內容* 和 *互動*。 此 *區* 是能夠接收和處理使用者互動輸入的區域。 它也是使用者可以看見的內容區域。 *內容* 是使用者可以看到的實際物件，也是移動或調整以回應使用者互動的物件。 主要使用者 *互動* (也稱為 *操作* ，) 直接操作所支援的移動和縮放。 這些互動會分別將轉譯或調整轉換套用至各區中的內容。 您可以在單一視窗中設定多個可 (多個不同) 的範圍，以建立豐富的 UI 體驗。

下圖顯示移動前和之後的基本直接操作實行。

![移動前和之後的基本直接操作實行。](images/dm-art-1.png)

在直接操作的初始化期間，會具現化 **DCompDirectManipulationCompositor** 物件，並且與直接操作相關聯。 此物件是 [DirectComposition](../directcomp/directcomposition-portal.md)的包裝函式，也就是系統組合器。 物件負責套用輸出轉換和驅動視覺效果更新。

連絡人代表在 [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md)訊息中提供的 **pointerId** 所識別的觸控點。 當收到 **WM \_ POINTERDOWN** 訊息時，應用程式會呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)。 應用程式會通知直接 Manipulationabout 應該處理的連絡人，以及應該對這些連絡人進行回應的 () 的區。 鍵盤和滑鼠輸入具有特殊的 **pointerId** 值，因此可以透過直接操作來適當地處理。

在上述的基本案例中，當呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) 時，會發生幾件事：

- 當使用者執行平移時，會將 [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) 訊息傳送至應用程式，以通知連絡人已被直接操作取用。
- 當使用者移動移動時，此區會引發 [DirectComposition](../directcomp/directcomposition-portal.md) 包裝函式所使用的更新事件，以驅動視覺效果更新至螢幕。 若要在使用者移動區中移動，內容會顯示在連絡人下順暢地移動。
- 當使用者將連絡人貼上時，使用者會看到內容在轉換成慣性動畫時繼續移動，並逐漸減速到到達最後的放置位置為止。

## <a name="processing-keyboard-and-mouse-input"></a>處理鍵盤和滑鼠輸入

直接操作可讓您透過 [**ProcessInput**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-processinput) API，從應用程式 UI 執行緒手動轉送鍵盤和滑鼠訊息，讓直接操作能夠適當地處理。

## <a name="directmanipulation-and-the-hwnd"></a>DirectManipulation 和 HWND

直接操作與 Win32 HWND 相關聯，以便接收和處理該視窗的指標輸入訊息。 當直接操作計算輸出值時，它會對直接操作元件物件模型進行非同步回呼， [ (COM) ](../com/component-object-model--com--portal.md) 在應用程式中執行的物件。 這些回呼會通知應用程式有關已套用至物件的轉換。 藉由呼叫 [**Activate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-activate)，在指定的 HWND 上啟用直接操作。

## <a name="supporting-documentation"></a>支援檔

- [區和內容](directmanipulation-viewports-and-content.md)
- [在 DirectManipulation 中使用多個區](directmanipulation-multiple-vieports.md)
- [使用 DirectManipulation 處理輸入](directmanipulation-processing-input-with-directmanipulation.md)
- [撰寫引擎](directmanipulation-composition-engine.md)
- [直接操作參考](direct-manipulation-reference.md)

- [組建2013： WCL-022：使用觸控、滑鼠和畫筆讓您的桌面應用程式發揮絕佳](https://channel9.msdn.com/Events/Build/2013/4-022)
- [使用直接操作範例處理觸控輸入](https://github.com/microsoft/Windows-classic-samples/tree/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/TouchInputDirectManipulation)
