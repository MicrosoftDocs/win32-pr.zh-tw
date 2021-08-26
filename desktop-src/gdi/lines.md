---
description: 線條是點陣顯示器上的反白顯示圖元 (或列印頁面上的一組點，) 由兩個點來識別：起點和結束點。
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: 線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b81976984cecc3d4d3b27fb3e474e896c6e81f03e6f601db36418b9e3cf197c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062098"
---
# <a name="lines"></a>線條

線條是點陣顯示器上的反白顯示圖元 (或列印頁面上的一組點，) 由兩個點來識別：起點和結束點。 位於起點的圖元一律會包含在行中，而且一律會排除位於結束點的圖元。 這種類型的 (有時稱為內含專屬。 ) 

當應用程式呼叫其中一個線條繪圖函式、圖形裝置介面 (GDI) ，或在某些情況下，設備磁碟機會判斷應該反白顯示的圖元。 GDI 是動態連結程式庫 (DLL) ，可處理來自應用程式的圖形函式呼叫，並將這些呼叫傳遞給設備磁碟機。 設備磁碟機是接收來自 GDI 之輸入的 DLL、將輸入轉換成裝置命令，然後將這些命令傳遞給適當的裝置。 GDI 會使用數位差異分析器 (DDA) 來判斷可定義線條的一組圖元。 DDA 藉由檢查線條上的每個點，並在顯示介面上識別這些圖元， (或列印) 頁面上對應到點的點，來決定一組圖元。 下圖顯示的是線條、其起點、其結束點，以及使用簡單的 DDA 強調顯示的圖元。

![圖例顯示圖元的方格、開始和結束點、線條，以及沿著直線的圖元陰影](images/cslcv-01.png)

最簡單且最常見的 DDA 是 Bresenham 或增量，DDA。 此演算法的修改版本會在 Windows 中繪製線條。 為了簡單起見，會記下遞增的 DDA，但其誤差也會注明。 因為它會四捨五入到最接近的整數值，所以有時無法表示應用程式所要求的原始程式列。 GDI 使用的 DDA 不會四捨五入到最接近的整數。 如此一來，這個新的 DDA 會產生輸出，有時會比應用程式所要求的原始程式列更接近外觀。

> [!Note]  
> 如果應用程式需要無法使用新的 DDA 達成的行輸出，它可以藉由呼叫 [**LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) 函式，並提供私用的 Dda ([**LineDDAProc**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)) 來繪製自己的行。 不過， **LineDDA** 函式繪製的線條速度會比線條繪圖函式慢許多。 如果速度是主要考慮，請勿在應用程式中使用此函數。

 

應用程式可以使用新的 DDA 來繪製單一線條和多個連接的線段。 應用程式可以藉由呼叫 [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) 函數來繪製單一行。 此函式會從目前的位置（但不包括指定的結束點）繪製線條。 應用程式可以藉由呼叫 [**彙總函式來**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) 繪製一連串的連接直線線段，提供指定每個線條區段之結束點的點陣列。 應用程式可以藉由呼叫 [**PolyPolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) 函式，並提供必要的結束點，來繪製多個脫離的連接線區段。

下圖顯示藉由呼叫 [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)、彙總函式和 [**PolyPolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)函式所 [**建立的行**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)輸出。

![圖例顯示直線、"l" 形方塊，以及兩個顯示3d 的圖形](images/cslcv-02.png)

 

 



