---
description: 取得已載入記憶體之映射的相關資訊。
ms.assetid: 6750116a-ad4f-4102-aba9-6ef32c367be4
title: 'D3DX10GetImageInfoFromMemory 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 677ce6a2ac8e4e165ca0a2bbb64b6254870e4ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986518"
---
# <a name="d3dx10getimageinfofrommemory-function"></a>D3DX10GetImageInfoFromMemory 函式

取得已載入記憶體之映射的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrcData* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

記憶體中影像的指標。

</dd> <dt>

*SrcDataSize* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**

記憶體中影像的大小（以位元組為單位）。

</dd> <dt>

*pPump* \[在\]
</dt> <dd>

類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

選擇性的執行緒抽取，可用來以非同步方式載入資訊。 可以是 **Null**。 請參閱 [**ID3DX10ThreadPump**](id3dx10threadpump.md)。

</dd> <dt>

*pSrcInfo* \[在\]
</dt> <dd>

類型： **[ **D3DX10 \_ 影像 \_ 資訊**](d3dx10-image-info.md)\***

記憶體中影像的相關資訊。

</dd> <dt>

*pHResult* \[擴展\]
</dt> <dd>

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

傳回值的指標。 可能是 **Null**。 如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 10 中的材質函數](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
