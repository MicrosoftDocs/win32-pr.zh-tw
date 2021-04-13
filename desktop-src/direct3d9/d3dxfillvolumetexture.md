---
description: 使用使用者提供的函式來填滿給定磁片區材質之每個 mip 層級的每個材質。
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: 'D3DXFillVolumeTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322920"
---
# <a name="d3dxfillvolumetexture-function"></a>D3DXFillVolumeTexture 函式

使用使用者提供的函式來填滿給定磁片區材質之每個 mip 層級的每個材質。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面的指標，代表填滿的材質。

</dd> <dt>

*pFunction* \[在\]
</dt> <dd>

類型： **[LPD3DXFILL3D](lpd3dxfill3d.md)**

使用者提供的評估工具函式的指標，該函式將用來計算每個材質的值。 函數會遵循 [LPD3DXFILL3D](lpd3dxfill3d.md)的原型。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

使用者定義資料之任意區塊的指標。 此指標會傳遞至 *pFunction* 中提供的函式。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

如果磁片區為非動態 (，因為使用方式在建立時設為 0) ，而且位於視訊記憶體 (記憶體集區設定為 D3DPOOL \_ 預設) 時， **D3DXFillVolumeTexture** 將會失敗，因為無法鎖定磁片區。

這個範例會建立一個名為 ColorVolumeFill 的函式，此函式依賴 D3DXFillVolumeTexture。


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
