---
description: 大部分的應用程式會嘗試支援 WYSIWYG (您看到的是) 輸出的結果。
ms.assetid: 34a1f37c-0fbf-451b-bb55-80ad85bcd4de
title: WYSIWYG 顯示和輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c03e4fa653c0d8e891cb079a7a7e7a003f9ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980640"
---
# <a name="wysiwyg-display-and-output"></a>WYSIWYG 顯示和輸出

大部分的應用程式會嘗試支援 WYSIWYG (您看到的是) 輸出的結果。 這表示在應用程式視窗中以10點的全形粗體字型繪製的文字在列印時應該會有類似的外觀。 幾乎無法取得真正的 WYSIWYG 輸出，甚至在大部分情況下都不需要。 這是因為影片和印表機技術的差異，螢幕上的圖元通常會大於一般雷射印表機上的一個點。 觀賞距離也不同;電腦使用者通常會在螢幕上離開兩英尺，但讀取器的眼睛通常是從列印頁面中的一英尺或更短。

為了彌補螢幕和列印頁面之間的可讀性差異，系統支援一個稱為邏輯英寸的單位，一律以圖元為單位來指定。 若為影片顯示器，邏輯英寸一律會大於實體的長度，以彌補較長的觀賞距離，而 (通常會) 粗解析度。 若是印表機，邏輯英寸永遠等於實體英寸。

若要在繪製文字時取得 WYSIWYG 效果，牽涉到兩個相關的問題：讓個別字元看起來相同，以及與裝置無關的頁面配置。 若要解決第一個問題，應用程式可以使用 [**CreateFont**](/windows/desktop/api/wingdi/nf-wingdi-createfonta) 函式來指定理想 (或邏輯) 字型的字型名稱和大小，然後呼叫 [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) 函數來識別顯示或印表機裝置內容。 當應用程式呼叫 **SelectObject** 時，系統會選取最接近指定之邏輯字型的實體字型。 當系統選取顯示字型時，它會選擇大於實際大小的實體字型。 這是因為顯示器上有較大的邏輯英寸。 但是從使用者的觀點來看，它似乎非常接近正確的高度。 當系統選取印表機的字型時，它會選擇實際上是所要求大小的實體字型。 如需字體和文字輸出的詳細資訊，請參閱字型 [和文字](/windows/desktop/gdi/fonts-and-text)。

第二個問題（與裝置無關的頁面配置）可以藉由使用 TrueType 計量來解決。 即使維持與16位 Windows 版本的相容性，也是如此。 如需詳細資訊，請參閱 [使用可移植的 TrueType 計量](/windows/desktop/gdi/using-portable-truetype-metrics)。

若要在繪製點陣圖圖形時取得 WYSIWYG 效果，應用程式可以取出螢幕和列印頁面的寬度和高度（以邏輯英寸為單位）。 使用這些值時，應用程式可以建立水準和垂直縮放比例，以維持在印表機上繪製點陣圖影像的比例。 如需點陣圖和點陣圖輸出的詳細資訊，請參閱 [點陣圖](/windows/desktop/gdi/bitmaps)。

 

 
