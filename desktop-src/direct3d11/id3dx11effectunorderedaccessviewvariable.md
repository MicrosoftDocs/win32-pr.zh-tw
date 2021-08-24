---
title: 'ID3DX11EffectUnorderedAccessViewVariable 介面 (D3dx11effect .h) '
description: 存取未排序的存取權。
ms.assetid: f78dc8c5-c85a-48cf-b579-f2937aa5ce2a
keywords:
- ID3DX11EffectUnorderedAccessViewVariable 介面 Direct3D 11
- ID3DX11EffectUnorderedAccessViewVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f81cb77f3757f9476b79277bf82252c8403738535acbbe1b1b07afa55f26d292
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119376808"
---
# <a name="id3dx11effectunorderedaccessviewvariable-interface"></a>ID3DX11EffectUnorderedAccessViewVariable 介面

存取未排序的存取權。

## <a name="members"></a>成員

**ID3DX11EffectUnorderedAccessViewVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。 **ID3DX11EffectUnorderedAccessViewVariable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectUnorderedAccessViewVariable** 介面具有這些方法。



| 方法                                                                                                      | 描述                                        |
|:------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetUnorderedAccessView**](id3dx11effectunorderedaccessviewvariable-getunorderedaccessview.md)           | 取得未排序的存取權。<br/>           |
| [**GetUnorderedAccessViewArray**](id3dx11effectunorderedaccessviewvariable-getunorderedaccessviewarray.md) | 取得未排序存取-views 的陣列。<br/> |
| [**SetUnorderedAccessView**](id3dx11effectunorderedaccessviewvariable-setunorderedaccessview.md)           | 設定未排序的存取權。<br/>           |
| [**SetUnorderedAccessViewArray**](id3dx11effectunorderedaccessviewvariable-setunorderedaccessviewarray.md) | 設定未排序存取-views 的陣列。<br/> |



 

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

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[效果11介面](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





