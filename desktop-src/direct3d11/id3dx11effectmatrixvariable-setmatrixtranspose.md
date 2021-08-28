---
title: 'ID3DX11EffectMatrixVariable SetMatrixTranspose 方法 (D3dx11effect .h) '
description: 變換並設定浮點數矩陣。
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- SetMatrixTranspose 方法 Direct3D 11
- SetMatrixTranspose 方法 Direct3D 11，ID3DX11EffectMatrixVariable 介面
- ID3DX11EffectMatrixVariable 介面 Direct3D 11，SetMatrixTranspose 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de86741ba3168276da48756082e2e59f876009523ea940cdb58d070b4e72c3a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535111"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a>ID3DX11EffectMatrixVariable：： SetMatrixTranspose 方法

變換並設定浮點數矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Pdata* 
</dt> <dd>

類型： **float \***

矩陣第一個元素的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

轉型矩陣會將資料順序從資料列資料行順序重新排列成資料行順序 (或反之亦然) 。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





