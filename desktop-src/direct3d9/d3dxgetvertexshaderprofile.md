---
description: D3DXGetVertexShaderProfile 函式-傳回指定裝置所支援的最高高階著色器語言 (HLSL) 設定檔的名稱。
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: 'D3DXGetVertexShaderProfile 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5c646fb9779ca923480487cb96f184c76eff9ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473624"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>D3DXGetVertexShaderProfile 函式

傳回指定裝置支援的最高階著色器語言 (HLSL) 設定檔的名稱。

## <a name="syntax"></a>語法


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

裝置的指標。 請參閱 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

HLSL 設定檔名稱。

如果裝置不支援頂點著色器，則函數會傳回 **Null**。

## <a name="remarks"></a>備註

著色器設定檔會指定要使用的元件著色器版本，以及編譯著色器時可供 HLSL 編譯器使用的功能。 下表列出支援的頂點著色器設定檔。




| 著色器設定檔 | Description | 
|----------------|-------------|
| vs_1_1 | 編譯為 vs_1_1 版本。 | 
| vs_2_0 | 編譯為 vs_2_0 版本。 | 
| vs_2_a | 如同 vs_2_0 設定檔，具有下列可供編譯器使用的其他功能：<ul><li> (r # ) 大於或等於13的臨時暫存器數目。</li><li>動態流程式控制制指令。</li><li>預測。</li></ul> | 
| vs_3_0 | 編譯為 vs_3_0 版本。 | 




 

如需著色器版本之間差異的詳細資訊，請參閱 [頂點著色器差異](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器函式](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
