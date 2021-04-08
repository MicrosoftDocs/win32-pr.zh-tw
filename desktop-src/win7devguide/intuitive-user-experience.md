---
title: 直覺的使用者體驗
description: 第一次，Windows 7 可讓開發人員和使用者透過觸及畫面來控制他們的電腦。
ms.assetid: cf5be4d6-4284-43e3-86ba-293c4513b477
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76576883186a77c53256dad7f011b75a7e260ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682902"
---
# <a name="intuitive-user-experience"></a>直覺的使用者體驗

第一次，Windows 7 可讓開發人員和使用者透過觸及畫面來控制他們的電腦。 觸控和多點觸控功能可提供自然且直覺的方式，讓使用者與電腦互動。 開發人員平臺包含高階手勢 Api，以及低層級的觸控訊息和觸控輸入 Api。 最上層的 UI 專案（例如 [ *開始* ] 功能表和 *工作列*）有比舊版 Windows 更大的目標，讓您更輕鬆地選取手指而非滑鼠。 視覺效果的意見反應是為了點一下和點一下。 Windows 檔案總管和 Windows Internet Explorer 8 都可方便使用，而且可以輕鬆地與 Windows 7 應用程式整合。

## <a name="multi-touch-gestures-and-manipulation-and-inertia-apis"></a>多點觸控手勢和操作和慣性 Api

Windows 7 的功能改進了觸控和手勢支援，讓開發人員能夠快速又輕鬆地建立超越簡單滑鼠指標、按一下和拖曳的獨特應用程式體驗。 新的多點觸控 Api 支援豐富的手勢，例如平移、縮放和旋轉。 所有手勢都提供直接視覺效果的意見反應，並以自然且直覺的方式與基礎內容互動。 例如，縮放手勢會將視圖置中在筆勢的位置。 較低層級的觸控輸入 Api 也可用於自訂手勢定義和先進的觸控回應體驗。 Windows 7 提供的開發平臺，可讓開發人員透過處理多點觸控裝置的使用者輸入，以及改善使用者介面，為開發人員提供需要的工具，以開發多點觸控輸入裝置的創意應用程式。 結果是更直覺化的環境，可讓您在電腦互動方面進行創新。

Windows 7 也提供物件操作和慣性處理的平臺支援。 一組豐富的操作函數可讓您以非常精細的方式，同時延展、調整大小或旋轉多個物件。 例如，您可以使用觸控式手勢，在單一會話中修剪、調整大小及旋轉多個數位相片。

Windows 7 包含慣性 Api，可在物件移動時模擬慣性，並與操作 Api 一起工作。 例如，在相片應用程式中，您可以使用操作 Api 來讓使用者旋轉、調整大小和移動相片。 同樣地，如果使用者「參入」相片，慣性 Api 會提供自然的互動，並讓相片將應用程式視窗的框線停止或離開。  (參閱 [Windows Touch 程式設計指南](../wintouch/programming-guide.md) 和 [Windows Touch：開發人員資源](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch)。 ) 

## <a name="single-finger-panning"></a>Single-Finger 移動

在許多常見的應用程式中，觸控功能在流覽時更適合用於文字選取。 使用擴充的觸控 Api，開發人員的應用程式可以選擇啟用移動流覽而非拖曳。 例如，如果您建立的應用程式使用多點觸控手勢來播放音樂的使用者，您可以讓這些使用者只需向下或向下滑動，即可調整音量、變更歌曲或下載檔案。 不需要任何滾動。

Windows 7 為想要為下一代電腦建立應用程式的開發人員提供無限的機會。 最棒的是，它會執行檢查捲軸和執行平移語義的困難工作。 應用程式也會收到一組更豐富的事件和意見反應，以自訂筆勢的自訂控制項，而不是在舊版的 Windows 中。  (請參閱 [改善 Single-Finger 的移動體驗](../wintouch/improving-the-single-finger-panning-experience.md)。 ) 

## <a name="raw-touch-input-data"></a>原始觸控輸入資料

在 Windows 7 中，可透過存取較低層級觸控輸入訊息的互動模型來啟用新的觸控體驗，並提供觸控式訊息組合的自訂回應。 在應用程式中多點觸控繪製應用程式和自訂手勢等案例中，平臺支援接收原始觸控輸入資料。 您可以使用適用于觸控的平臺支援，或建立您自己的原始多點觸控體驗。  (參閱 [WM \_ 觸控訊息](../wintouch/wm-touchdown.md)。 ) 

 

 