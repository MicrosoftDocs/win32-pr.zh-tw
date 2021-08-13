---
title: 'ID3DX11EffectVariable GetAnnotationByName 方法 (D3dx11effect .h) '
description: '依名稱取得批註。 |ID3DX11EffectVariable GetAnnotationByName 方法 (D3dx11effect .h) '
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- GetAnnotationByName 方法 Direct3D 11
- GetAnnotationByName 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetAnnotationByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 766366497187fec9c6dab3c5f92f5fbca23f5729297976d2c9e2c7e4ffb0deef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119376458"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a>ID3DX11EffectVariable：： GetAnnotationByName 方法

依名稱取得批註。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* 
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

批註名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。 請注意，如果找不到注釋，則傳回的 **ID3DX11EffectVariable** 會是空的。 應呼叫 [**ID3DX11EffectVariable：： IsValid**](id3dx11effectvariable-isvalid.md) 方法，以判斷是否找到注釋。

## <a name="remarks"></a>備註

Annonations 可以附加至技術、pass 或全域變數。

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

 

