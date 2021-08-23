---
title: 'ID3DX11EffectSamplerVariable SetSampler 方法 (D3dx11effect .h) '
description: 設定取樣器狀態。
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- SetSampler 方法 Direct3D 11
- SetSampler 方法 Direct3D 11，ID3DX11EffectSamplerVariable 介面
- ID3DX11EffectSamplerVariable 介面 Direct3D 11，SetSampler 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4667b8261b46b1ecb1732c1ecc77efcf93d327426f0ea20f6c7710e94ed825e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791938"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a>ID3DX11EffectSamplerVariable：： SetSampler 方法

設定取樣器狀態。

## <a name="syntax"></a>語法


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

索引至取樣器介面的陣列。 如果只有一個取樣器介面，請使用0。

</dd> <dt>

*pSampler* 
</dt> <dd>

類型： **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***

[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)介面的指標，其中包含取樣器狀態。

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

 

