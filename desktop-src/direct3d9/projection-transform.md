---
description: 您可以將投影轉換視為控制攝影機的內部;它類似于選擇相機的鏡頭。
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: " (Direct3D 9) 的投射轉換"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187496"
---
# <a name="projection-transform-direct3d-9"></a> (Direct3D 9) 的投射轉換

您可以將投影轉換視為控制攝影機的內部;它類似于選擇相機的鏡頭。 這是三種轉換類型中最複雜的轉換。 這項投射轉換的討論區分為下列主題。

投影矩陣通常是縮放和透視投影。 投影轉換會將檢視範圍轉換成立方體形狀。 由於檢視範圍的近端小於遠端，這會影響靠近相機之物體的展開；這也是透視套用到場景的方式。

在[檢視範圍](viewports-and-clipping.md)中，相機和檢視範圍空間的原點之間的距離隨意定義為 D，以便投影矩陣看起來如下圖。

![投影矩陣的圖例](images/projmat1.png)

檢視矩陣會透過在 z 方向平移 - D 將相機轉移至原點，轉移矩陣就如下圖。

![轉移矩陣的圖例](images/projmat2.png)

將平移矩陣乘以投射矩陣 (T \* P) 會提供複合投射矩陣，如下圖所示。

![複合投影矩陣的圖例](images/projmat3.png)

透視轉換會將檢視範圍轉換成新的座標空間。 請注意，範圍會變成立方體，而原點也會從場景的右上角移到中心，如下圖所示。

![透視轉換如何將檢視範圍變更為新的座標空間的圖表](images/cuboid.png)

在透視轉換中，x 方向與 y 方向的限制是 -1 及 1。 對於正面平面 z 方向的限制是 0 而對於後面平面是 1。

這個矩陣會根據從相機到近裁剪平面的指定距離平移和縮放物件，但是不會考慮視野 (fov)，而且在距離中對於物件產生的 z 值可能幾乎相同，使得難以比較深度。 下列矩陣處理這些問題，並且調整頂點以考慮檢視區的長寬比，使其成為透視投影的不錯選擇。

![透視投影的矩陣圖例](images/prjmatx1.png)

在這個矩陣中，Zₙ 是近裁剪平面的 z 值。 變數 w、h 和 Q 的意義如下。 請注意，fov<sub>w</sub>和 fovₖ 以弧度代表區檢視區的水平和垂直視野。

![變數的方程式意義](images/prjmatx2.png)

對於您的應用程式，使用視野角度來定義 x 和 y 縮放係數，可能不如使用檢視區的水平和垂直維度 (在相機空間中) 來得便利。 既然數學解出來，下列 w 和 h 的兩個方程式使用檢視區的維度，並且相當於前述方程式。

![W 和 h 變數的方程式意義](images/prjmatx3.png)

在這些公式中，Zₙ 代表近裁剪平面的位置，而 V<sub>w</sub>和 Vₕ 變數代表檢視區的寬度與高度 (照相機空間中)。

若是 c + + 應用程式，這兩個維度會直接對應至 [**D3DVIEWPORT9**](d3dviewport9.md) 結構的寬度和高度成員。

不論您決定使用哪個公式，務必將 Zₙ 設定為越大值越好，因為 z 值非常接近相機，不會差太多。 這會使得使用 16 位元 z 緩衝區的深度比較變得有些複雜。

如同「世界」和「視圖」轉換，您可以呼叫 [**IDirect3DDevice9：： SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) 方法來設定投影轉換。

## <a name="setting-up-a-projection-matrix"></a>設定投射矩陣

下列 ProjectionMatrix 範例函式會設定 front 和 back 裁剪平面，以及視角的水準和垂直欄位。 View 的欄位應小於 pi 弧度。


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



建立矩陣之後，請使用 [**IDirect3DDevice9：： SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) 指定 D3DTS 投射來設定它 \_ 。

D3DX 公用程式程式庫提供下列功能，協助您設定投影矩陣。

-   [**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
-   [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
-   [**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
-   [**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
-   [**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
-   [**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a>易記投影矩陣

Direct3D 可使用已被世界、檢視和投影矩陣轉換的 w 元件頂點，來執行深度緩衝區的深度計算或霧的效果。 這類運算需要投影矩陣將 w 標準化為等於世界空間 z。 簡言之，如果您的投影矩陣包含不是 1 的 (3,4) 係數，您必須透過反轉 (3,4) 係數來縮放所有係數以製作適當的矩陣。 如果您不提供相符的矩陣，霧效果和深度緩衝區就不會正確套用。

下圖顯示不相符的投影矩陣和縮放的矩陣，所以將會啟用眼睛相關的霧化。

![不相符投影矩陣及具有眼睛相關霧化的矩陣圖例](images/eyerlmx.png)

在前述矩陣中，所有變數都假設為非零。 如需眼睛相關模糊的詳細資訊，請參閱 [眼睛相關與以 Z 為基礎的深度](pixel-fog.md)。 如需以 w 為基礎深度緩衝的詳細資訊，請參閱 [ (Direct3D 9) 的深度緩衝區 ](depth-buffers.md)。

Direct3D 使用目前以 w 型深度計算的投影矩陣。 如此一來，應用程式必須設定相符的投影矩陣，才能接收所要的 w 型功能，即使它們不使用 Direct3D 進行轉換。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換](transforms.md)
</dt> </dl>

 

 
