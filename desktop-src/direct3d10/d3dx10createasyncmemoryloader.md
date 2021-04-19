---
description: 建立異步記憶體載入器。
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: 'D3DX10CreateAsyncMemoryLoader 函式 (D3DX10Async) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0219026eabfcff6dfcec0df4721716302f09f5e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986104"
---
# <a name="d3dx10createasyncmemoryloader-function"></a>D3DX10CreateAsyncMemoryLoader 函式

建立異步記憶體載入器。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

資料的指標。

</dd> <dt>

*cbData* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**

資料的大小。

</dd> <dt>

*ppDataLoader* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

非同步資料處理器指標的位址 (參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Async。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
