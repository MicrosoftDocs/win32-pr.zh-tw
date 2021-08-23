---
description: 切換模式以繪製 OpenGL 樣式的線條。
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'ID3DXLine：： SetGLLines 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bea46421cd259deb87bccaaf9e97073550467674491bba9e1983a7482686efd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748138"
---
# <a name="id3dxlinesetgllines-method"></a>ID3DXLine：： SetGLLines 方法

切換模式以繪製 OpenGL 樣式的線條。

## <a name="syntax"></a>語法


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bGLLines* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

切換 OpenGL 樣式的線條繪圖。 **TRUE** 會啟用 OpenGL 樣式的行，而 **FALSE** 則會啟用 Direct3D 樣式的行。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
