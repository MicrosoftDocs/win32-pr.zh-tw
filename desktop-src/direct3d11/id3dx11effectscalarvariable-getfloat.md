---
title: 'ID3DX11EffectScalarVariable GetFloat 方法 (D3dx11effect .h) '
description: 取得浮點數變數。
ms.assetid: 0416db40-5e70-44e4-905f-86f49a9b58b8
keywords:
- GetFloat 方法 Direct3D 11
- GetFloat 方法 Direct3D 11，ID3DX11EffectScalarVariable 介面
- ID3DX11EffectScalarVariable 介面 Direct3D 11，GetFloat 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f00e5f4863b54a208b1b9f9b32e4292c274575271e447c3ac20e7b09a686ace
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952718"
---
# <a name="id3dx11effectscalarvariablegetfloat-method"></a>ID3DX11EffectScalarVariable：： GetFloat 方法

取得浮點數變數。

## <a name="syntax"></a>語法


```C++
HRESULT GetFloat(
   float *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pValue* 
</dt> <dd>

類型： **float \***

變數的指標。

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





