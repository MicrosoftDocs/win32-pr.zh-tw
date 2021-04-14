---
description: 材質描述多邊形如何反映燈光，或看似在3D 場景中發出燈光。
ms.assetid: vs|directx_sdk|~\materials.htm
title: Direct3D 9) 的教材 (
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104552269"
---
# <a name="materials-direct3d-9"></a>Direct3D 9) 的教材 (

材質描述多邊形如何反映燈光，或看似在3D 場景中發出燈光。 材質屬性會詳細說明材質的擴散反映、環境反映、光線排放和高光特性。 Direct3D 會使用 [**D3DMATERIAL9**](d3dmaterial9.md) 結構來攜帶所有材質屬性資訊。 除了反射屬性之外，每個屬性都會描述為 RGBA 色彩，其代表指定之光線類型的紅色、綠色和藍色部分，以及 Alpha 混色因數。

## <a name="diffuse-and-ambient-reflection"></a>擴散和環境反映

[**D3DMATERIAL9**](d3dmaterial9.md)結構的擴散和環境成員會描述材質如何反映場景中的環境和擴散燈。 因為大部分的場景所包含的擴散速度遠高於環境光線，所以擴散反映在決定色彩方面扮演最大的部分。 此外，由於擴散燈的方向，擴散光的發生角度會影響反映的整體濃度。 當光線將頂點平行至頂點正常時，擴散反映會很大。 當角度增加時，擴散反映的效果會降低。 反射的光線量是連入燈光與頂點法線之間的角度余弦值，如下圖所示。

![反映的光線量圖](images/incident.png)

環境反映（像是環境燈）是 nondirectional。 環境反映對轉譯物件的明顯色彩會有較小的影響，但它會影響整體的色彩，而且在輕微或無擴散光線反映材質時，最明顯。 使用 D3DRS 環境旗標呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，以針對場景的環境光源來影響材質的環境反映 \_ 。

擴散和環境反映會一起運作，以判斷物件的已知色彩，且通常是相同的值。 例如，若要轉譯藍色 crystalline 物件，您可以建立只反映擴散和環境光源之藍色元件的材質。 放在具有白色燈光的房間時，crystal 會顯示為藍色。 不過，在只有紅色光的房間內，相同的 crystal 會顯示為黑色，因為它的材質不會反映紅色光源。

## <a name="emission"></a>排放

材質可以用來讓轉譯的物件看似自我 luminous。 [**D3DMATERIAL9**](d3dmaterial9.md)結構的放射成員是用來描述已發出光源的色彩和透明度。 放射會影響物件的色彩，例如讓深色材質更亮，並呈現部分的發出色彩。

您可以使用材質的放射屬性來新增物件發出光線的假像，而不會造成將燈光新增至場景的計算額外負荷。 在 blue crystal 的情況下，如果您想要讓 crystal 看起來很亮，而不是在場景中的其他物件上轉換燈光，放射屬性就很有用。 請記住，具有放射屬性的材質不會發出可由場景中其他物件反映的燈。 若要達到這種反映的光線，您需要在場景內放置額外的燈。

## <a name="specular-reflection"></a>反射反映

反射反映會在物件上建立醒目顯示，讓它們看起來很亮。 [**D3DMATERIAL9**](d3dmaterial9.md)結構包含兩個成員，這些成員描述反射反白顯示色彩以及材質的整體反光。 您可以藉由將反射成員設定為所需的 RGBA 色彩來建立高光的色彩-最常見的色彩為白色或淺灰色。 您在 Power 成員中設定的值會控制反射效果的清晰程度。

高光可能會產生顯著的效果。 在藍色 crystal 上再次繪圖：較大的功率值會建立更清晰的高光，讓 crystal 看似相當亮。 較小的值會增加效果的面積，建立讓 crystal 外觀 frosty 的單調反映。 若要將物件設為真正的遮罩，請將 Power 成員設定為零，並將高光中的色彩設定為黑色。 試驗不同層級的反映，以針對您的需求產生實際的外觀。 下圖顯示兩個相同的模型。 左邊的一個會使用10的反射反映乘冪;右邊的模型沒有反射反映。

![反射反映模型的圖例](images/spechigh.png)

## <a name="setting-material-properties"></a>設定材質屬性

Direct3D 轉譯裝置一次只能使用一組材質屬性來呈現。

在 c + + 應用程式中，您可以藉由準備 [**D3DMATERIAL9**](d3dmaterial9.md) 結構，然後呼叫 [**IDirect3DDevice9：： SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) 方法，來設定系統所使用的材質屬性。

若要準備要使用的 [**D3DMATERIAL9**](d3dmaterial9.md) 結構，請設定結構中的屬性資訊，以在轉譯期間建立所要的效果。 下列程式碼範例會為紫色材質設定有清晰白色高光的 **D3DMATERIAL9** 結構。


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



準備 [**D3DMATERIAL9**](d3dmaterial9.md) 結構之後，您可以藉由呼叫轉譯裝置的 [**IDirect3DDevice9：： SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) 方法來套用屬性。 這個方法會接受備妥 **D3DMATERIAL9** 結構的位址做為其唯一的參數。 您可以視需要使用新的資訊來呼叫 **IDirect3DDevice9：： SetMaterial** ，以更新裝置的材質屬性。 下列程式碼範例顯示如何在程式碼中查看。


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



當您建立 Direct3D 裝置時，會自動將目前的材質設定為下表所示的預設值。



| 成員   | 值                |
|----------|----------------------|
| 擴散  |  (R:0、G:0、B:0、A:0)  |
| 反射 |  (R:0、G:0、B:0、A:0)  |
| 環境  |  (R:0、G:0、B:0、A:0)  |
| 放射 |  (R:0、G:0、B:0、A:0)  |
| 電源    |  (0.0)                 |



 

## <a name="retrieving-material-properties"></a>正在抓取材質屬性

您可以藉由呼叫裝置的 [**IDirect3DDevice9：： GetMaterial**](/windows/desktop/api) 方法，來取出轉譯裝置目前所使用的材質屬性。 不同于 [**IDirect3DDevice9：： SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) 方法， **IDirect3DDevice9：： GetMaterial** 不需要準備。 **IDirect3DDevice9：： GetMaterial** 方法接受 [**D3DMATERIAL9**](d3dmaterial9.md)結構的位址，並在傳回之前，以描述目前材質屬性的資訊填入提供的結構。


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> 如果您的應用程式未指定用於轉譯的材質屬性，系統就會使用預設的材質。 預設材質會反映所有的擴散淺白色，例如，沒有環境或反射反映，而且沒有放射色彩。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[燈光和材質](lights-and-materials.md)
</dt> </dl>

 

 
