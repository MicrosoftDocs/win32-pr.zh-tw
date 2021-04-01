---
title: 'ID3DX11EffectShaderResourceVariable GetResource 方法 (D3dx11effect .h) '
description: 取得著色器資源。
ms.assetid: 7c56aba0-ce60-4b50-9c1a-802bf1d73c6b
keywords:
- GetResource 方法 Direct3D 11
- GetResource 方法 Direct3D 11，ID3DX11EffectShaderResourceVariable 介面
- ID3DX11EffectShaderResourceVariable 介面 Direct3D 11，GetResource 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea841ae63646958603396d5b65305c242961942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196189"
---
# <a name="id3dx11effectshaderresourcevariablegetresource-method"></a>ID3DX11EffectShaderResourceVariable：： GetResource 方法

取得著色器資源。

## <a name="syntax"></a>語法


```C++
HRESULT GetResource(
   ID3D11ShaderResourceView **ppResource
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppResource* 
</dt> <dd>

類型： **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

著色器資源-view 介面指標的位址。 請參閱 [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)。

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

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





