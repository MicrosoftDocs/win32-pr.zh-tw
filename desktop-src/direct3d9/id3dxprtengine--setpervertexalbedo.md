---
description: 設定每個網格頂點的 >albedo 值，並覆寫先前的 >albedo 值。
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'ID3DXPRTEngine：： SetPerVertexAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985723"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a>ID3DXPRTEngine：： SetPerVertexAlbedo 方法

設定每個網格頂點的 >albedo 值，並覆寫先前的 >albedo 值。

## <a name="syntax"></a>語法


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDataIn* \[在\]
</dt> <dd>

類型： **CONST VOID \***

第一個範例的 FLOAT >albedo 資料指標。

</dd> <dt>

*NumChannels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要設定的色彩通道數目。 設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。

</dd> <dt>

*Stride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

取得下一個樣本 >albedo 值所需的 Stride （以位元組為單位）。 請參閱 [寬度與音調 (Direct3D 9) ](width-vs--pitch.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
