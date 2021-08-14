---
title: 'ID3DX11EffectMatrixVariable SetMatrixArray 方法 (D3dx11effect .h) '
description: 設定浮點數矩陣的陣列。
ms.assetid: c90d621c-7500-49c3-ab40-2d0630fc4bec
keywords:
- SetMatrixArray 方法 Direct3D 11
- SetMatrixArray 方法 Direct3D 11，ID3DX11EffectMatrixVariable 介面
- ID3DX11EffectMatrixVariable 介面 Direct3D 11，SetMatrixArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c310dcb5d5469edd603b4d8801eed91366b68fbe9a25b089075d4bb8118a811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046086"
---
# <a name="id3dx11effectmatrixvariablesetmatrixarray-method"></a>ID3DX11EffectMatrixVariable：： SetMatrixArray 方法

設定浮點數矩陣的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetMatrixArray(
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

第一個矩陣的指標。

</dd> <dt>

*Offset* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要從陣列開頭跳過的矩陣元素數目。

</dd> <dt>

*Count* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要設定的元素數目。

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

 

