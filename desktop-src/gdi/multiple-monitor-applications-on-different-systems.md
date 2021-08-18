---
description: 若要讓您的多個 monitoraware 應用程式在具有和無多個監視器支援的系統上運作，請使用 Multimon 連結您的應用程式。
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: 不同系統上的多個監視器應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c597261063f49b6e6856576e3528698291348afb2b8478d854a824b92d2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037716"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>不同系統上的多個監視器應用程式

若要讓您的多個 monitoraware 應用程式在具有和無多個監視器支援的系統上運作，請使用 Multimon 連結您的應用程式。 您也必須 \_ \_ 在剛好一個 C 檔案中定義 COMPILE MULTIMON 存根。 如果系統不支援多個監視器，則會從 [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 傳回預設值，而多個監視器函式的作用就像只有一個顯示器一樣。 在多個監視器系統上，您的應用程式會正常運作。

因為負座標可以在 multimonitor 系統中輕鬆進行，所以您應該使用 **get \_ X \_ lParam** 和 **get \_ Y \_ lParam** 宏來取得封裝在 lParam 中的座標。

請勿使用大於 SM \_ CXSCREEN 和 sm CYSCREEN 的負座標或座標 \_ 來隱藏視窗。 使用這些限制來隱藏的 Windows 可能會顯示在另一個監視器上。 同樣地，請勿使用這些限制讓視窗保持可見，因為這可能會導致視窗貼齊至主要監視器。 最好重新檢查現有的應用程式是否有這些問題。 不過，您可以在主要監視器上執行應用程式，或將主要監視器保留在虛擬螢幕左上角，以將現有應用程式中的問題降至最低。

請注意，SM \_ CXMAXTRACK 和 sm \_ CYMAXTRACK 是針對桌面所定義，而不只是一個監視器。 使用這些限制的 Windows 可能需要重新定義。

父或相關視窗可能不在與子視窗相同的監視器上。 若要找出視窗的監視器，應用程式應該使用 [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) 函式。

若要在所有監視器上顯示幕幕保護，請與 Scrnsave 的最新版本連結。 否則，螢幕保護裝置可能只會出現在主要監視器上，並讓其他監視器保持不變。 與最新 Scrnsave 連結的螢幕保護裝置可在單一和多個監視器系統上運作。 若要在每個監視器上擁有不同的螢幕保護裝置，請使用多個監視功能來個別處理每個監視器。

以絕對座標（例如平板電腦）將座標傳遞給系統的輸入裝置，會將其游標輸入限制為主要監視器。 若要切換監視器之間的平板電腦輸入，請參閱 OEM 的指示。

若要將以絕對座標傳送的滑鼠輸入對應至整個虛擬畫面，請使用[](/windows/win32/api/winuser/ns-winuser-input)具有 MOUSEEVENTF \_ 絕對和 MOUSEEVENTF VIRTUALDESKTOP 的輸入結構 \_ 。

[**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)函數適用于多個監視系統。 但是，如果來源和目的地裝置內容不同， [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)、 [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt)、 [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)和 [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) 函數將會失敗。

 

 
