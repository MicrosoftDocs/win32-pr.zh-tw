---
title: 'ID3DX11EffectDepthStencilViewVariable SetDepthStencilArray 方法 (D3dx11effect .h) '
description: 設定深度樣板視圖資源的陣列。
ms.assetid: 7a00ca3e-fb07-4185-a361-36228f72dcea
keywords:
- SetDepthStencilArray 方法 Direct3D 11
- SetDepthStencilArray 方法 Direct3D 11，ID3DX11EffectDepthStencilViewVariable 介面
- ID3DX11EffectDepthStencilViewVariable 介面 Direct3D 11，SetDepthStencilArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e6588a039d77730c42e68a977fe16e8126cf54ab502a6806a45a5190e57b26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858128"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencilarray-method"></a>ID3DX11EffectDepthStencilViewVariable：： SetDepthStencilArray 方法

設定深度樣板視圖資源的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppResources* 
</dt> <dd>

類型： **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***

深度樣板視圖介面陣列的指標。 請參閱 [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)。

</dd> <dt>

*Offset* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

以零為基底的陣列索引，用來設定第一個介面。

</dd> <dt>

*Count* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

陣列中的項目數。

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

