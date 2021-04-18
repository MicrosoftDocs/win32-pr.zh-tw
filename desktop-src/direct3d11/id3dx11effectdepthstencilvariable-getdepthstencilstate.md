---
title: 'ID3DX11EffectDepthStencilVariable GetDepthStencilState 方法 (D3dx11effect .h) '
description: 取得深度樣板介面的指標。
ms.assetid: 3e8f7fc6-960c-45f5-9276-9aa2a5e7a6c9
keywords:
- GetDepthStencilState 方法 Direct3D 11
- GetDepthStencilState 方法 Direct3D 11，ID3DX11EffectDepthStencilVariable 介面
- ID3DX11EffectDepthStencilVariable 介面 Direct3D 11，GetDepthStencilState 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9276c7a126d5441361a4d449c4ee2ece70d995
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974681"
---
# <a name="id3dx11effectdepthstencilvariablegetdepthstencilstate-method"></a>ID3DX11EffectDepthStencilVariable：： GetDepthStencilState 方法

取得深度樣板介面的指標。

## <a name="syntax"></a>語法


```C++
HRESULT GetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState **ppDepthStencilState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

索引至深度樣板介面的陣列。 如果只有一個深度樣板介面，請使用0。

</dd> <dt>

*ppDepthStencilState* 
</dt> <dd>

類型： **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***

Blend 狀態介面指標的位址 (參閱 [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)) 。

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

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

