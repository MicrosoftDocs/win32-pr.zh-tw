---
title: 'ID3DX11EffectGroup 介面 (D3dx11effect .h) '
description: ID3DX11EffectGroup 介面會存取效果群組。ID3DX11EffectGroup 物件的存留期等於其父 ID3DX11Effect 物件的存留期。
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- ID3DX11EffectGroup 介面 Direct3D 11
- ID3DX11EffectGroup 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974564"
---
# <a name="id3dx11effectgroup-interface"></a>ID3DX11EffectGroup 介面

**ID3DX11EffectGroup** 介面會存取效果群組。

**ID3DX11EffectGroup** 物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectGroup** 介面具有這些方法。



| 方法                                                                  | 描述                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetAnnotationByIndex**](id3dx11effectgroup-getannotationbyindex.md) | 依索引取得批註。<br/>                        |
| [**GetAnnotationByName**](id3dx11effectgroup-getannotationbyname.md)   | 依名稱取得批註。<br/>                         |
| [**GetDesc**](id3dx11effectgroup-getdesc.md)                           | 取得群組描述。<br/>                          |
| [**GetTechniqueByIndex**](id3dx11effectgroup-gettechniquebyindex.md)   | 依索引取得技術。<br/>                          |
| [**GetTechniqueByName**](id3dx11effectgroup-gettechniquebyname.md)     | 依名稱取得技術。<br/>                           |
| [**IsValid**](id3dx11effectgroup-isvalid.md)                           | 測試效果，以查看它是否包含有效的語法。<br/> |



 

## <a name="remarks"></a>備註

若要取得 **ID3DX11EffectGroup** 介面，請呼叫方法，例如 [**ID3DX11Effect：： GetGroupByName**](id3dx11effect-getgroupbyname.md)。

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

 

 





