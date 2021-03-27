---
title: 'ID3DX11EffectMatrixVariable SetMatrixTransposeArray 方法 (D3dx11effect .h) '
description: 變換並設定浮點數矩陣的陣列。
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- SetMatrixTransposeArray 方法 Direct3D 11
- SetMatrixTransposeArray 方法 Direct3D 11，ID3DX11EffectMatrixVariable 介面
- ID3DX11EffectMatrixVariable 介面 Direct3D 11，SetMatrixTransposeArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946210"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a>ID3DX11EffectMatrixVariable：： SetMatrixTransposeArray 方法

變換並設定浮點數矩陣的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Pdata* 
</dt> <dd>

類型： **float \***

矩陣陣列的指標。

</dd> <dt>

*Offset* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

位移 (在陣列的開頭與要設定的第一個矩陣之間的矩陣數目) 。

</dd> <dt>

*Count* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要設定的陣列中的矩陣數目。

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

 

