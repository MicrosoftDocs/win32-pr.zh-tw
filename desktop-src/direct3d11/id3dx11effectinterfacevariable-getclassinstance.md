---
title: 'ID3DX11EffectInterfaceVariable GetClassInstance 方法 (D3dx11effect .h) '
description: 取得類別實例。
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- GetClassInstance 方法 Direct3D 11
- GetClassInstance 方法 Direct3D 11，ID3DX11EffectInterfaceVariable 介面
- ID3DX11EffectInterfaceVariable 介面 Direct3D 11，GetClassInstance 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6fb05473b2671e0224fe36214fa7d8be93dc3bea17ceb90b0b8f0a871cc755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988458"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a>ID3DX11EffectInterfaceVariable：： GetClassInstance 方法

取得類別實例。

## <a name="syntax"></a>語法


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEffectClassInstance* 
</dt> <dd>

類型： **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***

將設定為類別實例之 [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) 指標的指標。

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

[ID3DX11EffectInterfaceVariable](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





