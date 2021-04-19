---
description: 傳回指定裝置支援的最高階著色器語言 (HLSL) 設定檔的名稱。
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
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997391"
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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>著色器設定檔</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vs_1_1</td>
<td>編譯為 vs_1_1 版本。</td>
</tr>
<tr class="even">
<td>vs_2_0</td>
<td>編譯為 vs_2_0 版本。</td>
</tr>
<tr class="odd">
<td>vs_2_a</td>
<td>如同 vs_2_0 設定檔，具有下列可供編譯器使用的其他功能：
<ul>
<li> (r # ) 大於或等於13的臨時暫存器數目。</li>
<li>動態流程式控制制指令。</li>
<li>預測。</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_3_0</td>
<td>編譯為 vs_3_0 版本。</td>
</tr>
</tbody>
</table>



 

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

 

 
