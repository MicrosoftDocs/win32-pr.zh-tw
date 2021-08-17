---
description: Direct3D 燈光模型涵蓋環境、擴散、反射及發光。
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: " (Direct3D 9) 的照明數學"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1c6ffa8a1142c1be40993dcd8130b4708f2b509c8a5a1f05e234d0231c3bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728333"
---
# <a name="mathematics-of-lighting-direct3d-9"></a> (Direct3D 9) 的照明數學

Direct3D 燈光模型涵蓋環境、擴散、反射及發光。 這個範圍足以因應大範圍的照明情況。 您可以參考場景中的光線總數量作為全球照明，然後使用下列方程式來計算。


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



[環境光源 (Direct3D 9) ](ambient-lighting.md) 是固定光源。 它在所有方向都是固定的，而且會以相同的方式將物件的所有圖元色彩。 加以計算很快速，但是會讓物件看起來很平板且不真實。 若要瞭解 Direct3D 如何計算環境光源，請參閱 (Direct3D 9) 的環境光源。

[擴散光源 (Direct3D 9) ](diffuse-lighting.md) 取決於光線方向和物件介面正常。 它會因變化光線方向和變化的 surface 數位向量而在物件的表面上有所不同。 計算擴散光源需要較長時間，因為它改變每個物件頂點，不過使用它的優點是它會遮蔽物件，並提供物件三維 (3D) 深度。 若要查看如何在 Direct3D 中計算擴散光源，請參閱 (Direct3D 9) 的擴散光源。

[ (Direct3D 9 的反射光源) ](specular-lighting.md) 識別光碰到物件介面並反映到相機上時所發生的明亮高光。 它比擴散燈更密集，並且在物件介面上更快速地下降。 反射光源比擴散光源需要較長的時間計算，但是使用它的優點是它在物件表面上新增重要細節。 若要瞭解如何在 Direct3D 中計算反射光源，請參閱 (Direct3D 9) 的反射光源。

[放射光源 (Direct3D 9) ](emissive-lighting.md) 是由物件發出的淺色;例如，發光。 若要查看如何在 Direct3D 中計算放射光源，請參閱放射光源 (Direct3D 9) 。

可藉由運用每一種類型的光源至 3D 場景來成就實際光源。 計算環境、放射，擴散元件的值會輸出為擴散頂點色彩，而反射光源元件的值則輸出為反射頂點色彩。 環境、擴散及反射光線值可能受到指定光線衰減和聚光燈係數的影響。 如需衰減運作方式的詳細資訊，請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。

若要完成更多實際照明效果，您可以新增更多光線，不過場景會花較長的時間來呈現。 若要取得所有效果設計師的想法，某些遊戲使用比一般常用者更多的 CPU 功率。 若是如此，通常會將照明計算數目減到最小值，方法是在使用材質貼圖的同時，使用光照貼圖和環境貼圖將光源引入場景。

在相機空間計算光源。 若要查看如何計算光源轉換，請參閱 [ (Direct3D 9) 的相機空間轉換 ](camera-space-transformations.md)。 當特殊條件存在時，可在模型空間中計算優化光源：已正規化標準向量 (D3DRS \_ NORMALIZENORMALS 為 True) 、不需要頂點混色、轉換矩陣為正向等。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[燈光和材質](lights-and-materials.md)
</dt> </dl>

 

 



