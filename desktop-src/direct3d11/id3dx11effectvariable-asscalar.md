---
title: 'ID3DX11EffectVariable AsScalar 方法 (D3dx11effect .h) '
description: 取得純量變數。
ms.assetid: 5cc02fb3-351a-4309-9145-1ed7d759a650
keywords:
- AsScalar 方法 Direct3D 11
- AsScalar 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，AsScalar 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsScalar
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e455250ae99075af449793d634fd6b3c2fafc4b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696871"
---
# <a name="id3dx11effectvariableasscalar-method"></a>ID3DX11EffectVariable：： AsScalar 方法

取得純量變數。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectScalarVariable* AsScalar();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***

純量變數的指標。 請參閱 [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)。

## <a name="remarks"></a>備註

AsScalar 會傳回已特製化到純量變數的效果變數版本。 類似于轉換，如果效果變數不包含純量資料，則此特製化會傳回不正確物件。

應用程式可以藉由呼叫 [**IsValid**](id3dx11effectvariable-isvalid.md)來測試傳回的物件是否有效。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





