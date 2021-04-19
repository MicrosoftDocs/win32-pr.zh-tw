---
description: 取得著色器輸入的語法。 您可以使用這個方法來判斷輸入頂點格式。
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: 'D3DXGetShaderInputSemantics 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982010"
---
# <a name="d3dxgetshaderinputsemantics-function"></a>D3DXGetShaderInputSemantics 函式

取得著色器輸入的語法。 您可以使用這個方法來判斷輸入頂點格式。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFunction* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

著色器函式 DWORD 資料流程的指標。

</dd> <dt>

*pSemantics* \[在\]
</dt> <dd>

類型： **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***

[**D3DXSEMANTIC**](d3dxsemantic.md)結構陣列的指標。 此函式會使用著色器所參考的每個輸入專案的語義來填滿此陣列。 此陣列假設至少包含 MAXD3DDECLLENGTH 元素。 不過，使用 pSemantics = **Null** 呼叫 **D3DXGetShaderInputSemantics** 會傳回 pCount 所需的元素數目。

</dd> <dt>

*pCount* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

傳回 pSemantics 中的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

使用 **D3DXGetShaderInputSemantics** 傳回著色器所需的輸入語義清單。 這是用來找出高階著色器語言 (HLSL) 著色器的輸入頂點格式的方式。 如果著色器有遺漏您頂點宣告的其他輸入，您可以建立具有值為0的額外頂點資料流程，其具有預設值的遺漏元件。 比方說，這項技術可以用來為未指定的模型提供預設頂點色彩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器函式](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
