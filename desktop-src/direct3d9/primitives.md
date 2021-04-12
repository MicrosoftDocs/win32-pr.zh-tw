---
description: 3D 基本類型是形成單一 3D 實體的頂點集合。 最簡單的基本物件是3D 座標系統中的點集合，稱為點清單。
ms.assetid: vs|directx_sdk|~\primitives.htm
title: " (Direct3D 9 圖形) 的基本專案"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108456"
---
# <a name="primitives-direct3d-9-graphics"></a> (Direct3D 9 圖形) 的基本專案

3D 基本類型是形成單一 3D 實體的頂點集合。 最簡單的基本物件是3D 座標系統中的點集合，稱為點清單。

3D 基本專案通常是多邊形。 多邊形是由至少三個頂點來描繪的 3D 封閉圖形。 最簡單的多邊形為三角形。 Microsoft Direct3D 使用三角形來組合大部分的多邊形，因為這保證三角形中的所有三個頂點為共面。 轉譯非平面頂端沒有效率。 您可以結合三角形來形成大型且複雜的多邊形和網格。

下圖顯示立方體。 兩個三角形形成立方體的每個面。 整組三角形形成一個立方體基本類型。 您可以將材質和材質套用至基本專案的表面，讓它們看起來就像是單一穩固的表單。 如需詳細資訊，請參閱 [ (direct3d 9) ](materials.md) 和 [Direct3D 材質 (direct3d 9) ](direct3d-textures.md)的材質。

![每個面有兩個三角形的立方體的圖例](images/cube3d.png)

您也可以使用三角形。建立表面看起來像是平滑曲線的基本類型。 下圖顯示使用三角形模擬球體的方式。 在套用材質之後，球體會在呈現時顯示為曲線。 尤其是當您使用 Gouraud 陰影時更是如此。 如需詳細資訊，請參閱 [Gouraud 陰影](shading-modes.md)。

![使用三角形模擬球體的圖例](images/sphere3d.png)

Direct3D 裝置可以建立和操作下列類型的基本類型。

-   [點清單](point-lists.md)
-   [行清單](line-lists.md)
-   [行條紋](line-strips.md)
-   [三角形清單](triangle-lists.md)
-   [三角形條紋](triangle-strips.md)
-   [ (Direct3D 9) 的三角形風扇 ](triangle-fans.md)

您可以使用 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面的任何轉譯方法，從 c + + 應用程式呈現基本類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 裝置](direct3d-devices.md)
</dt> </dl>

 

 
