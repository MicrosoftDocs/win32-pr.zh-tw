---
description: 使用者執行的方法，用於關閉著色器的 \# 包含檔案。
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'ID3DXInclude：： Close 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974894"
---
# <a name="id3dxincludeclose-method"></a>ID3DXInclude：： Close 方法

使用者執行的方法，用於關閉著色器的 \# 包含檔案。

## <a name="syntax"></a>語法


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

傳回之緩衝區的指標，其中包含 include 指示詞。 這是對應的 [**ID3DXInclude：： Open**](id3dxinclude--open.md) 呼叫所傳回的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

使用者執行的方法應該會傳回 S \_ OK。 如果回呼在讀取 include 檔案時失敗 \# ，則造成呼叫回呼的 API 將會失敗。 這是下列項目之一：

-   HLSL 著色器將會失敗其中一個 D3DXCompileShader \* \* \* 函數。
-   元件著色器將會使其中一個 D3DXAssembleShader 函式失敗 \* \* \* 。
-   此效果將會使其中一個 D3DXCreateEffect \* \* \* 或 D3DXCreateEffectCompiler \* \* \* 函數失敗。

## <a name="remarks"></a>備註

如果 [**ID3DXInclude：： Open**](id3dxinclude--open.md) 成功，就保證會在使用此介面的 API 傳回之前呼叫 **ID3DXInclude：： Close** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude：： Open**](id3dxinclude--open.md)
</dt> </dl>

 

 
