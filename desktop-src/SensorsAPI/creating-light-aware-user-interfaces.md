---
description: 本節涵蓋環境光線感應器資料的使用，以及使用者介面功能和程式內容如何針對許多光源條件進行優化。
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: 建立 Light-Aware 使用者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944749"
---
# <a name="creating-light-aware-user-interfaces"></a>建立 Light-Aware 使用者介面

本節涵蓋環境光線感應器資料的使用，以及使用者介面功能和程式內容如何針對許多光源條件進行優化。

環境燈光感應器會公開可用來判斷感應器所在之照明條件各方面的資料。 環境光線感應器可以公開環境的整體亮度 (illuminance) 以及周圍照明的其他層面，例如 chromaticity 或色溫。

當系統回應照明狀況時，電腦可能會有數種方式可發揮效用。 這些功能包括控制電腦顯示器的亮度 (Windows 7) 的全新、完整支援功能、自動調整發亮鍵盤的照明等級，甚至是其他燈光的亮度控制 (例如按鈕照明、活動燈等) 。

終端使用者程式也可以從燈光感應器獲益。 程式可以套用適用于特定光源條件的主題，例如特定的室外主題和室內主題。 也許最重要的一點是，「光線感應器」與「程式」整合的最重要層面，就是根據光源的可讀性和可讀性優化。

感應器 API 可讓您建立這類程式。 請考慮下列案例。

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a>案例：使用您的膝上型電腦流覽餐廳

假設您想要使用電腦協助您流覽至新餐廳。 您會在房屋中開始查詢餐廳的位址，並規劃您的路線。 下列螢幕擷取畫面顯示您的流覽程式如何優化其 UI，以顯示室內照明條件中的詳細資訊。

![針對室內照明設計的 ui。](images/nav-normal.png)

當您移至您的車輛之外時，您會遇到直接的陽光，這會讓膝上型電腦的螢幕難以閱讀。 下列螢幕擷取畫面顯示您的程式如何改變其 UI，以最大化可讀性/可讀性。 在此觀點中，大部分的詳細資料都已省略，而且對比會最大化。

![專為直接光源條件設計的 ui。](images/nav-contrast.png)

當您更接近餐廳、夜間的方法，它的範圍會變暗。 在下列螢幕擷取畫面中，已針對輕量的視覺效果優化流覽程式的 UI。 藉由整體使用較深的色彩，此 UI 很容易就能在深車中一目了然。

![針對低度觀賞而設計的 ui。](images/nav-lowlight.png)

在本節的其餘部分，您將探索一些可為各種光源條件優化程式，以及如何使用感應器 API 來協助啟用淺感知 UI 的事項。

## <a name="in-this-section"></a>本節內容

-   [Light-Aware 的使用者介面基礎](fundamentals-of-light-aware-user-interfaces.md)
-   [Light-Aware 使用者介面的範例](examples-of-light-aware-user-interfaces.md)
-   [優化使用者體驗](optimizing-the-user-experience.md)
-   [瞭解和解讀 Lux 值](understanding-and-interpreting-lux-values.md)
-   [使用 Light 感應器資料](handling-data-from-multiple-light-sensors.md)

 

 



