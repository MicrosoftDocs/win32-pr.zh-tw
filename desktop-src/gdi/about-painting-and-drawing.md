---
description: 幾乎所有的應用程式都會使用畫面來顯示他們所操作的資料。
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: 關於繪製和繪製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991154"
---
# <a name="about-painting-and-drawing"></a>關於繪製和繪製

幾乎所有的應用程式都會使用畫面來顯示他們所操作的資料。 應用程式會繪製影像、繪製圖形以及寫入文字，讓使用者可以在建立、編輯和列印資料時加以查看。 Microsoft Windows 提供繪圖和繪圖的豐富支援，但由於多工作業系統的本質，因此應用程式必須在存取畫面時互相合作。

為了讓所有應用程式都能順暢且合作地運作，系統會管理螢幕的所有輸出。 應用程式會使用 windows 作為其主要輸出裝置，而不是螢幕本身。 系統會提供可唯一對應至 windows 的顯示裝置內容。 應用程式會使用顯示裝置內容，將其輸出導向至指定的視窗。 在視窗中繪製 (將輸出導向至該應用程式，) 可防止應用程式干擾其他應用程式的輸出，並允許應用程式互相並存，同時仍能充分利用系統的圖形功能。

-   [在視窗中繪製的時機](when-to-draw-in-a-window.md)
-   [WM \_ 油漆訊息](the-wm-paint-message.md)
-   [不含 WM \_ 油漆訊息的繪圖](drawing-without-the-wm-paint-message.md)
-   [視窗座標系統](window-coordinate-system.md)
-   [視窗區域](window-regions.md)
-   [視窗背景](window-background.md)
-   [最小化視窗](minimized-windows.md)
-   [調整視窗大小](resized-windows.md)
-   [非工作區](nonclient-area.md)
-   [子視窗更新區域](child-window-update-region.md)
-   [顯示裝置](display-devices.md)
-   [視窗更新鎖定](window-update-lock.md)
-   [累積的周框](accumulated-bounding-rectangle.md)

 

 



