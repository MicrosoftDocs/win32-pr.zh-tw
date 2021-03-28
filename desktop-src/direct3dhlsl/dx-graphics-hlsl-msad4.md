---
title: msad4
description: 比較4位元組的參考值和8位元組的來源值，並累積4加總的向量。 每個總和都會對應至參考值與來源值之間不同位元組對齊的絕對差異的遮罩總和。
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- msad4 HLSL
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104971856"
---
# <a name="msad4"></a>msad4

比較4位元組的參考值和8位元組的來源值，並累積4加總的向量。 每個總和都會對應至參考值與來源值之間不同位元組對齊的絕對差異的遮罩總和。



| uint4 result = msad4 (uint reference、uint2 source、uint4 accum) ; |
|------------------------------------------------------------------|



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="reference"></span><span id="REFERENCE"></span>*參考*
</dt> <dd>

\[在 \] 一個 **uint** 值中4個位元組的參考陣列中。

</dd> <dt>

<span id="source"></span><span id="SOURCE"></span>*源*
</dt> <dd>

\[在 \] 8 個位元組的來源陣列中，兩個 **uint2** 值。

</dd> <dt>

<span id="accum"></span><span id="ACCUM"></span>*accum*
</dt> <dd>

\[在 \] 4 個值的向量中。 **msad4** 會將這個向量新增至參考值與來源值之間不同位元組對齊的遮罩加總。

</dd> </dl>

## <a name="return-value"></a>傳回值

4加總的向量。 每個總和都對應于參考值與來源值之間不同位元組對齊的遮罩加總。 如果 msad4 的差異是遮罩的，則不會包含總和的差異 (也就是說，參考位元組為 0) 。

## <a name="remarks"></a>備註

若要在您的著色器程式碼中使用 **msad4** 內建，請使用 [**D3D11 \_ FEATURE \_ D3D11 \_ 選項**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature)來呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport)方法，以確認 Direct3D 裝置支援 [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)功能選項。 **Msad4** 內建需要 WDDM 1.2 顯示驅動程式，且所有 WDDM 1.2 顯示器驅動程式都必須支援 **msad4**。 如果您的應用程式使用 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 或11.1 建立轉譯裝置，而且編譯目標為著色器模型5或更新版本，則 HLSL 原始程式碼可以使用 **msad4** 內建。

傳回值的精確度最高為65535。 如果您使用可能導致傳回值大於65535的輸入來呼叫 **msad4** 內建， **msad4** 會產生未定義的結果。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                | 支援 |
|-------------------------------------------------------------|-----------|
| [著色器模型5或更新版本](d3d11-graphics-reference-sm5.md) | 是       |



 

## <a name="examples"></a>範例

以下是 **msad4** 的範例結果計算：


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



以下範例示範如何使用 **msad4** 來搜尋緩衝區內的參考模式：


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>           |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

