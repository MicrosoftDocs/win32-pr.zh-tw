---
title: 'ID3DX11EffectVariable AsInterface 方法 (D3dx11effect .h) '
description: 取得介面變數。
ms.assetid: 5b1e5d05-ab36-42c2-9990-154baff5e9a4
keywords:
- AsInterface 方法 Direct3D 11
- AsInterface 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，AsInterface 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsInterface
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95fd7000e8529d04054ccaed84642e12d55417929789c569cc1f9893c2726f4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565648"
---
# <a name="id3dx11effectvariableasinterface-method"></a>ID3DX11EffectVariable：： AsInterface 方法

取得介面變數。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectInterfaceVariable* AsInterface();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***

介面變數的指標。 請參閱 [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)。

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

 

 





