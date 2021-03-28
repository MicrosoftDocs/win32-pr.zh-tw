---
title: 'ID3DX11EffectRasterizerVariable GetRasterizerState 方法 (D3dx11effect .h) '
description: 取得轉譯器介面的指標。
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- GetRasterizerState 方法 Direct3D 11
- GetRasterizerState 方法 Direct3D 11，ID3DX11EffectRasterizerVariable 介面
- ID3DX11EffectRasterizerVariable 介面 Direct3D 11，GetRasterizerState 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972140a8f74a3e5a6728429faddacc253aaa6c9d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974727"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a>ID3DX11EffectRasterizerVariable：： GetRasterizerState 方法

取得轉譯器介面的指標。

## <a name="syntax"></a>語法


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

在轉譯器介面陣列中編制索引。 如果只有一個轉譯器介面，請使用0。

</dd> <dt>

*ppRasterizerState* 
</dt> <dd>

類型： **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***

轉譯器介面指標的位址 (參閱 [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

