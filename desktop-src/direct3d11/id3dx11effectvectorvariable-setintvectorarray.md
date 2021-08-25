---
title: 'ID3DX11EffectVectorVariable SetIntVectorArray 方法 (D3dx11effect .h) '
description: 設定包含整數資料之四個元件向量的陣列。
ms.assetid: c9e522d7-5545-4b91-b6b3-6fad9a151cb0
keywords:
- SetIntVectorArray 方法 Direct3D 11
- SetIntVectorArray 方法 Direct3D 11，ID3DX11EffectVectorVariable 介面
- ID3DX11EffectVectorVariable 介面 Direct3D 11，SetIntVectorArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5260fd85461b23d02d9aa33619fcf2c00a81fcb63212d612e6e8920728bbefd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894538"
---
# <a name="id3dx11effectvectorvariablesetintvectorarray-method"></a>ID3DX11EffectVectorVariable：： SetIntVectorArray 方法

設定包含整數資料之四個元件向量的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetIntVectorArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Pdata* 
</dt> <dd>

類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

要設定之資料開頭的指標。

</dd> <dt>

*Offset* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

必須設為 0;這會保留供日後使用。

</dd> <dt>

*Count* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要設定的陣列元素數目。

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

 

