---
description: 在轉譯期間，管線會在每個矩形上插入頂點資料。
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: " (Direct3D 9) 的三角形插補"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972952"
---
# <a name="triangle-interpolation-direct3d-9"></a> (Direct3D 9) 的三角形插補

在轉譯期間，管線會在每個矩形上插入頂點資料。 頂點資料可以是各種不同的資料，而且可以包含 (但不限於) ：擴散色彩、反射色彩、擴散 Alpha (三角形不透明度) 、反射 Alpha 和霧化因數 (取自固定函式頂點管線的反射 Alpha，以及可程式化頂點管線) 的霧化暫存器。 頂點資料是由 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告所定義。

某些頂點資料的插補取決於目前的陰影模式，如下表所示。



| 陰影模式 | Description                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一般         | 在平面陰影模式下，只內插霧因數。 對於所有其他內插補值，三角形中第一個頂點的色彩會套用到整個面。 |
| Gouraud      | 在所有三個頂點之間執行線性內插補點。                                                                                                               |



 

擴散色彩和反射色彩的處理方式不同，視色彩模型而定。 在 RGB 色彩模型，系統會在內插補點中使用紅色、綠色和藍色元件。

色彩的 Alpha 元件被視為不同的內插補值，因為裝置驅動程式可透過兩種不同方式實作透明度：使用紋理混合或使用點畫。

使用 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 ShadeCaps 成員，判斷目前設備磁碟機支援的插補形式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[座標系統和幾何](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



