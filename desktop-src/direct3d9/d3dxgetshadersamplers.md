---
description: 取得著色器中所參考的取樣器名稱。
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: 'D3DXGetShaderSamplers 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986094"
---
# <a name="d3dxgetshadersamplers-function"></a>D3DXGetShaderSamplers 函式

取得著色器中所參考的取樣器名稱。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFunction* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

著色器函式 DWORD 資料流程的指標。

</dd> <dt>

*pSamplers* \[in、out\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)\***

LPCSTRs 陣列的指標。 函式會使用 *pFunction* 中所包含之取樣器名稱的指標來填滿此陣列。 陣列大小上限是 vs \_ 3 \_ 0 和 ps \_ 3 \_ 0) 的取樣器暫存器數目上限 (16。

若要尋找使用的取樣器數目，請在使用 pSamplers = **Null** 呼叫 **D3DXGetShaderSamplers** 之後，檢查 *pCount* 。

</dd> <dt>

*pCount* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

傳回著色器所參考的取樣器數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器函式](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
