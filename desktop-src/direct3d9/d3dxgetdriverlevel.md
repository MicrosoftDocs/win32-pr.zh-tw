---
description: 傳回驅動程式層級。
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: 'D3DXGetDriverLevel 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982012"
---
# <a name="d3dxgetdriverlevel-function"></a>D3DXGetDriverLevel 函式

傳回驅動程式層級。

## <a name="syntax"></a>語法


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

代表裝置之 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](../winprog/windows-data-types.md)**

驅動程式層級。 請參閱＜備註＞。

## <a name="remarks"></a>備註

這個方法會傳回驅動程式版本，也就是下列其中一項：

-   700-Direct3D 7 層級驅動程式
-   800-Direct3D 8 層級驅動程式
-   900-Direct3D 9 層級的驅動程式

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
