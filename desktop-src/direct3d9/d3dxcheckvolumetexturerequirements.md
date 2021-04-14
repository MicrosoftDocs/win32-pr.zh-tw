---
description: 檢查磁片區材質建立參數。
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: 'D3DXCheckVolumeTextureRequirements 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386471"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a>D3DXCheckVolumeTextureRequirements 函式

檢查磁片區材質建立參數。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與磁片區材質相關聯的裝置。

</dd> <dt>

*pWidth* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

要求的寬度（以圖元為單位）的指標，或為 **Null**。 傳回已更正的大小。

</dd> <dt>

*pHeight* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

要求高度（以圖元為單位）的指標，或為 **Null**。 傳回已更正的大小。

</dd> <dt>

*pDepth* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

要求的深度（以圖元為單位）的指標，或為 **Null**。 傳回已更正的大小。

</dd> <dt>

*pNumMipLevels* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

要求的 mipmap 層級數目的指標，或 **為 Null**。 傳回已更正的 mipmap 層級數目。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

目前未使用，設定為0。

</dd> <dt>

*pformatetc 架構* \[in、out\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)\***

[D3DFORMAT](d3dformat.md)列舉型別的成員指標。 指定所需的像素格式，或 **為 Null**。 傳回更正的格式。

</dd> <dt>

*集* \[ 區在\]
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置磁片區材質的記憶體類別。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE，D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

如果此函式的參數無效，此函式會傳回已更正的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
