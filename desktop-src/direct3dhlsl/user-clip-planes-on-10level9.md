---
title: 功能等級9硬體上的使用者剪輯平面
description: 從 Windows 8 開始，Microsoft 高階著色器語言 (HLSL) 支援可搭配 Microsoft Direct3D 11 API 使用的語法，以在功能層級 9 \_ x 和更高版本上指定使用者剪輯平面。
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315571"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a>功能等級9硬體上的使用者剪輯平面

從 Windows 8 開始，Microsoft 高階著色器語言 (HLSL) 支援可搭配 Microsoft Direct3D 11 API 使用的語法，以在 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x 和更高版本上指定使用者剪輯平面。 您可以使用這個剪切平面語法來寫入著色器，然後使用該著色器物件搭配 Direct3D 11 API，以在所有 Direct3D 功能層級上執行。

-   [背景](#background-reading)
-   [語法](#syntax)
-   [在功能層級9和更高的剪輯空間中建立剪輯平面](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [背景讀取](#background-reading)
    -   [10Level9 功能等級](#10level9-feature-levels)
    -   [裁剪平面數學](#clip-plane-math)
    -   [在視圖空間中裁剪](#clipping-in-view-space)
    -   [投射矩陣](#projection-matrix)
    -   [剪輯空間裁剪平面](#clip-space-clip-plane)
-   [相關主題](#related-topics)

## <a name="background"></a>背景

您可以透過 [**IDirect3DDevice9：： SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) 和 [**IDirect3DDevice9：： GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) 方法，在 Microsoft Direct3D 9 API 中存取使用者剪輯平面。 在 Microsoft Direct3D 10 和更新版本中，您可以透過 [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) 語義來存取使用者剪輯平面。 但在 Windows 8 之前， \_ direct3d 10 或 direct3d 11 api 中的 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 x 硬體無法使用 SV ClipDistance \_ 。 因此，在 Windows 8 之前，使用功能層級 9 x 硬體來存取使用者剪輯平面的唯一方法 \_ 是透過 Direct3D 9 API。 Direct3D Windows Store 應用程式無法使用 Direct3D 9 API。 在這裡，我們將說明您可以在功能層級 9 \_ x 和更高版本上透過 Direct3D 11 API 存取使用者剪輯平面的語法。

應用程式會使用「剪輯」平面來定義3D 世界內的一組隱藏的平面， (擲出) 所有繪製的基本專案。 Windows 不會繪製任何裁剪平面之負角的任何圖元。 然後，應用程式可以使用剪輯平面來呈現平面反射。

## <a name="syntax"></a>Syntax

使用此語法可將剪輯平面宣告為 [函式宣告](dx-graphics-hlsl-function-syntax.md)中的函式屬性。 例如，我們在這裡使用頂點著色器片段上的語法：

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

這是頂點著色器片段的範例，表示兩個裁剪平面。 它會顯示您需要將新的 **clipplanes** 屬性放在括弧內的括弧內，緊接在頂點著色器的傳回值之前。 在 **clipplanes** 屬性之後的括弧內，您可以提供最多6個 **float4** 常數的清單，以定義每個使用中剪輯平面的平面係數。 此範例也顯示您需要讓每個平面的係數都位於常數緩衝區中。

> [!Note]  
> 沒有可動態停用剪切平面的語法。 您必須重新編譯沒有 **clipplanes** 屬性的另一個相同著色器，否則您的應用程式可以將常數緩衝區中的係數設定為零，如此平面就不會再影響任何幾何。

 

此語法適用于任何4.0 或更新版本的頂點著色器目標，其中包括 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1 和 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 3。

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a>在功能層級9和更高的剪輯空間中建立剪輯平面

在這裡，我們將示範如何在 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x 和更高的剪輯空間中建立剪輯平面。

### <a name="background-reading"></a>背景讀取

「使用 DirectX 10 進行3D 遊戲程式設計簡介」。 Luna 將說明您需要的圖形數學背景 (第1、2和 3) ，以及在頂點著色器中發生的各種空間和空間轉換 (區段5.6 和 5.8) 。

### <a name="10level9-feature-levels"></a>10Level9 功能等級

在 Direct3D 10 和更新版本中，您可以裁剪任何有意義的空間，通常是在世界空間或視野空間中。 但是，Direct3D 9 會使用剪輯空間，也就是在分割投影空間之前的觀點。 當頂點著色器將這些向量傳遞給 [圖形管線](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline)中後續的階段時，它們會在剪輯空間中。

當您撰寫 Windows Store 應用程式時，您必須使用10Level9 功能等級 ([功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) ，讓應用程式可以在功能層級 9 \_ x 和更高的硬體上執行。 因為您的應用程式支援功能層級 9 \_ x 和更高版本，所以您也必須使用在剪輯空間中套用剪輯平面的一般功能。

當您使用 vs \_ 4 \_ 0 \_ 層級 9 1 或更新版本來編譯頂點著色器時 \_ \_ ，該頂點著色器可以使用 **clipplanes** 屬性。 Direct3D 10 或更新版本的物件具有發出頂點的點乘積，其中包含屬性中指定的每個 **float4** 全域常數。 Direct3D 9 物件有足夠的中繼資料，可讓10Level9 執行時間發出適當的 [**IDirect3DDevice9：： SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane)呼叫。

### <a name="clip-plane-math"></a>裁剪平面數學

剪輯平面是由具有4個元件的向量所定義。 前三個元件會定義 x、y、z 向量，以從我們想要裁剪的空間中的原點 emanates。 此向量表示平面，垂直至向量並透過原點執行。 Windows 會將所有圖元保留在平面的向量端，並將所有圖元剪到平面後方。 第四個元件會將平面推回，並讓 Windows 更少 (負面 w 會導致視窗沿著向量線裁剪更) 。 如果 x、y、z 元件 (正規化) 向量來撰寫一個單位，則會將平面推回的平面。

圖形處理器 (GPU) 執行以判斷裁剪的數學，是頂點向量 (x、y、z、1) 和裁剪平面向量之間的簡單點乘積。 此數學運算會在裁剪平面向量上建立投射長度。 負點產品會顯示要在平面裁剪端的頂點。

### <a name="clipping-in-view-space"></a>在視圖空間中裁剪

以下是視圖空間中的頂點：

![視圖空間中的頂點](images/vertex-clip.png)

以下是我們在視野空間中的剪輯平面：

![視圖空間中的剪切平面](images/clip-plane-view.png)

以下是頂點的點乘積和查看空間中的剪切平面：

ClipDistance = **v** ·**C**  = *v* ₓ *C* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>

此數學運算適用于 Direct3D 10 或更新版本的物件，但不適用於 Direct3D 9 物件。 針對 Direct3D 9，我們必須先在剪輯空間中進行投影轉換。

### <a name="projection-matrix"></a>投射矩陣

投射矩陣會將頂點從 view space 轉換 (其中原點是檢視器的眼睛、+ x 朝右、+ y 已啟動，而 + z 則是直接) 在剪輯空間中。 投射矩陣準備硬體裁剪和 [點陣化階段](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage)的頂點。 以下是標準的透視圖矩陣 (其他投射需要不同的數學) ：

<dl>    視窗寬度/高度的 r 比例  
*α*   視圖角度  
   從檢視器到目前平面的 f 距離  
   從檢視器到接近平面的距離
</dl>![投射矩陣](images/projection-matrix.png)

下一個矩陣是前一個矩陣的簡化版本。 我們會將矩陣簡化，讓我們可以在稍後的矩陣乘法運算中使用。

![簡化的投射矩陣](images/projection-matrix2.png)

現在，我們將 view space 頂點轉換成具有矩陣乘積的剪切空間：

![矩陣相乘](images/matrix-multiply.png)

在我們的矩陣乘法運算中，我們的 x 和 y 元件只會稍微調整，但 z 和 w 元件的變化很大。 我們的剪輯平面無法提供我們所需的其他資訊。

### <a name="clip-space-clip-plane"></a>剪輯空間裁剪平面

在這裡，我們想要建立一個具有剪輯空間頂點的點乘積的剪輯空間裁剪平面，讓我們擁有與 v ·相同的值。 在 [[查看空間](#clipping-in-view-space)] 區段的剪切中的 C。

![裁剪平面](images/clip-space-clip-plane.png)

**v** ·**C**  = **v P** ·**C**<sub>P</sub>

*v* ₓ *C* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>c w v y v z c z c  +  ** <sub>w</sub>  =  *v* ₓ *P* ₓ *C*<sub>p ₓ</sub>  + *v*<sub>y</sub>*p*<sub>y</sub>*c*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub>z</sub></sub>  +  *BC*<sub>P <sub>z</sub></sub>  +  *v*<sub>z</sub>z *c*<sub>p <sub>w</sub></sub>

現在我們可以將頂點元件的前面數學運算分成四個不同的方程式：

![剪輯平面產品的 x 頂點元件](images/clip-space-clip-plane-equ1.png)

![剪輯平面產品的 y 頂點元件](images/clip-space-clip-plane-equ2.png)

![剪輯平面產品的 w 頂點元件](images/clip-space-clip-plane-equ3.png)

![剪切平面產品的 z 頂點元件](images/clip-space-clip-plane-equ4.png)

我們的視圖空間裁剪平面和投射矩陣會衍生出來，並為我們提供剪輯空間裁剪平面。

![剪輯空間裁剪平面](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[函式宣告語法](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 