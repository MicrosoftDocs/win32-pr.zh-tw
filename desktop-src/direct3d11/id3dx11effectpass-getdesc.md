---
title: 'ID3DX11EffectPass GetDesc 方法 (D3dx11effect .h) '
description: 取得傳遞描述。
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- GetDesc 方法 Direct3D 11
- GetDesc 方法 Direct3D 11，ID3DX11EffectPass 介面
- ID3DX11EffectPass 介面 Direct3D 11，GetDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd75b5b23e253715af33c712fe957ae057b681f715a60fa37d4451c3fc76232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535064"
---
# <a name="id3dx11effectpassgetdesc-method"></a>ID3DX11EffectPass：： GetDesc 方法

取得傳遞描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDesc* 
</dt> <dd>

類型： **[ **D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)\***

傳遞描述的指標 (參閱 [**D3DX11 \_ pass \_ DESC**](d3dx11-pass-desc.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

Pass 是設定轉譯狀態和著色器的程式碼區塊， (接著設定常數緩衝區、取樣器和紋理) 。 效果技術包含一或多個階段。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





