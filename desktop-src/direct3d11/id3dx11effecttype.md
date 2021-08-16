---
title: 'ID3DX11EffectType 介面 (D3dx11effect .h) '
description: ID3DX11EffectType 介面會依類型存取效果變數。ID3DX11EffectType 物件的存留期等於其父 ID3DX11Effect 物件的存留期。
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- ID3DX11EffectType 介面 Direct3D 11
- ID3DX11EffectType 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d397f856fec49cf9909cd7089a1067250e78ca3f97c72d913d0ffdc146efb93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532145"
---
# <a name="id3dx11effecttype-interface"></a>ID3DX11EffectType 介面

**ID3DX11EffectType** 介面會依類型存取效果變數。

**ID3DX11EffectType** 物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectType** 介面具有這些方法。



| 方法                                                                       | 描述                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [**GetDesc**](id3dx11effecttype-getdesc.md)                                 | 取得效果類型描述。<br/>        |
| [**GetMemberName**](id3dx11effecttype-getmembername.md)                     | 取得成員的名稱。<br/>              |
| [**GetMemberSemantic**](id3dx11effecttype-getmembersemantic.md)             | 取得附加至成員的語義。<br/> |
| [**GetMemberTypeByIndex**](id3dx11effecttype-getmembertypebyindex.md)       | 依索引取得成員類型。<br/>            |
| [**GetMemberTypeByName**](id3dx11effecttype-getmembertypebyname.md)         | 依名稱取得成員類型。<br/>            |
| [**GetMemberTypeBySemantic**](id3dx11effecttype-getmembertypebysemantic.md) | 依語義取得成員類型。<br/>         |
| [**IsValid**](id3dx11effecttype-isvalid.md)                                 | 測試效果類型是否有效。<br/>   |



 

## <a name="remarks"></a>備註

若要從效果變數取得效果類型的相關資訊，請呼叫 [**ID3DX11EffectVariable：： GetType**](id3dx11effectvariable-gettype.md)。

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

 

 





