---
title: 'ID3DX11EffectTechnique 介面 (D3dx11effect .h) '
description: ID3DX11EffectTechnique 介面是通過的集合。ID3DX11EffectTechnique 物件的存留期等於其父 ID3DX11Effect 物件的存留期。
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- ID3DX11EffectTechnique 介面 Direct3D 11
- ID3DX11EffectTechnique 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d8970ad1e75f37e8270a013d3830216ae128e41c03d4ad5245ac6ffc7615691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532350"
---
# <a name="id3dx11effecttechnique-interface"></a>ID3DX11EffectTechnique 介面

**ID3DX11EffectTechnique** 介面是通過的集合。

**ID3DX11EffectTechnique** 物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectTechnique** 介面具有這些方法。



| 方法                                                                        | 描述                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**ComputeStateBlockMask**](id3dx11effecttechnique-computestateblockmask.md) | 計算狀態欄塊遮罩以允許/防止狀態變更。<br/> |
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | 依索引取得批註。<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | 依名稱取得批註。<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | 取得技術描述。<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | 依索引取得傳遞。<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | 依名稱取得傳遞。<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | 測試技術以查看其是否包含有效的語法。<br/>       |



 

## <a name="remarks"></a>備註

效果包含一或多個技術;每個技術都包含一或多個階段;每個階段都包含狀態指派。

若要取得效果技巧介面，請呼叫 [**ID3DX11Effect：： GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)之類的方法。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11介面](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





