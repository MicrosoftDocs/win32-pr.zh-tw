---
title: 'ID3DX11Effect GetTechniqueByName 方法 (D3dx11effect .h) '
description: '依名稱取得技術。 |ID3DX11Effect GetTechniqueByName 方法 (D3dx11effect .h) '
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- GetTechniqueByName 方法 Direct3D 11
- GetTechniqueByName 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetTechniqueByName 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974656"
---
# <a name="id3dx11effectgettechniquebyname-method"></a>ID3DX11Effect：： GetTechniqueByName 方法

依名稱取得技術。

## <a name="syntax"></a>語法


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* 
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

技術的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)的指標。 如果找不到具有適當名稱的技術，則會傳回不正確技巧。 [**ID3DX11EffectTechnique：： IsValid**](id3dx11effecttechnique-isvalid.md) 應針對傳回的技術進行呼叫，以判斷它是否有效。

## <a name="remarks"></a>備註

效果包含一或多個技術;每個技術都包含一或多個階段。 您可以使用其名稱或索引來存取技術。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

