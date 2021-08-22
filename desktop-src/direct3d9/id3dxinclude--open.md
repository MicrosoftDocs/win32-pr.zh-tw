---
description: 使用者執行的方法，用來開啟和讀取著色器包含檔案的內容 \# 。
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'ID3DXInclude：： Open 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e50b4774f6ed62b1e8a6e6cb85b5732efd878302563958e25e6b9017f9acc58d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987388"
---
# <a name="id3dxincludeopen-method"></a>ID3DXInclude：： Open 方法

使用者執行的方法，用來開啟和讀取著色器包含檔案的內容 \# 。

## <a name="syntax"></a>語法


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IncludeType* \[在\]
</dt> <dd>

類型： **[ **D3DXINCLUDE \_ 類型**](./d3dxinclude-type.md)**

Include 檔案的位置 \# 。 請參閱 [**D3DXINCLUDE \_ 類型**](./d3dxinclude-type.md)。

</dd> <dt>

*pFileName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

Include 檔案的名稱 \# 。

</dd> <dt>

*pParentData* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

包含 include 檔之容器的指標 \# 。 編譯器可能會在 *pParentData* 中傳遞 Null。 如需詳細資訊，請參閱 [編譯效果 (Direct3D 11) ](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md)中的「搜尋 Include 檔」一節。

</dd> <dt>

*ppData* \[擴展\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)\***

傳回之緩衝區的指標，其中包含 include 指示詞。 這個指標會維持有效，直到呼叫 [**ID3DXInclude：： Close**](id3dxinclude--close.md) 為止。

</dd> <dt>

*pBytes* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

PpData 中傳回的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

使用者執行的方法應該會傳回 S \_ OK。 如果回呼在讀取 include 檔案時失敗 \# ，則造成呼叫回呼的 API 將會失敗。 這是下列項目之一：

-   HLSL 著色器將會失敗其中一個 D3DXCompileShader \* \* \* 函數。
-   元件著色器將會使其中一個 D3DXAssembleShader 函式失敗 \* \* \* 。
-   此效果將會使其中一個 D3DXCreateEffect \* \* \* 或 D3DXCreateEffectCompiler \* \* \* 函數失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude：： Close**](id3dxinclude--close.md)
</dt> </dl>

 

 
