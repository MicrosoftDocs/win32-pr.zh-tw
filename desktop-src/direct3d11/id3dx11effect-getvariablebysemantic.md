---
title: 'ID3DX11Effect GetVariableBySemantic 方法 (D3dx11effect .h) '
description: 依語義取得變數。
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- GetVariableBySemantic 方法 Direct3D 11
- GetVariableBySemantic 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetVariableBySemantic 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196388"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a>ID3DX11Effect：： GetVariableBySemantic 方法

依語義取得變數。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*語義* 
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

語義名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

以語義表示之效果變數的指標。 請參閱 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。

## <a name="remarks"></a>備註

每個效果變數都可以附加語義，也就是使用者定義的中繼資料字串。 某些 [系統值的語法](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) 是保留字，會觸發管線階段內建的功能。

如果找不到變數，方法會傳回 [**效果變數介面**](id3dx11effectvariable.md) 的指標;您可以呼叫 [**ID3DX11Effect：： IsValid**](id3dx11effect-isvalid.md) 來確認語義是否存在。

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

 

