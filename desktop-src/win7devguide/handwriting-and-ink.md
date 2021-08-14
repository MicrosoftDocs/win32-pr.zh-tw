---
title: 手寫和筆墨
description: 隨著市面上的 Tablet Pc 激增，平板電腦功能也成為主流運算的一部分。
ms.assetid: 22caf8b3-d519-418f-b662-180d270b7cfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4704300ed28d1ca10987ad0c22633ba65a3f529ec8ebeab63f7ea62137839d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118708933"
---
# <a name="handwriting-and-ink"></a>手寫和筆墨

隨著市面上的 *Tablet pc* 激增， *平板* 電腦功能也成為主流運算的一部分。 在 Windows 7 中，觸控和書寫是一流的使用者體驗。 Windows 7 提供更高的精確度和速度，以改善畫筆體驗。 手寫輸入已改善，並支援更多語言。 文字輸入面板提供預測文字，以提供更高速的輸入和修正。 透過個人化語言辨識中所有語言、自訂字典和突破的個人化，來改善手寫精確度。 改良的互動模型可在可攜式電腦常見的小型高解析度畫面上，提供更好的閱讀體驗。  (參閱 [設計文字輸入面板的](../tablet/programming-the-text-input-panel.md)程式。 ) 

![tablet pc 輸入面板](images/windows7-4.jpg)

文字輸入面板具有簡單的文字校正功能

## <a name="math-recognition"></a>數學辨識

新的數學辨識功能可讓使用者以手寫方式在應用程式中輸入數學，也就是輸入數學運算式的最自然、最有效率的方式。 這項功能是由兩個 UI 元件所提供。 數學輸入面板是一種獨立的 Windows 配件，適用于任何數學感知應用程式。 數學輸入控制項透過其 API 整合至應用程式。

基礎 UI 元件是數學辨識器。 此引擎會辨識手寫的數學運算式，並將結果轉譯為 *MathML* 格式，以便讓應用程式使用。 修正經驗已經過改善，可協助使用者更快進行修正。  (參閱程式 [設計數學輸入控制項](../tablet/programming-the-math-input-control.md)。 ) 

![數學輸入面板](images/windows7-5.jpg)

數學辨識可讓使用者透過手寫方式在應用程式中輸入數學

## <a name="handwriting-with-personalized-custom-dictionary"></a>使用個人化自訂字典手寫

在許多案例中，良好的手寫精確度需要針對使用領域量身打造的字典。 Windows 7 引進了自訂字典，可針對特製化詞彙啟用更好的手寫辨識。 撰寫垂直應用程式的開發人員（例如醫療處方記事本），現在可以將特定詞彙新增至其應用程式，例如藥物名稱。  (請參閱[Windows Touch 和 Tablet PC 開發人員的增強功能](https://www.microsoft.com/whdc/device/input/Touch_tab_enhance.mspx)。 ) 

 

 