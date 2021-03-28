---
description: 每當應用程式建立 DC 並立即開始呼叫 GDI 繪圖或輸出函式時，它就會利用預設的頁面空間來進行裝置空間，以及使用裝置空間來進行用戶端區域的轉換。
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: 預設轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5f13c764a92c005fad36c9f2599b99a654284f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972716"
---
# <a name="default-transformations"></a>預設轉換

每當應用程式建立 DC 並立即開始呼叫 GDI 繪圖或輸出函式時，它就會利用預設的頁面空間來進行裝置空間，以及使用裝置空間來進行用戶端區域的轉換。 在應用程式第一次呼叫 [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) 函式以將模式設定為 GM \_ ADVANCED，然後呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式之前，不會發生「世界到頁面空間」轉換。

使用 MM \_ TEXT (預設頁面空間至裝置空間轉換) 會產生一對一的對應; 也就是說，頁面空間中的給定點會對應到裝置空間中的相同點。 如先前所述，矩陣不會指定這項轉換。 相反地，它是以視窗的寬度和視窗的高度（依視窗的高度）將區寬的寬度分割來取得。 在預設情況下，視口維度是1圖元 x 1 圖元，而視窗維度是1頁單位（1頁單位）。

裝置空間至實體裝置 (工作區、桌面或印表機紙張) 轉換一律會產生一對一的對應;也就是說，裝置空間中的一個單位一律等於用戶端區域、桌面上或頁面上的一個單位。 這項轉換的唯一目的是轉譯;它可確保在應用程式的視窗中正確顯示輸出，無論該視窗在桌上型電腦上的移動位置為何。

MM 文字的一個獨特層面 \_ 是頁面空間中 y 軸的方向。 在 MM \_ TEXT 中，正 y 軸會向下延伸，而負 y 軸會向上擴充。

 

 



