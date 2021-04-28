---
description: D3DX10CheckVersion 函式-確認您用來編譯的 D3DX 版本是您正在執行的版本。
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: 'D3DX10CheckVersion 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fc8befa88fb706965a30224843745b033ea205b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105346"
---
# <a name="d3dx10checkversion-function"></a>D3DX10CheckVersion 函式

確認您用來編譯的 D3DX 版本是您正在執行的版本。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*D3DSdkVersion* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

使用 D3D10 \_ SDK \_ 版本。 請參閱＜備註＞。

</dd> <dt>

*D3DX10SdkVersion* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

使用 D3DX10 \_ SDK \_ 版本。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果版本不相符，則函式會傳回 FALSE (小於或等於0的數位，數位本身沒有任何意義) 。

## <a name="remarks"></a>備註

在您的應用程式初始化期間，請使用此函數。


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
