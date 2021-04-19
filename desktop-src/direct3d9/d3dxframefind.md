---
description: 尋找根框架的子框架。
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: 'D3DXFrameFind 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986514"
---
# <a name="d3dxframefind-function"></a>D3DXFrameFind 函式

尋找根框架的子框架。

## <a name="syntax"></a>語法


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFrameRoot* \[在\]
</dt> <dd>

Type： **Const [**D3DXFRAME**](d3dxframe.md) \***

根框架的指標。 請參閱 [**D3DXFRAME**](d3dxframe.md)。

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

要尋找的子框架名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **LPD3DXFRAME**](d3dxframe.md)**

如果找到，則傳回子框架，否則傳回 **Null** 。 請參閱 [**D3DXFRAME**](d3dxframe.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動畫函數](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
