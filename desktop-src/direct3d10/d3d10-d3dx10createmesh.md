---
description: D3DX10CreateMesh 函式-使用宣告子建立網格物件。
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: 'D3DX10CreateMesh 函式 (D3DX10Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4f044d3337a2da05eb78b027492b870f450e4309c94faa8c72db935437511dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853478"
---
# <a name="d3dx10createmesh-function"></a>D3DX10CreateMesh 函式

使用宣告子建立網格物件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

[**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)的指標，也就是要與網格相關聯的裝置物件。

</dd> <dt>

*pDeclaration* \[在\]
</dt> <dd>

Type： **Const [**D3D10 \_ INPUT \_ ELEMENT \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

[**D3D10 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)元素的陣列，描述傳回之網格的頂點格式。 此參數必須直接對應至彈性頂點格式， (FVF) 。

</dd> <dt>

*DeclCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

PDeclaration 中的元素數目。

</dd> <dt>

*pPositionSemantic* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

識別頂點宣告中哪個部分包含位置資訊的語法。

</dd> <dt>

*VertexCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

網格的頂點數目。 此參數必須大於0。

</dd> <dt>

*FaceCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

網格的臉部數目。 此數位的有效範圍大於0，而一個小於最大 DWORD (通常是 65534) ，因為會保留最後一個索引。

</dd> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

[**D3DX10 \_ 網格**](d3dx10-mesh.md)中一或多個旗標的組合，指定網格的選項。

</dd> <dt>

*ppMesh* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

[**ID3DX10Mesh 介面**](id3dx10mesh.md)指標的位址，表示所建立的網格物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[D3DX 函式](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
