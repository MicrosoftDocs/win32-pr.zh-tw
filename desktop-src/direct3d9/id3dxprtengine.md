---
description: ID3DXPRTEngine 介面可用來計算預先計算 radiance 傳輸 (PRT) 模擬。 其方法通常會離線使用，以計算即時3D 模型化的每個頂點或每個材質傳輸向量。
ms.assetid: d5be657f-2b0c-48fd-a7f0-ddb90107772f
title: 'ID3DXPRTEngine 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bef527f9044c01b0696e86b44ddaef7ec72c336771ed136ddd071d11c0d73836
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293352"
---
# <a name="id3dxprtengine-interface"></a>ID3DXPRTEngine 介面

ID3DXPRTEngine 介面可用來計算預先計算 radiance 傳輸 (PRT) 模擬。 其方法通常會離線使用，以計算即時3D 模型化的每個頂點或每個材質傳輸向量。

## <a name="members"></a>成員

**ID3DXPRTEngine** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXPRTEngine** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXPRTEngine** 介面具有這些方法。



| 方法                                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)                       | 在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。 如果找到交集，方法會傳回最接近之網格臉部的索引，以及交集點的 barycentric 座標。<br/>                                                                                                                                                                                |
| [**ComputeBounce**](id3dxprtengine--computebounce.md)                                     | 計算 interreflected 燈的單一彈跳所產生的來源 radiance。 此方法可用於任何照明的場景，包括球面調和 (SH) 為基礎的預先計算 radiance 傳輸 (PRT) 模型。<br/>                                                                                                                                                                                                                                                    |
| [**ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)                     | 使用調適型取樣來計算由單一 interreflected 燈彈跳產生的來源 radiance。 這個方法會在網格上產生新的頂點和臉部，以更精確地近似預先計算 radiance 傳輸 (PRT) 信號。 此方法可用於任何照明的場景，包括球形調和 (SH) 為基礎的 PRT 模型。<br/>                                                                                                                   |
| [**ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)                 | 計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。<br/>                                                                                                                                                                                                                                                                                                                            |
| [**ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) | 使用調適型取樣，計算以球面調和 (SH) 近似值表示之3D 物件的直接光源比重。 這個方法會在網格上產生新的頂點和臉部，以更精確地近似預先計算 radiance 傳輸 (PRT) 信號。<br/>                                                                                                                                                           |
| [**ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md)           | 使用 GPU 來計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。 計算 GPU 的照明通常會比 CPU 更快。<br/>                                                                                                                                                                                                                            |
| [**ComputeLDPRTCoeffs**](id3dxprtengine--computeldprtcoeffs.md)                           | 計算本地 deformable 預先計算 radiance 傳輸 (LDPRT 相對於每個樣本一般向量的) 係數，以將輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 資料的最小平方誤差降至最低。 這些係數可搭配 skinned 或轉換的一般向量使用，以在動態物件上建立全域效果的模型。<br/>                                                                                                                     |
| [**ComputeSS**](id3dxprtengine--computess.md)                                             | 使用 [**ID3DXPRTEngine：： SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)設定的材質屬性，計算地下散佈所產生的來源 radiance。 這個方法僅適用于網格物件中每個頂點定義的材質。<br/>                                                                                                                                                                                                       |
| [**ComputeSSAdaptive**](id3dxprtengine--computessadaptive.md)                             | 計算使用 [**ID3DXPRTEngine：： SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)所設定的調適型取樣和材質屬性，將來源 radiance 對應至地下散佈所產生之結束 radiance 的傳輸向量。 方法會在網格上產生新的頂點和臉部，以更精確地近似預先計算 radiance 傳輸 (PRT) 信號。 這個方法僅適用于網格物件中每個頂點定義的材質。<br/> |
| [**ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)               | 針對任意點 (和一般向量) 計算預先計算 radiance 傳輸 (PRT) 範例。<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)           | 計算，在不在網格上的任意時間點，對應來源 radiance (由球面調和表示的傳輸向量 (SH) 近似值) 結束 radiance。<br/>                                                                                                                                                                                                                                                                                                   |
| [**ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)                       | 計算上一個光源的投射投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。<br/>                                                                                                                                                                                                                                                                                         |
| [**ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)       | 計算目前的光源投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ExtractPerVertexAlbedo**](id3dxprtengine--extractpervertexalbedo.md)                   | 從網格複製每個頂點的 >albedo 值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**FreeBounceData**](id3dxprtengine--freebouncedata.md)                                   | 釋出用於暫時退光模擬資料的記憶體。<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**FreeSSData**](id3dxprtengine--freessdata.md)                                           | 釋出用於暫存地下輕量模擬資料的記憶體。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**GetAdaptedMesh**](id3dxprtengine--getadaptedmesh.md)                                   | 傳回包含自調適型空間取樣所產生之修改的網格。 傳回的網格僅包含位置、法線和材質座標 (如果定義) 。<br/>                                                                                                                                                                                                                                                                                                   |
| [**GetNumFaces**](id3dxprtengine--getnumfaces.md)                                         | 抓取網格中的臉部數目，包括自調適型空間取樣的結果所加入的任何新臉部。<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetNumVerts**](id3dxprtengine--getnumverts.md)                                         | 抓取網格中的頂點數目，包括自我調整空間取樣之後加入的任何新頂點。<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetVertexAlbedo**](id3dxprtengine--getvertexalbedo.md)                                 | 抓取網格頂點的 >albedo 值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md)                                   | 將每個預先計算 radiance 傳輸 (PRT) 向量乘以每個頂點 >albedo。<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ResampleBuffer**](id3dxprtengine--resamplebuffer.md)                                   | Resamples 輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區，並將其儲存至輸出緩衝區。 這個方法可以用來將頂點緩衝區轉換成材質緩衝區，反之亦然。 它也可以用來將單一通道緩衝區轉換成3通道緩衝區，反之亦然。<br/>                                                                                                                                                                                  |
| [**RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)                               | 在網格上細分臉部，以提供不會消除網格上功能的保守調適型取樣。<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**ScaleMeshChunk**](id3dxprtengine--scalemeshchunk.md)                                   | 調整所有與指定 submesh 相關聯的範例。 方法適用于計算地下散佈。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetCallBack**](id3dxprtengine--setcallback.md)                                         | 設定選擇性回呼函式的指標，此函式會計算已完成的球面調和 (SH) 計算的百分比，並為呼叫端提供中止模擬器的選項。<br/>                                                                                                                                                                                                                                                                               |
| [**SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)                               | 設定3D 場景中的網格材質屬性。 使用這個方法來指定地下散佈參數。<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)                     | 設定3D 物件之間交集的最小和最大距離。 這些距離值可以用來控制物件可以陰影或反映光線的最小或最大距離。 例如，方法可以用來限制3D 模型的鄰近功能遮蔽。<br/>                                                                                                                                                                          |
| [**SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md)                             | 設定每個材質的 >albedo 值，並覆寫先前的 >albedo 值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**SetPerTexelNormal**](id3dxprtengine--setpertexelnormal.md)                             | 針對材質物件中的每個材質設定一般向量。 如果) 計算以圖元為基礎的預先計算 radiance 傳輸 (PRT) ，則會使用這個方法來儲存網格 (中的頂點一般向量或插入頂點法線。<br/>                                                                                                                                                                                                                                          |
| [**SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)                           | 設定每個網格頂點的 >albedo 值，並覆寫先前的 >albedo 值。<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)                                 | 設定預先計算 radiance 傳輸 (PRT) 模擬器所使用的取樣屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)                         | 在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。 通常用來判斷指定的點是否在陰影中。<br/>                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>備註

若要從 RGB 轉換成亮度值，請使用下列公式：


```
Luminance = R * 0.2125 + G * 0.7154 + B * 0.0721
```



**ID3DXPRTEngine** 介面是藉由呼叫 [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)函數來取得。

LPD3DXPRTENGINE 型別定義為 **ID3DXPRTEngine** 介面的指標。


```
typedef interface ID3DXPRTEngine ID3DXPRTEngine;
typedef interface ID3DXPRTEngine *LPD3DXPRTENGINE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)
</dt> <dt>

[預先計算 Radiance Transfer (Direct3D 9) ](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
