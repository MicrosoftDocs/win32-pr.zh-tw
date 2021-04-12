---
description: 淺色屬性描述燈光來源的型別和色彩。
ms.assetid: b39f1287-c67b-4cbb-b599-4a1b2f4981ac
title: " (Direct3D 9) 的燈光屬性"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63239024109327e483ff93c2ee29fe42fc22c922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108841"
---
# <a name="light-properties-direct3d-9"></a> (Direct3D 9) 的燈光屬性

淺色屬性描述燈光來源的型別和色彩。 根據使用的光線類型，光線可有衰減和範圍或聚光燈特效屬性。 但是，並非所有類型的燈光都會使用所有屬性。 Direct3D 會使用 [**D3DLIGHT9**](d3dlight9.md) 結構，針對所有類型的燈光來源攜帶燈光屬性的相關資訊。 本節包含所有淺色屬性的資訊。 資訊分成下列群組。

位置、範圍及衰減屬性定義現世空間裡的照明位置，並且定義如何經由距離發出光線的行為。 如同您在 c + + 中使用的所有 light 屬性，這些屬性都包含在光線的 [**D3DLIGHT9**](d3dlight9.md) 結構中。

-   [淺色衰減](#light-attenuation)
-   [淺色色彩](#light-color)
-   [光方向](#light-direction)
-   [光線位置](#light-position)
-   [淺色範圍](#light-range)

## <a name="light-attenuation"></a>光線衰減

衰減控制光線強度如何隨著範圍屬性指定的最大距離減少。 三個 [**D3DLIGHT9**](d3dlight9.md) 結構成員代表淺衰減： Attenuation0、Attenuation1 和 Attenuation2。 這些成員包含浮點值範圍從0.0 到無限大，控制光線衰減。 某些應用程式設定 Attenuation1 成員至 1.0，其他成員至 0.0，導致光線強度變更為 1 / D，其中 D 是光源到頂點的距離。 最大光線強度在於來源，在光線的距離減至 1 (光線範圍)。 一般而言，應用程式會將 Attenuation0 設定為0.0、Attenuation1 為常數值，並 Attenuation2 至0.0。

您可以合併衰減值，以獲得更複雜的衰減效果。 或者可將這些值設為一般範圍以外的值，以建立更怪異的衰減效果。 但不接受負衰減值。 請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。

## <a name="light-color"></a>淺色

在 Direct3D 光線發出三種顏色，其在系統照明運算中各自獨立運用︰ 擴散色彩、環境色彩及反射色彩。 每個由 Direct3D 結合在一起的照明模組，與目前材質對應互動，以製作轉譯中使用的最後色彩。 擴散色彩與目前材質的擴散反射率屬性互動，反射色彩與材質反射的反射率屬性互動，依此類推。 如需 Direct3D 如何套用這些色彩的詳細資訊，請參閱 [ (Direct3D 9 的照明數學) ](mathematics-of-lighting.md)。

在 c + + 應用程式中， [**D3DLIGHT9**](d3dlight9.md) 結構包含三個這些色彩的成員-擴散、環境和反射-每個成員都是一個 [**D3DCOLORVALUE**](d3dcolorvalue.md) 結構，可定義所發出的色彩。

最常運用系統運算的色彩類型是擴散色彩。 最常見的擴散色彩為白色 (R:1.0 G:1.0 B:1.0)，但是您可以依需求建立色彩來達到所需的效果。 例如，壁爐可以使用紅光，或者也可以將交通號誌的綠燈設定為「執行」(Go)。

一般而言，您將淺色元件值設定為 0.0 到 1.0 (含) 之間，但這不是必需。 例如，您可能會將所有元件設為 2.0，建立比白色亮的光線。 這類設定在您使用衰減常數以外的設定時尤其管用。

請注意，雖然 Direct3D 針對燈光使用 RGBA 值，但不會使用 Alpha 色彩元件。

通常會使用照明材質色彩。 不過，您可以指定材質發色、環境、擴散及反射是由擴散或反射頂點色彩覆寫。 這是藉由呼叫 [**graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) ，並設定下表所列的裝置狀態變數來完成。



| 裝置狀態變數         | 意義                                       | 類型                   | 預設          |
|-------------------------------|-----------------------------------------------|------------------------|------------------|
| D3DRS \_ AMBIENTMATERIALSOURCE  | 定義要取得環境材質色彩的位置。  | D3DMATERIALCOLORSOURCE | D3DMCS \_ 材質 |
| D3DRS \_ DIFFUSEMATERIALSOURCE  | 定義要取得擴散材質色彩的位置。  | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR1   |
| D3DRS \_ SPECULARMATERIALSOURCE | 定義要取得反射材質色彩的位置。 | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR2   |
| D3DRS \_ EMISSIVEMATERIALSOURCE | 定義取得放射材質色彩的位置。 | D3DMATERIALCOLORSOURCE | D3DMCS \_ 材質 |
| D3DRS \_ COLORVERTEX            | 停用或啟用頂點色彩的使用。     | BOOL                   | true             |



 

Alpha/透明度值永遠只來自擴散色彩 alpha 色板。

霧值永遠只來自反射色彩 alpha 色板。

D3DMATERIALCOLORSOURCE 可以具有下列值。

-   D3DMCS \_ 材質材質會用來作為來源。
-   D3DMCS \_ COLOR1-使用擴散頂點色彩作為來源。
-   D3DMCS \_ COLOR2-反射頂點色彩可作為來源。

## <a name="light-direction"></a>光方向

光方向屬性決定了移動物件在自然空間發出的光方向。 方向只由方向燈和聚光燈使用，而且只用向量描述。

在光線的 [**D3DLIGHT9**](d3dlight9.md) 結構的方向成員中設定燈光方向。 方向成員的類型為 [**D3DVECTOR**](d3dvector.md)。 無論場景中的光線位置為何，從邏輯原點描述方向向量為距離。 因此，直接指向場景的焦點（沿著正 Z 軸）的方向向量為 <0、0、1> 無論其位置定義的位置為何。 同樣地，您可以使用方向為 <0，-1，0> 的方向光線，直接在場景上模擬陽光照明。 很明顯地，您不需要建立沿著座標軸的燈光，您可以混合和比對值，以建立可深入瞭解更有趣角度的燈光。

> [!Note]  
> 雖然您不需要將光線方向向量正常化，您隨時都確定它的級數。 換句話說，請勿使用 <0、0、0> 方向向量。

 

## <a name="light-position"></a>光線位置

光源的描述是在 [**D3DLIGHT9**](d3dlight9.md)結構的 position 成員中使用 [**D3DVECTOR**](d3dvector.md)結構。 X、y 和 z 座標會假設在世界空間中。 方向燈是唯一不使用位置屬性的光線類型。

## <a name="light-range"></a>光線範圍

光線範圍屬性決定自然空間中的距離，而場景中網狀結構在此距離不會再接收該物件發出的光線。 範圍成員包含浮點值，代表光線最大範圍，在世界空間中。 方向燈不使用範圍屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[燈光和材質](lights-and-materials.md)
</dt> </dl>

 

 
