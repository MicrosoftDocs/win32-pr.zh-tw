---
description: ID3DXPRTCompBuffer 介面會儲存 ID3DXPRTBuffer 緩衝區的壓縮版本，以搭配 (PCA) 的主體元件分析使用。
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: 'ID3DXPRTCompBuffer 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a84f1bc7b25af0c900f5587ba0d1dd948cac39bc52f706ff389c0ca9d053ec0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985608"
---
# <a name="id3dxprtcompbuffer-interface"></a>ID3DXPRTCompBuffer 介面

**ID3DXPRTCompBuffer** 介面會儲存 [**ID3DXPRTBuffer**](id3dxprtbuffer.md)緩衝區的壓縮版本，以搭配 (PCA) 的主體元件分析使用。

## <a name="members"></a>成員

**ID3DXPRTCompBuffer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXPRTCompBuffer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXPRTCompBuffer** 介面具有這些方法。



| 方法                                                             | 描述                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtractBasis**](id3dxprtcompbuffer--extractbasis.md)           | 從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區中，針對指定的叢集，將 mean 和主體元件分析 (PCA) 基礎向量。<br/>                                                                       |
| [**ExtractClusterIDs**](id3dxprtcompbuffer--extractclusterids.md) | 從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區解壓縮每個範例的叢集識別碼。<br/>                                                                                                                              |
| [**ExtractPCA**](id3dxprtcompbuffer--extractpca.md)               | 從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區，將每個樣本的主體元件分析 (PCA) 投影係數。<br/>                                                                               |
| [**ExtractTexture**](id3dxprtcompbuffer--extracttexture.md)       | 從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件。<br/> |
| [**ExtractToMesh**](id3dxprtcompbuffer--extracttomesh.md)         | 從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 [**ID3DXMesh**](id3dxmesh.md) 物件。<br/>                 |
| [**GetHeight**](id3dxprtcompbuffer--getheight.md)                 | 抓取紋理的高度（以圖元為單位）。<br/>                                                                                                                                                                         |
| [**GetNumChannels**](id3dxprtcompbuffer--getnumchannels.md)       | 抓取記憶體中用來儲存範例的色彩通道數目。<br/>                                                                                                                                                 |
| [**GetNumClusters**](id3dxprtcompbuffer--getnumclusters.md)       | 抓取要用於壓縮的群集數目。<br/>                                                                                                                                                                |
| [**GetNumCoeffs**](id3dxprtcompbuffer--getnumcoeffs.md)           | 抓取記憶體中用來儲存範例的每個顏色通道的純量數目。<br/>                                                                                                                                      |
| [**GetNumPCA**](id3dxprtcompbuffer--getnumpca.md)                 | 抓取每個叢集中要使用的主體元件分析 (PCA) 基礎向量的數目。<br/>                                                                                                                        |
| [**GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md)         | 抓取取樣 (或材質) 的頂點數目。<br/>                                                                                                                                                                   |
| [**GetWidth**](id3dxprtcompbuffer--getwidth.md)                   | 抓取紋理的寬度（以圖元為單位）。<br/>                                                                                                                                                                          |
| [**IsTexture**](id3dxprtcompbuffer--istexture.md)                 | 指出緩衝區是否包含材質。<br/>                                                                                                                                                                        |
| [**NormalizeData**](id3dxprtcompbuffer--normalizedata.md)         | 將所有主體元件分析正規化 (PCA) 權數，使其介於-1 到1之間。 基礎向量會經過修改，以反映此正規化。<br/>                                                                  |



 

## <a name="remarks"></a>備註

**ID3DXPRTCompBuffer** 介面是藉由呼叫 [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)函數來取得。

LPD3DXPRTCOMPBUFFER 型別定義為 **ID3DXPRTCompBuffer** 介面的指標。


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
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

[**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> </dl>

 

 
