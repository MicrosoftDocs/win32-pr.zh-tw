---
description: 翻頁是多媒體、動畫和遊戲軟體的關鍵;這與您可以使用一張紙來進行動畫的方式類似。
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: " (Direct3D 9 的頁面翻轉和後臺緩衝) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107001645"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a> (Direct3D 9 的頁面翻轉和後臺緩衝) 

翻頁是多媒體、動畫和遊戲軟體的關鍵;這與您可以使用一張紙來進行動畫的方式類似。 在每個頁面上，演出者會稍微變更圖，因此當您在工作表之間快速切換時，繪圖就會顯示為動畫。

軟體中的頁面翻轉與此程式類似。 Direct3D 會透過交換鏈（這是裝置的屬性）來實行頁面翻轉功能。 一開始，您可以設定一系列的 Direct3D 緩衝區，以將演出者的紙張翻轉到下一頁。 第一個緩衝區稱為色彩前端緩衝區。 它背後的緩衝區稱為回緩衝區。 您的應用程式會寫入背景緩衝區，然後翻轉色彩前端緩衝區，讓背景緩衝區顯示在畫面上。 當系統顯示影像時，您的軟體會再次寫入至背景緩衝區。 只要您要製作動畫，程式就會繼續進行，讓您有效率地製作影像動畫。

Direct3D 可讓您輕鬆地設定翻頁的配置，從簡單的雙重緩衝配置 (具有一個背景緩衝區的彩色前端緩衝區) 到更複雜的配置，還有額外的背景緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 表面](direct3d-surfaces.md)
</dt> <dt>

[什麼是交換鏈？ (Direct3D 9) ](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



