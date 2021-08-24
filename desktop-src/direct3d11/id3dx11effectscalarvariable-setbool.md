---
title: 'ID3DX11EffectScalarVariable SetBool 方法 (D3dx11effect .h) '
description: 設定布林值變數。
ms.assetid: b5385ed3-6e65-4d65-bb8e-835967e6f610
keywords:
- SetBool 方法 Direct3D 11
- SetBool 方法 Direct3D 11，ID3DX11EffectScalarVariable 介面
- ID3DX11EffectScalarVariable 介面 Direct3D 11，SetBool 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f12837a0a6c33d4b5ae0345bd654bd5e0d19d31ea449a5eca8e77ba740c782c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408168"
---
# <a name="id3dx11effectscalarvariablesetbool-method"></a>ID3DX11EffectScalarVariable：： SetBool 方法

設定布林值變數。

## <a name="syntax"></a>語法


```C++
HRESULT SetBool(
   BOOL Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* 
</dt> <dd>

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

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

 

