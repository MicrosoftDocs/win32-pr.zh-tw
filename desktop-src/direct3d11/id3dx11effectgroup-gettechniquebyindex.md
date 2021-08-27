---
title: 'ID3DX11EffectGroup GetTechniqueByIndex 方法 (D3dx11effect .h) '
description: '依索引取得技術。 |ID3DX11EffectGroup GetTechniqueByIndex 方法 (D3dx11effect .h) '
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- GetTechniqueByIndex 方法 Direct3D 11
- GetTechniqueByIndex 方法 Direct3D 11，ID3DX11EffectGroup 介面
- ID3DX11EffectGroup 介面 Direct3D 11，GetTechniqueByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654b090b3481a915557569e0801e75b8ad089c66cfca4a893d6f865345088171
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046286"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a>ID3DX11EffectGroup：： GetTechniqueByIndex 方法

依索引取得技術。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

以零為基底的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)的指標。

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

