---
description: 定義材質階段的材質篩選模式。
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: 'D3DTEXTUREFILTERTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bd6038e1b3d2b2f85e5766605583db9879427343
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343003"
---
# <a name="d3dtexturefiltertype-enumeration"></a>D3DTEXTUREFILTERTYPE 列舉

定義材質階段的材質篩選模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ 無**
</dt> <dd>

搭配 [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md)使用時，會停用 mipmap。

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF \_ 點**
</dt> <dd>

搭配 [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) 或 [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)使用時，會指定點篩選要分別當做材質放大或縮制篩選使用。 搭配 **D3DSAMP \_ MIPFILTER** 使用時，會啟用 mipmap，並指定轉譯器會從最接近的 mip 層級材質中選擇色彩。

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ 線性**
</dt> <dd>

搭配 [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) 或 [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)使用時，會指定線性篩選要分別當做材質放大或縮制篩選使用。 與 **D3DSAMP \_ MIPFILTER** 搭配使用時，會啟用 mipmap 和三線性篩選; 它會指定在兩個最接近的 mip 層級之間，進行轉譯器的插補。

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ 各向異性**
</dt> <dd>

搭配 [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) 或 [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)使用時，會指定用來分別作為紋理縮放比例或縮制篩選的非等向材質篩選。 補償紋理多邊形和螢幕平面之間的角度差異所造成的扭曲。 未定義搭配 **D3DSAMP \_ MIPFILTER** 使用。

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**
</dt> <dd>

用來作為材質放大或縮制濾波器的四個範例折做篩選。 未定義搭配 [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) 使用。

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**
</dt> <dd>

用來作為材質放大或縮制濾波器的4個範例高斯篩選。 未定義搭配 [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) 使用。

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**
</dt> <dd>

單色紋理的卷積篩選。 請參閱 [D3DFMT \_ A1](d3dformat.md)。

Direct3D 9 與 Direct3D 9Ex 之間的差異：

- 此旗標僅適用于 Direct3D 9Ex。



 

未定義搭配 [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) 使用。

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

[**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)和 [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)會使用 D3DTEXTUREFILTERTYPE 來定義材質階段的材質篩選模式。

若要檢查格式是否支援 D3DTEXF 點以外的材質篩選類型 \_ ， (一律支援) ，請使用 D3DUSAGE 查詢篩選準則來呼叫 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) \_ \_ 。

藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 與 D3DSAMP \_ MAGFILTER 值做為第二個參數，並使用這個列舉的一個成員做為第三個參數，設定紋理階段的放大篩選篩選。

藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 與 D3DSAMP \_ MINFILTER 值做為第二個參數，並使用這個列舉的一個成員做為第三個參數，來設定紋理階段的縮制篩選。

藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 與 D3DSAMP \_ MIPFILTER 值做為第二個參數，並將此列舉的一個成員作為第三個參數，將材質篩選設定為使用 mipmap 層級。

並非所有適用于裝置的有效篩選模式都適用于磁片區對應。 一般而言，磁片區 \_ 對應會支援 D3DTEXF POINT 和 D3DTEXF \_ 線性放大篩選。 如果 \_ 設定了 D3DPTEXTURECAPS MIPVOLUMEMAP，則磁片區 \_ 對應將會支援 D3DTEXF 點 mipmap 濾波器和 D3DTEXF \_ 點以及 D3DTEXF \_ 線性縮制篩選。 裝置不一定會支援磁片區對應的 D3DTEXF \_ 線性 mipmap 篩選。 支援2D 對應之非等向篩選的裝置不一定支援磁片區對應的非等向篩選。 不過，啟用非等向篩選的應用程式將會收到最佳的可用篩選 (可能的線性) 如果不支援非等向篩選。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**ID3DXPatchMesh::GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[**ID3DXPatchMesh::SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> <dt>

[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
