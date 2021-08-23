---
title: '範例 (S、float、int、float、uint) 函數 (HLSL 參考) '
description: 使用選擇性的值來取樣 Texture2D，以將範例詳細資料」 LOD () 的值，並傳回作業的狀態。
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
keywords:
- 範例函式 HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 648897a4e2250e0b91544676a3469b2d29402c757bcc77b2285d0181ca2fa5f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986208"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a>範例 (S、float、int、float、uint) 函數 (HLSL 參考) 

使用選擇性的值來取樣 [**Texture2D**](sm5-object-texture2d.md) ，以將範例詳細資料」 lod () 的值，並傳回作業的狀態。

> [!Note]  
> 需要 [著色器型號 5](d3d11-graphics-reference-sm5.md) 或更新版本。

 

## <a name="syntax"></a>語法

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
);
```

## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的 S\]
</dt> <dd>

[取樣器狀態](dx-graphics-hlsl-sampler.md)。 這是在包含狀態指派的效果檔案中宣告的物件。

</dd> <dt>

*位置* \[在\]
</dt> <dd>

材質座標。 引數類型相依于材質物件類型。



| Texture-Object 類型                    | 參數類型 |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray、Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*位移* \[在\]
</dt> <dd>

選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。 材質位移必須是靜態的。 引數類型相依于材質物件類型。 如需詳細資訊，請參閱套用 [材質座標位移](dx-graphics-hlsl-to-sample.md)。



| Texture-Object 類型           | 參數類型 |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D、Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | 不支援  |



 

</dd> <dt>

*夾具* \[在\]
</dt> <dd>

用來將範例」 LOD 值設為的選擇性值。 例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。

</dd> <dt>

*狀態* \[擴展\]
</dt> <dd>

作業的狀態。 您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。 如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。 如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。

## <a name="remarks"></a>備註

紋理取樣會使用材質位置來查閱材質值。 位移可以套用到查閱之前的位置。 取樣器狀態包含取樣和篩選選項。 這個方法可以在圖元著色器中叫用，但在頂點著色器或幾何著色器中不支援。

只在整數 miplevel 使用位移;否則，您可能會根據硬體的執行或驅動程式設定取得不同的結果。

### <a name="calculating-texel-positions"></a>計算材質位置

材質座標是參考紋理資料的浮點值，也稱為標準化材質空間。 位址換行模式會依此順序套用 (材質座標 + 位移 + 換行模式) 來修改 \[ 0 ... 1 範圍以外的材質座標。 \]

針對材質陣列，location 參數中的額外值會指定紋理陣列中的索引。 此索引會被視為調整的浮點值 (而不是標準材質座標) 的正規化空間。 整數索引的轉換是以下列順序完成， (float + 四捨五入至最接近的陣列範圍) ，甚至是整數 + 夾具。

### <a name="applying-texture-coordinate-offsets"></a>套用材質座標位移

Offset 參數會修改材質空間中的材質座標。 雖然材質座標是正規化浮點數，但位移會套用整數位移。 另請注意，材質位移必須是靜態的。

傳回的資料格式取決於材質格式。 例如，如果紋理資源是以 DXGI \_ 格式 \_ A8B8G8R8 \_ UNORM SRGB 格式所定義 \_ ，則取樣作業會將取樣的材質從 gamma 2.0 轉換為1.0、篩選，並將結果以浮點數形式寫入範圍 \[ 0 ..1 \] 。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範例方法](texture-sample-overload.md)
</dt> <dt>

[材質物件](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
