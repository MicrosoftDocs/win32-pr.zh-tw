---
description: 取得 OpenGL 樣式的線條繪圖模式。
ms.assetid: 80b33c05-d081-45f3-83d8-71a3555cc8ef
title: 'ID3DXLine：： GetGLLines 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe521b743dab6c9c4922014ff82785d303f83f7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196457"
---
# <a name="id3dxlinegetgllines-method"></a>ID3DXLine：： GetGLLines 方法

取得 OpenGL 樣式的線條繪圖模式。

## <a name="syntax"></a>語法


```C++
BOOL GetGLLines();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果已啟用 OpenGL 樣式的行，則傳回 **TRUE** ; 如果啟用 Direct3D 樣式的行，則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::SetGLLines**](id3dxline--setgllines.md)
</dt> </dl>

 

 
