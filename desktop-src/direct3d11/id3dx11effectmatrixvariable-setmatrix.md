---
title: 'ID3DX11EffectMatrixVariable SetMatrix 方法 (D3dx11effect .h) '
description: 設定浮點數矩陣。
ms.assetid: 91c69bc0-c8c6-4232-8c70-801ac8ddbcda
keywords:
- SetMatrix 方法 Direct3D 11
- SetMatrix 方法 Direct3D 11，ID3DX11EffectMatrixVariable 介面
- ID3DX11EffectMatrixVariable 介面 Direct3D 11，SetMatrix 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af7b64e7391461efc47b6f65ca676b870174347
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974625"
---
# <a name="id3dx11effectmatrixvariablesetmatrix-method"></a>ID3DX11EffectMatrixVariable：： SetMatrix 方法

設定浮點數矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT SetMatrix(
   float *pData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Pdata* 
</dt> <dd>

類型： **float \***

矩陣中第一個元素的指標。

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

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





