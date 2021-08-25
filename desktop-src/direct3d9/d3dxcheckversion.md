---
description: D3DXCheckVersion 函式-確認您用來編譯的 D3DX 版本是您正在執行的版本。
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: 'D3DXCheckVersion 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26831f3a1a5f08494a7382cd412c30dcd24c1482c01dca684962a580068d380d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894118"
---
# <a name="d3dxcheckversion-function"></a>D3DXCheckVersion 函式

確認您用來編譯的 D3DX 版本是您正在執行的版本。

## <a name="syntax"></a>語法


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*D3DSDKVersion* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

使用 D3D \_ SDK \_ 版本。 請參閱＜備註＞。

</dd> <dt>

*D3DXSDKVersion* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

使用 D3DX \_ SDK \_ 版本。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果您編譯的 D3DX 版本是您正在執行的版本，則傳回 **TRUE** ;否則會傳回 **FALSE** 。

## <a name="remarks"></a>備註

在應用程式初始化期間使用此函數，如下所示：


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



使用 [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) 來確認是否已安裝正確的執行時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
