---
title: RWTexture2D
description: 讀取/寫入資源。 |RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322164"
---
# <a name="rwtexture2d"></a>RWTexture2D

讀取/寫入資源。



| 方法                                                        | 描述                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | 取得資源維度。 |
| [**載入**](rwtexture2d-load.md)                              | 讀取紋理資料。           |
| [**運算子\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | 取得資源變數。     |



 

您可以在 RWTexture2D 物件前面加上儲存類別 **globallycoherent**。 此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。 如果沒有這個規範，記憶體屏障或同步將只會清除未排序的存取視圖， (UAV) 在目前群組中。

RWTexture2D 物件需要物件的宣告語句中的元素類型。 例如，下列宣告不正確：


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



下列宣告是正確的：


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



由於 RWTexture2D 物件是 UAV 類型的物件，因此它的屬性與著色器資源檢視不同 (SRV) 型別物件，例如 [Texture2D](sm5-object-texture2d.md) 物件。 例如，您可以讀取和寫入 RWTexture2D 物件，但只能從 Texture2D 物件讀取。

RWTexture2D 物件無法使用來自 [Texture2D](sm5-object-texture2d.md) 物件的方法，例如 [範例](dx-graphics-hlsl-to-sample.md)。 不過，因為您可以為相同的資源建立多個檢視類型，所以您可以將多個紋理類型宣告為多個著色器中的單一材質。 例如，下列程式碼片段會示範如何在計算著色器中宣告和使用 RWTexture2D 物件做為 *tex* ，然後在圖元著色器中宣告並使用 Texture2D 物件做為 *tex* 。

> [!Note]  
> 當您在相同的資源中建立多個檢視類型時，執行時間會強制執行特定的使用模式。 例如，執行時間不允許您同時讓相同資源的資源和 SRV 對應的 UAV 對應同時啟用。

 

下列程式碼適用于計算著色器：


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



下列程式碼適用于圖元著色器：


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此物件：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




