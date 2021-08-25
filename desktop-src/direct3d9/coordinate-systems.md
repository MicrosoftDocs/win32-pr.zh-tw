---
description: 3D 圖形應用程式通常會使用兩種類型的笛卡兒座標系統：左手和右手。
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: " (Direct3D 9) 協調系統"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e47b87ae6374d68b8c836dfb4818781e83e77c288f7bf05b121dbb4426c9aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857571"
---
# <a name="coordinate-systems-direct3d-9"></a> (Direct3D 9) 協調系統

3D 圖形應用程式通常會使用兩種類型的笛卡兒座標系統：左手和右手。 在這兩個座標系統中，正 x 軸指向右側，而正 y 軸指向上方。 您可以藉由將左手或右手指指向正 x 軸方向，並將它們彎曲至正 y 軸的方向，以記得正 z 軸指向的方向。 您拇指所指的方向，不論是指向您或指向您的反方向，即是該座標系統正 z 軸所指的方向。 下圖顯示這兩個座標系統。

![左手系和右手系笛卡兒座標的圖例](images/leftrght.png)

Direct3D 使用左手系座標系統。 如果您要移植以右手座標系統為基礎的應用程式，則必須對傳遞給 Direct3D 的資料進行兩項變更。

-   翻轉三角形頂點的順序，讓系統從前面順時針轉動這些頂點。 意即如果頂點為 v0、v1、v2，請依 v0、v2、v1 的順序傳遞給 Direct3D。
-   使用檢視矩陣將世界空間在 z 方向縮放 -1。 若要這樣做，請將您用於 \_ \_ 視圖矩陣之 D3DMATRIX 結構的31、32、 \_ 33 和 \_ 34 成員[](d3dmatrix.md)的正負號翻轉。

若要取得右手 world 的數量，請使用 [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) 和 [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) 函數來定義投射轉換。 不過，請小心使用對應的 [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) 函式、反轉背面剔除順序，並據此配置 cube 對應。

雖然左手系和右手系座標是最常見的系統，但 3D 軟體中還使用各種不同的其他座標系統。 舉例來說，3D 模型應用程式也常使用一種座標系統，其中 y 軸指向檢視器或指向其反方向，而且 z 軸朝上。

正式來說，一組基礎向量的方向 (也就是座標系統) 可以藉由計算一組特定基礎向量所定義之矩陣的行列式來尋找。 如果行列式是正面的，則基準會被視為「積極」導向 (或右手) 。 如果行列式是負數，則會將其視為「負面」導向 (或左手) 。 如需行列式的說明，請參閱任何線性代數資源。

非正式地說，您可以使用「右/左邊規則」來判斷指定的一組基礎向量是否形成右手或左的座標系統。

在3D 座標系統中定義的物件上所執行的基本作業為轉譯、旋轉和縮放。 您可以結合這些基本轉換來建立轉換矩陣。 如需詳細資訊，請參閱 [ (Direct3D 9 的轉換) ](transforms.md)。

當您結合這些作業時，結果不可相互交換。您以倍數增加矩陣的順序至關重要。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[座標系統和幾何](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



