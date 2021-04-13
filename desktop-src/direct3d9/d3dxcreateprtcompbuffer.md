---
description: 從未壓縮的 ID3DXPRTBuffer 物件建立壓縮的預先計算 radiance 傳輸 (PRT) 緩衝區。 此函式應該搭配每個頂點或磁片區緩衝區使用。
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: 'D3DXCreatePRTCompBuffer 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322944"
---
# <a name="d3dxcreateprtcompbuffer-function"></a>D3DXCreatePRTCompBuffer 函式

從未壓縮的 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件建立壓縮的預先計算 radiance 傳輸 (PRT) 緩衝區。 此函式應該搭配每個頂點或磁片區緩衝區使用。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*品質* \[在\]
</dt> <dd>

類型： **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**

球形調和 (SH) 壓縮的品質。 請參閱 [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)。

</dd> <dt>

*NumClusters* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要用於壓縮的群集數目。

</dd> <dt>

*NumPCA* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

每個叢集中要使用的主體元件分析數目 (PCA) 基礎向量。

</dd> <dt>

*pCB* \[在\]
</dt> <dd>

類型： **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)回呼函式的選擇性指標，可用來計算已完成的 PRT 壓縮計算百分比。 必須實回呼函式來傳回， \_ 才能繼續執行壓縮常式。 任何其他值都會中止壓縮。 可能是 **Null**。

</dd> <dt>

*lpUserCoNtext* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

傳遞至 [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) 回呼函式的使用者定義值的選擇性指標。 通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。 可能是 **Null**。

</dd> <dt>

*pBuffer* \[在\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

將壓縮之未壓縮 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標位址。

</dd> <dt>

*ppBuffer* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

輸出 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 物件之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
