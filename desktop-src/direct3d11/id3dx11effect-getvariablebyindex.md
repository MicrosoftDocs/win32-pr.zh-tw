---
title: 'ID3DX11Effect GetVariableByIndex 方法 (D3dx11effect .h) '
description: 依索引取得變數。
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- GetVariableByIndex 方法 Direct3D 11
- GetVariableByIndex 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetVariableByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992339"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a>ID3DX11Effect：： GetVariableByIndex 方法

依索引取得變數。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

以零為基底的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

指向 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。

## <a name="remarks"></a>備註

效果可能包含一或多個變數。 技術以外的變數會被視為所有效果的全域變數，而這些變數位於某個技術內，就是該技巧的本機變數。 您可以使用其名稱或索引來存取任何本機非靜態效果變數。

如果找不到變數，方法會傳回 [**效果變數介面**](id3dx11effectvariable.md) 的指標;您可以呼叫 [**ID3DX11Effect：： IsValid**](id3dx11effect-isvalid.md) 來確認索引是否存在。

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

 

