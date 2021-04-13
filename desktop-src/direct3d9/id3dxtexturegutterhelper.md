---
description: ID3DXTextureGutterHelper 介面是用來建立和管理材質中的裝訂區區域。 裝訂邊區域會將材質分開，並允許雙線性插補，以避免在材質界限呈現成品。
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: 'ID3DXTextureGutterHelper 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323223"
---
# <a name="id3dxtexturegutterhelper-interface"></a>ID3DXTextureGutterHelper 介面

ID3DXTextureGutterHelper 介面是用來建立和管理材質中的裝訂區區域。 裝訂邊區域會將材質分開，並允許雙線性插補，以避免在材質界限呈現成品。

Get .。。方法可讓您存取 Apply 所使用的資料結構 .。。方法。

## <a name="members"></a>成員

**ID3DXTextureGutterHelper** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXTextureGutterHelper** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXTextureGutterHelper** 介面具有這些方法。



| 方法                                                                   | 描述                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) | 將裝訂邊套用至 FLOAT 材質緩衝區。<br/>                                                  |
| [**ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md)     | 將裝訂邊套用至 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區物件。<br/>               |
| [**ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)     | 將裝訂邊套用至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 材質物件。<br/>        |
| [**GetBaryMap**](id3dxtexturegutterhelper--getbarymap.md)               | 抓取材質 barycentric 座標。<br/>                                                    |
| [**GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md)               | 抓取每個材質所屬之網格臉部的索引。<br/>                           |
| [**GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md)           | 接收材質類別值，指出根據每個材質位置的材質類別。<br/> |
| [**GetHeight**](id3dxtexturegutterhelper--getheight.md)                 | 抓取紋理的高度（以圖元為單位）。<br/>                                             |
| [**GetTexelMap**](id3dxtexturegutterhelper--gettexelmap.md)             | 抓取每個材質的 (u，v) 材質座標。<br/>                                     |
| [**GetWidth**](id3dxtexturegutterhelper--getwidth.md)                   | 抓取紋理的寬度（以圖元為單位）。<br/>                                              |
| [**ResampleTex**](id3dxtexturegutterhelper--resampletex.md)             | 將材質 Resamples 到這個 gutterhelper 的參數化。<br/>                              |
| [**SetBaryMap**](id3dxtexturegutterhelper--setbarymap.md)               | 設定材質 barycentric 座標。<br/>                                                         |
| [**SetFaceMap**](id3dxtexturegutterhelper--setfacemap.md)               | 設定每個材質所屬之網格臉部的索引。<br/>                                |
| [**SetGutterMap**](id3dxtexturegutterhelper--setguttermap.md)           | 設定材質類別值，指出根據每個材質位置的材質類別。<br/>     |
| [**SetTexelMap**](id3dxtexturegutterhelper--settexelmap.md)             | 設定每個材質的 (u，v) 材質座標。<br/>                                          |



 

## <a name="remarks"></a>備註

> [!Note]  
> 搭配預先計算 radiance transfer (PRT) 使用時，此介面需要模型的唯一參數化。 每個材質都必須對應到模型表面上的單一點，反之亦然。 如果模型包含多個紋理，則必須將它分割成個別的片段，每個材質各包含一個裝訂邊協助程式物件。

 

這個介面可以用來在材質空間中產生地圖，其中每個材質都是在四個類別中的其中一個。



| 材質類別 | 材質位置                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | 不正確點;將不會使用材質。                                                                                                                                                                                                                                                                                                                                        |
| 1           | 在三角形內。                                                                                                                                                                                                                                                                                                                                                              |
| 2           | 在裝訂邊內。                                                                                                                                                                                                                                                                                                                                                                |
| 4           | 內部裝訂邊;材質將會評估為 [**ID3DXTextureGutterHelper：： ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md)、 [**ID3DXTextureGutterHelper：： ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)或 [**ID3DXTextureGutterHelper：： ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) 方法中的完整範例。 |



 

針對類別1和2，材質會與它所屬的臉部一起儲存，以及該臉部前兩個頂點的 barycentric 座標。 裝訂邊頂點會指派至材質空間中最接近的邊緣。

沒有材質類別3。

**ID3DXTextureGutterHelper** 介面是藉由呼叫 [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md)函數來取得。

LPD3DXTEXTUREGUTTERHELPER 型別定義為 **ID3DXTextureGutterHelper** 介面的指標。


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
