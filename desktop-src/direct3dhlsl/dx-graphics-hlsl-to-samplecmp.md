---
title: 'SampleCmp (DirectX HLSL 材質物件) '
description: 針對材質進行紋理取樣，並將單一元件與指定的比較值進行比較。
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a606ad9081f1ca1fdc4261d862ea6edfef4460989bb6d51d839d85f5797c1466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854638"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>SampleCmp (DirectX HLSL 材質物件) 

針對材質進行紋理取樣，並將單一元件與指定的比較值進行比較。

<table>
<tbody>
<tr class="odd">
<td>float 物件. SampleCmp ( <dl> SamplerComparisonState S、<br />
float 位置、<br />
float CompareValue、<br />
[int Offset]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

比較是材質中儲存的第一個元件與方法中所傳遞的比較值之間的單一元件比較。

這個方法只能從圖元著色器叫用;頂點或幾何著色器不支援此功能。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*物件*
</dt> <dd>

任何 [材質物件](dx-graphics-hlsl-to-type.md) 類型 (除了 Texture2DMS、Texture2DMSArray 或 Texture3D) 之外。

</dd> <dt>

<span id="S"></span><span id="s"></span>*！*
</dt> <dd>

\[在 \] 取樣器的比較狀態中，也就是取樣器狀態加上比較狀態 (比較函數和比較篩選) 。 如需詳細資訊和範例，請參閱 [取樣器類型](dx-graphics-hlsl-sampler.md) 。

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*位置*
</dt> <dd>

\[在 \] 紋理座標中。 引數類型相依于材質物件類型。

| Texture-Object 類型          | 參數類型 |
|------------------------------|----------------|
| Texture1D                    | FLOAT          |
| Texture1DArray、Texture2D    | float2         |
| Texture2DArray ¹，TextureCube | float3         |
| TextureCubeArray ¹            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

用來作為比較值的浮點值。

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*抵消*
</dt> <dd>

\[在 \] 選擇性的材質座標位移中（可用於任何材質物件類型）; 位移會套用至取樣之前的位置。 材質位移必須是靜態的。 引數類型相依于材質物件類型。 如需詳細資訊，請參閱套用 [材質座標位移](dx-graphics-hlsl-to-sample.md)。

| Texture-Object 類型            | 參數類型 |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | int            |
| Texture2D，Texture2DArray ¹     | int2           |
| TextureCube，TextureCubeArray ¹ | 不支援  |

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回範圍 0 ..1 中的浮點值。 \[ \]

針對每個根據篩選模式) 的取樣器設定取得 (的材質， **SampleCmp** 會根據材質值（如果比較成功，從著色器針對值 (1），執行 z 值 (第三個) 元件的比較。否則為 0) 。 然後， **SampleCmp** 會將每個材質的這0和1個結果混合成一般材質篩選 (不是平均) ，並將產生的 \[ 0 ..1 \] 值傳回給著色器。

## <a name="remarks"></a>備註

比較篩選會提供基本的篩選作業，適用于百分比深度的篩選。

在浮點資源上使用這個方法時 (而非經過簽署的正規化或不帶正負號標準化) 格式時，不會自動在0.0 和1.0 之間壓制比較值。 因此，常見的遮蔽技術可能需要比較值的手動夾具。

只在整數 miplevel 使用位移;否則，您可能會根據硬體的執行或驅動程式設定取得不同的結果。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ² | ps \_ 4 \_ 0 | ps \_ 4 \_ 1 ² | gs \_ 4 \_ 0 | gs \_ 4 \_ 1 ² |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x ¹       | x         |          |           |

1.  Texture2DArray 和 TextureCubeArray 適用于著色器模型4.1 或更高版本。
2.  在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。

> [!NOTE]  
>  \_ \_ \_ \_ \_ \_ \_ \_ 當您使用在[Direct3D 功能層級9中執行陰影緩衝區](/previous-versions/windows/apps/jj262110(v=win.10))時所述的技術，也可以在 ps 4 0 層級 9 1 和 4 0 層級 9 3 中使用 SampleCmp。

## <a name="related-topics"></a>相關主題

[材質物件](dx-graphics-hlsl-to-type.md)
