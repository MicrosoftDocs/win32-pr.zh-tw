---
title: 'ID3DX11Effect GetVariableByName 方法 (D3dx11effect .h) '
description: 依名稱取得變數。
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- GetVariableByName 方法 Direct3D 11
- GetVariableByName 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetVariableByName 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992335"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>ID3DX11Effect：： GetVariableByName 方法

依名稱取得變數。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* 
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

變數名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。 如果找不到指定的名稱，則傳回不正確變數。

## <a name="remarks"></a>備註

效果可能包含一或多個變數。 技術以外的變數會被視為所有效果的全域變數，而這些變數位於某個技術內，就是該技巧的本機變數。 您可以使用其名稱或索引來存取效果變數。

無論是否找到變數，方法都會傳回 [**效果變數介面**](id3dx11effectvariable.md) 的指標。 應呼叫 [**ID3DX11Effect：： IsValid**](id3dx11effect-isvalid.md)來確認名稱是否存在。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

