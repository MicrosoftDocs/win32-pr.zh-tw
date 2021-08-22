---
title: '載入 (DirectX HLSL 材質物件) '
description: 讀取材質資料，而不進行任何篩選或取樣。
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ba394fb13fd98793401b29e6343ef4fa9ff0194b7a86f22dda1e58439737b34b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119862"
---
# <a name="load-directx-hlsl-texture-object"></a>載入 (DirectX HLSL 材質物件) 

讀取材質資料，而不進行任何篩選或取樣。



<table>
<tbody>
<tr class="odd">
<td>ret 物件。 Load (<dl> typeX 位置，<br />
[typeX SampleIndex, ]<br />
[typeX Offset]<br />
</dl>);</td>
</tr>
</tbody>
</table>

typeX 表示有四種可能的類型： **int**、 **int2**、 **int3** 或 **int4**。

 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*物件*
</dt> <dd>

[材質物件](dx-graphics-hlsl-to-type.md)類型 (除了 TextureCube 或 TextureCubeArray) 之外。

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*位置*
</dt> <dd>

\[在 \] 材質座標中，最後一個元件會指定 mipmap 層級。 這個方法會使用以0為基礎的座標系統，而不是 0.0-1.0 的 UV 系統。 引數類型相依于材質物件類型。



| 物件類型                                  | 參數類型 |
|----------------------------------------------|----------------|
| Buffer                                       | int            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray、材質2D、Texture2DMSArray | int3           |
| Texture2DArray, Texture3D                    | int4           |



 

例如，若要存取2D 材質，請提供前兩個元件的 UV 座標和第三個元件的 mipmap 層級。

> [!Note]  
> 當某個 *位置* 中的一個或多個座標超過材質的 u、v 或 w mipmap 層級維度時， **載入** 會在所有元件中傳回零。 Direct3D 保證可針對任何超出範圍存取的資源傳回零。

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*
</dt> <dd>

\[在 \] 選擇性的取樣索引中。



| 材質類型                                                                                                   | 參數類型 |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D、Texture1DArray、Texture2D、Texture2DArray、Texture3D、Texture2DArray、TextureCube、TextureCubeArray | 不支援  |
| Texture2DMS，Texture2DMSArray ¹                                                                                 | int            |



 

> [!Note]  
> *SampleIndex* 僅適用于多範例紋理。

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*抵消*
</dt> <dd>

\[在 \] 取樣之前套用至材質座標的選擇性位移。 位移類型相依于材質物件類型，而且必須是靜態。



| 材質類型                                             | 參數類型 |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | int            |
| Texture2D、Texture2DArray、Texture2DMS、Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | int3           |



 

> [!Note]  
> 如果您使用 *Offset* 搭配多範例紋理，您也必須指定 *SampleIndex*。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回型別符合 *物件* 宣告中的型別。 例如，宣告為 "Texture2d myTexture;" 的 Texture2D 物件 <uint4> 具有 **uint4** 類型的傳回值。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ¹ | ps \_ 4 \_ 0 | ps \_ 4 \_ 1 ¹ | gs \_ 4 \_ 0 | gs \_ 4 \_ 1 ¹ |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。

## <a name="example"></a>範例

這個部分的程式碼範例是來自[AdvancedParticles 範例](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)中的小畫家 fx 檔案。


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質物件](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




