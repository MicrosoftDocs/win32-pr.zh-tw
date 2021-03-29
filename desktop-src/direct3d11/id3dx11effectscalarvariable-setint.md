---
title: 'ID3DX11EffectScalarVariable SetInt 方法 (D3dx11effect .h) '
description: 設定整數變數。
ms.assetid: 614284be-8f70-4d7e-b797-b67e813615ab
keywords:
- SetInt 方法 Direct3D 11
- SetInt 方法 Direct3D 11，ID3DX11EffectScalarVariable 介面
- ID3DX11EffectScalarVariable 介面 Direct3D 11，SetInt 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4e2f44a3b67db12bd84f5dd23426c033b99b57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196191"
---
# <a name="id3dx11effectscalarvariablesetint-method"></a>ID3DX11EffectScalarVariable：： SetInt 方法

設定整數變數。

## <a name="syntax"></a>語法


```C++
HRESULT SetInt(
   int Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* 
</dt> <dd>

類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**

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

 

