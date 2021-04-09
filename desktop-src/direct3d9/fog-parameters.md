---
description: 霧化參數是透過裝置轉譯狀態來控制。
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: " (Direct3D 9) 的霧化參數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846172"
---
# <a name="fog-parameters-direct3d-9"></a> (Direct3D 9) 的霧化參數

霧化參數是透過裝置轉譯狀態來控制。 圖元和頂點霧化類型都支援在 [ (Direct3D 9) 的霧化公式 ](fog-formulas.md)中引進的所有霧化公式。 [**D3DFOGMODE**](./d3dfogmode.md)列舉型別定義常數，可讓您用來識別您想要 Microsoft Direct3D 使用的霧化公式。 D3DRS \_ FOGTABLEMODE 轉譯狀態控制 Direct3D 用於圖元霧化的霧化模式，而 D3DRS FOGVERTEXMODE 轉譯狀態則 \_ 控制頂點霧化的模式。

使用線性霧化公式時，您可以透過 D3DRS \_ FOGSTART 和 D3DRS FOGEND 轉譯狀態來設定開始和結束距離 \_ 。 系統解釋這些值的方式取決於您的應用程式所使用的霧化類型-圖元或頂點霧化，以及當使用圖元霧化時，如果使用以 z 為基礎或以 w 為基礎的深度。 下表匯總了霧型別及其開始與結束單位。



| 霧化類型  | 霧化開始/結束單位      |
|-----------|--------------------------|
| 圖元 (Z)  | 裝置空間 \[ 0.0、1。0\] |
| 圖元 (W)  | 攝影機空間             |
| 頂點    | 攝影機空間             |



 

D3DRS \_ FOGDENSITY 轉譯狀態會控制啟用指數霧化公式時所套用的霧化密度。 相較于從0.0 到 1.0 (內含) ，相較于調整指數中的距離值，霧化密度基本上是加權因數。

系統用於霧化混色的色彩是透過 D3DRS \_ FOGCOLOR 裝置轉譯狀態來控制。 如需詳細資訊，請參閱 [ (direct3d 9 的霧化色彩) ](fog-color.md) 和 [ (direct3d 9) 的霧化 ](fog-blending.md)混色。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[霧化類型](fog-types.md)
</dt> </dl>

 

 
