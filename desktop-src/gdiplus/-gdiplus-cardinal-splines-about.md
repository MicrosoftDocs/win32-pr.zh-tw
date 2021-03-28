---
description: 基本曲線是一條聯結的個別曲線，形成較大的曲線。
ms.assetid: 4fc62f00-7006-4ade-bfcc-091a3a97d889
title: 基本曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d85c0163e405a6f9346f521b4057eb936108cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192353"
---
# <a name="cardinal-splines"></a>基本曲線

基本曲線是一條聯結的個別曲線，形成較大的曲線。 曲線是由點陣列和張力參數所指定。 基線曲線會順暢地通過陣列中的每個點;曲線的 tightness 沒有尖角，而且沒有任何突然變化。 下圖顯示一組點，以及通過集合中每個點的基本曲線。

![圖例顯示通過六個定義點的基線曲線](images/aboutgdip02-art09.gif)

實體曲線是一種精簡的木頭或其他彈性的教材。 在數學曲線的出現之前，設計人員使用了實體曲線來繪製曲線。 設計工具會將曲線放在一張紙上，並錨定到指定的點集合。 然後，設計工具可以使用鉛筆沿著曲線繪製來建立曲線。 根據實體曲線的屬性，指定的點集合可能會產生各種曲線。 例如，具有高阻力來彎曲的曲線會產生與極具彈性曲線的不同曲線。

數學曲線的公式是以彈性棒敲的屬性為基礎，因此數學曲線所產生的曲線類似于實體曲線所產生的曲線。 如同不同張力的實體曲線會透過一組指定的點來產生不同的曲線，具有張力參數不同值的數學曲線將會透過一組指定的點來產生不同的曲線。 下圖顯示四個透過相同點集合傳遞的基本曲線。 會顯示每個曲線的張力。 請注意，張力0會對應到無限的實體張力，強制曲線採用最短的方式 (直線之間) 的點。 一個張力1對應到無實體張力，讓曲線能夠採用最少的折彎軌跡。 當張力值大於1時，曲線的行為就像是壓縮的彈簧，會被推送以取得較長的路徑。

![顯示四個基本曲線的圖，透過相同的三個點](images/aboutgdip02-art10.gif)

請注意，上圖中的四個曲線會在起始點共用相同的正切線條。 正切函數是沿著曲線從起點到下一個點繪製的線條。 同樣地，結束點的共用正切函數是從結束點繪製到曲線上上一個點的線條。

若要繪製基本曲線，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件和 [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) 物件的陣列。 **Graphics** 物件提供 [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inreal))方法，它會繪製曲線，而 **Pen** 物件會儲存曲線的屬性，例如線條寬度和色彩。 **Point** 物件的陣列會儲存曲線將通過的點。 下列範例會繪製在 *myPointArray* 中傳遞點的基本曲線。 第三個參數是張力。


```
myGraphics.DrawCurve(&myPen, myPointArray, 3, 1.5f);
```



 

 



