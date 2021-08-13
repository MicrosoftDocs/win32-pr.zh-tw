---
title: 'ID3DX11EffectConstantBuffer SetTextureBuffer 方法 (D3dx11effect .h) '
description: 設定材質緩衝區。
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- SetTextureBuffer 方法 Direct3D 11
- SetTextureBuffer 方法 Direct3D 11，ID3DX11EffectConstantBuffer 介面
- ID3DX11EffectConstantBuffer 介面 Direct3D 11，SetTextureBuffer 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d71b104d51b8310f2922c25e940cd559e2d47dca695cbe844e7526eb8235fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046367"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a>ID3DX11EffectConstantBuffer：： SetTextureBuffer 方法

設定材質緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTextureBuffer* 
</dt> <dd>

類型： **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***

用來存取材質緩衝區的著色器資源檢視介面指標。

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

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





