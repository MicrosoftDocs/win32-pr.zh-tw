---
title: 'ID3DX11EffectScalarVariable GetBool 方法 (D3dx11effect .h) '
description: 取得布林值變數。
ms.assetid: 9d2789af-c59f-4d2d-87c6-9f36286e8a15
keywords:
- GetBool 方法 Direct3D 11
- GetBool 方法 Direct3D 11，ID3DX11EffectScalarVariable 介面
- ID3DX11EffectScalarVariable 介面 Direct3D 11，GetBool 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d402507c009f46adb2dcb455c772f2102e0e0673675446e25cff0da3382c111a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119377858"
---
# <a name="id3dx11effectscalarvariablegetbool-method"></a>ID3DX11EffectScalarVariable：： GetBool 方法

取得布林值變數。

## <a name="syntax"></a>語法


```C++
HRESULT GetBool(
   BOOL *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pValue* 
</dt> <dd>

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)\***

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

 

