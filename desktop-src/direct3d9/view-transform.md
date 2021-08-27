---
description: 本節介紹 view 轉換的基本概念，並提供如何在 Direct3D 應用程式中設定視圖轉換矩陣的詳細資料。
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: " (Direct3D 9) 視圖轉換"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb184cb75f84a1d28ed6f03f2e65113ea65292fd6ca1871d517d472614f64a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118524"
---
# <a name="view-transform-direct3d-9"></a> (Direct3D 9) 視圖轉換

本節介紹 view 轉換的基本概念，並提供如何在 Direct3D 應用程式中設定視圖轉換矩陣的詳細資料。

檢視轉換將檢視器放置在世界空間中，並將頂點轉換成相機空間。 在相機空間，相機或檢視器位於原點，朝著正 z 方向看。 回想一下，Direct3D 會使用左手型座標系統，因此 z 在場景中是正面的。 檢視矩陣圍繞相機位置 (相機空間的起點) 將物件重新放置在世界空間中。

有許多的方式可建立檢視矩陣。 在所有情況下，相機在世界空間有特定邏輯位置和方向，做為起點用來建立檢視矩陣，套用到場景中的模型。 檢視矩陣平移並旋轉物件，將它們置於相機空間中 (相機位於原點)。 建立檢視矩陣的一個方式是為每個軸結合旋轉矩陣和轉移矩陣。 下列一般矩陣方程式適用於這種方式。

![檢視轉換的方程式](images/viewtran.png)

在這個公式中，V 是所建立的檢視矩陣，T 是將物件重新置放在世界空間中的轉移矩陣，而 Rₓ 到 R<sub>z</sub> 則是沿著 x、y 與 z 軸旋轉物件的旋轉矩陣。 轉移矩陣與旋轉矩陣以世界空間中的相機邏輯位置和方向為基礎。 因此，如果世界中的相機邏輯位置是 <10，20100>，則轉譯矩陣的目標是在 X 軸移動物件-10 個單位，沿著 y 軸移動20個單位，並沿著 Z 軸移動-100 個單位。 在公式中旋轉矩陣以相機方向為基礎，亦即相機空間的軸旋轉多少，不對齊世界空間。 例如，如果前面所提到的相機往下指，其 z 軸是 90 度（pi/2 弧度），不對齊世界空間的 z 軸，如下圖所示。

![相機檢視空間相對於世界空間的圖例](images/camtop.png)

旋轉矩陣對場景中模型套用相等但相反的旋轉大小。 這個相機的檢視矩陣包含圍繞 x 軸 -90 度的旋轉。 旋轉矩陣與轉移矩陣結合，建立調整場景中物件之位置和方向的檢視矩陣，使其頂端面向相機，提供相機在模型上方的表面現象。

## <a name="setting-up-a-view-matrix"></a>設定檢視矩陣

[**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md)和 [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md)協助程式函式會根據相機位置和查看點建立視圖矩陣。

下列範例會建立左手座標的視圖矩陣。


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



Direct3D 使用世界和檢視矩陣來設定數個內部資料結構。 每當您設定世界或檢視矩陣，系統會重新計算相關內部結構。 頻繁設定這些矩陣通常在計算上耗費時間。 您可以串連世界和檢視矩陣成為世界檢視矩陣 (您將其設為世界矩陣)，然後將檢視矩陣設為單位矩陣，將所需的計算次數最小化。 保留個別世界和檢視矩陣的快取複本，您可以視需要修改、串連並重設世界矩陣。 為了清楚起見，範例很少採用這種優化。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換](transforms.md)
</dt> </dl>

 

 



