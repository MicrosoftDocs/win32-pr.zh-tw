---
title: 'ID3DX11EffectType GetDesc 方法 (D3dx11effect .h) '
description: 取得效果類型描述。
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- GetDesc 方法 Direct3D 11
- GetDesc 方法 Direct3D 11，ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，GetDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381f885a15dede6a500e82b08a1f24e4f0542ffa46211e5b68ef7f73f40d0f0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460778"
---
# <a name="id3dx11effecttypegetdesc-method"></a>ID3DX11EffectType：： GetDesc 方法

取得效果類型描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDesc* 
</dt> <dd>

類型： **[ **D3DX11 \_ 效果 \_ 類型 \_ DESC**](d3dx11-effect-type-desc.md)\***

效果類型描述的指標。 請參閱 [**D3DX11 \_ 效果 \_ 類型 \_ DESC**](d3dx11-effect-type-desc.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

效果變數描述包含效果類型的名稱、注釋、語義、旗標和緩衝區位移的相關資料。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

 





