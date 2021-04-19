---
description: 將霧化新增至3D 場景可以增強逼真、提供 ambiance 或設定調式，以及在較遠的幾何進入視野時，有時會造成隱匿的構件。
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: " (Direct3D 9) 的霧化"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972101"
---
# <a name="fog-direct3d-9"></a> (Direct3D 9) 的霧化

將霧化新增至3D 場景可以增強逼真、提供 ambiance 或設定調式，以及在較遠的幾何進入視野時，有時會造成隱匿的構件。 Direct3D 支援兩種霧化模型：圖元霧化和頂點霧化，各有自己的功能和程式設計介面。

基本上，會根據場景中物件的深度或與視點之間的距離，將場景中的物件色彩與所選擇的霧化色彩混合，來實行霧化。 隨著物件的成長較遠，其原始色彩會以所選的霧化色彩更多及更高的色彩，建立物件在場景中浮動浮動的微小物件。 下圖顯示在沒有霧化的情況下呈現的場景，以及已啟用霧化的類似場景。

![具有和不具有霧化之相同場景的圖例](images/fogcomp.png)

在此圖中，左邊的場景具有明確的範圍，但不會顯示任何景象，即使它會顯示在真實世界中也一樣。 右邊的場景會使用與背景色彩相同的霧化色彩來遮蔽範圍，讓多邊形出現淡入距離。 藉由結合離散的霧化效果與創意場景設計，您可以在場景中新增調式和柔化物件的色彩。

Direct3D 提供兩種方式來將霧化新增至場景：圖元霧化和頂點霧化，名為會如何套用霧化效果。 如需詳細資訊，請參閱 [ (direct3d 9 的圖元霧化) ](pixel-fog.md) 和 [ (direct3d 9) 的頂點霧化 ](vertex-fog.md)。 簡言之，圖元霧化（也稱為資料表霧化）會在設備磁碟機中執行，並在 Direct3D 光源引擎中實作為頂點霧化。 應用程式可以使用頂點著色器和圖元霧化（如有需要）來執行霧化。

> [!Note]  
> 無論您是使用圖元或頂點霧化，您的應用程式都必須提供符合規範的投射矩陣，以確保已正確套用霧化效果。 這種限制甚至適用于未使用 Direct3D 轉換和光源引擎的應用程式。 如需如何提供適當矩陣的其他詳細資料，請參閱 [ (Direct3D 9) 的投射轉換 ](projection-transform.md)。

 

下列主題介紹在 Direct3D 應用程式中使用各種霧化功能的霧化和展示資訊。

-   [ (Direct3D 9) 的霧化公式 ](fog-formulas.md)
-   [ (Direct3D 9) 的霧化參數 ](fog-parameters.md)
-   [ (Direct3D 9) 的霧化混色 ](fog-blending.md)
-   [ (Direct3D 9) 的霧化色彩 ](fog-color.md)
-   [ (Direct3D 9) 的頂點霧化 ](vertex-fog.md)
-   [ (Direct3D 9) 的圖元霧化 ](pixel-fog.md)

霧化混色由轉譯狀態控制;它不是可程式化的圖元管線的一部分。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 轉譯](direct3d-rendering.md)
</dt> </dl>

 

 



