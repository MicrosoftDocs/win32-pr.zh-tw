---
title: 'ID3DX11EffectVariable GetType 方法 (D3dx11effect .h) '
description: 取得型別資訊。
ms.assetid: c9ada96a-0259-48c1-b869-ba0f51bf4600
keywords:
- GetType 方法 Direct3D 11
- GetType 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetType 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0eae9da797ee22f85234383e2e54d97f4cb1045bcdd0216e70899b294b42378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894548"
---
# <a name="id3dx11effectvariablegettype-method"></a>ID3DX11EffectVariable：： GetType 方法

取得型別資訊。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectType* GetType();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

[**ID3DX11EffectType**](id3dx11effecttype.md)的指標。

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

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





