---
title: 'ID3DX11EffectTechnique GetAnnotationByIndex 方法 (D3dx11effect .h) '
description: '依索引取得批註。 |ID3DX11EffectTechnique GetAnnotationByIndex 方法 (D3dx11effect .h) '
ms.assetid: 703663b0-ee00-4686-a038-6c99ce61266b
keywords:
- GetAnnotationByIndex 方法 Direct3D 11
- GetAnnotationByIndex 方法 Direct3D 11，ID3DX11EffectTechnique 介面
- ID3DX11EffectTechnique 介面 Direct3D 11，GetAnnotationByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7de800e05dfb6731340ad7255019d4017eefb0cc88f9069e8c4aae4f327071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532566"
---
# <a name="id3dx11effecttechniquegetannotationbyindex-method"></a>ID3DX11EffectTechnique：： GetAnnotationByIndex 方法

依索引取得批註。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

介面指標以零為基底的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。

## <a name="remarks"></a>備註

使用注釋，將中繼資料的片段附加至技術。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

