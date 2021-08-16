---
description: 將材質 Resamples 到這個 gutterhelper 的參數化。
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'ID3DXTextureGutterHelper：： ResampleTex 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7d3afe8155eb33a37b30abcfc96aae83c0a96461c1ee2dd6118a671701cfed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800317"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>ID3DXTextureGutterHelper：： ResampleTex 方法

將材質 Resamples 到這個 gutterhelper 的參數化。

## <a name="syntax"></a>語法


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTextureIn* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

對應至 pMeshIn 中原始參數化的材質。 此材質將用來建立 pTextureOut。

</dd> <dt>

*pMeshIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

包含原始和新參數化的網格。 您必須在 D3DDECLUSAGE TEXCOORD index 0 中儲存新的參數化 \_ 。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

頂點資料使用量 (與 UsageIndex) 搭配使用，這會識別包含 pMeshIn 中原始參數化之頂點宣告的元件。 請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。

</dd> <dt>

*UsageIndex* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

以零為基底的索引 (搭配使用) 使用，這會識別包含 pMeshIn 中原始參數化之頂點宣告的元件。 \_新參數化需要 D3DDECLUSAGE TEXCOORD 和 index 0 的組合; 您可以使用任何其他使用方式/索引組合。

</dd> <dt>

*pTextureOut* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

重新取樣的材質。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

在此函式的情況下，參數化是一組材質座標，可將網格的三角形對應至材質上的三角形。 新的參數化是一組包含在裝訂邊協助程式介面中的材質座標，而原始參數化則是包含在輸入網格內的材質座標集合。

假設材質座標介於0和1（含）之間，而且新的參數化必須在頂點宣告中宣告為紋理座標索引0。 原始材質和重新取樣的材質必須具有相同的寬度和高度。

例如，為了準備將材質重新取樣：

-   使用 [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)之類的函式，建立下面)  (pOriginalTex 的原始紋理介面。
-   為重新取樣的材質建立新的材質介面 (pResampledTex 以下) 。 此材質的大小必須符合裝訂邊協助程式材質 (寬度和高度) 的大小。
-   呼叫 [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) 以取得新的參數化，如下所示：


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



其中一個常見的案例可能是使用 UVAtlas 來建立材質塔，然後使用 ResampleTex 將材質重新取樣至新的參數化。 如需圖集的詳細資訊，請參閱 [使用 UVAtlas (Direct3D 9) ](using-uvatlas.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)
</dt> </dl>

 

 
