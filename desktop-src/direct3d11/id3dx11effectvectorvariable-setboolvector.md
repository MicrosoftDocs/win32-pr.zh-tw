---
title: 'ID3DX11EffectVectorVariable SetBoolVector 方法 (D3dx11effect .h) '
description: 設定包含布林資料的四個元件向量。
ms.assetid: 2138eeb9-6aa0-43f5-852c-1ab9c8117a88
keywords:
- SetBoolVector 方法 Direct3D 11
- SetBoolVector 方法 Direct3D 11，ID3DX11EffectVectorVariable 介面
- ID3DX11EffectVectorVariable 介面 Direct3D 11，SetBoolVector 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ec75ab46bcebb796680310b88897ac8519cdeeb640967e1ddd1a5f413e1a3af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734030"
---
# <a name="id3dx11effectvectorvariablesetboolvector-method"></a>ID3DX11EffectVectorVariable：： SetBoolVector 方法

設定包含布林資料的四個元件向量。

## <a name="syntax"></a>語法


```C++
HRESULT SetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Pdata* 
</dt> <dd>

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)\***

第一個元件的指標。

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

