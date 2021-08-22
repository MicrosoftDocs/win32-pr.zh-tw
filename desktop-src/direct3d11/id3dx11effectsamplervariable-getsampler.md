---
title: 'ID3DX11EffectSamplerVariable GetSampler 方法 (D3dx11effect .h) '
description: 取得取樣器介面的指標。
ms.assetid: ac2a05f1-e3ca-4ebf-b655-34133c4e50ac
keywords:
- GetSampler 方法 Direct3D 11
- GetSampler 方法 Direct3D 11，ID3DX11EffectSamplerVariable 介面
- ID3DX11EffectSamplerVariable 介面 Direct3D 11，GetSampler 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc9c400f3596d380f5e671eaa04f4e4340bde385230f331e3e2fdc7ee1a92f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045826"
---
# <a name="id3dx11effectsamplervariablegetsampler-method"></a>ID3DX11EffectSamplerVariable：： GetSampler 方法

取得取樣器介面的指標。

## <a name="syntax"></a>語法


```C++
HRESULT GetSampler(
   UINT               Index,
   ID3D11SamplerState **ppSampler
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

索引至取樣器介面的陣列。 如果只有一個取樣器介面，請使用0。

</dd> <dt>

*ppSampler* 
</dt> <dd>

類型： **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***

取樣器介面指標的位址 (參閱 [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)) 。

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

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

