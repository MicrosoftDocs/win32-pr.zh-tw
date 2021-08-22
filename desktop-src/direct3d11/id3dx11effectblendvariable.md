---
title: 'ID3DX11EffectBlendVariable 介面 (D3dx11effect .h) '
description: Blend 變數介面會存取 blend 狀態。
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- ID3DX11EffectBlendVariable 介面 Direct3D 11
- ID3DX11EffectBlendVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bd65c15c40c2e7ce44092baebdef66f17f2de8c1052589a984ff15c9f4b77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046456"
---
# <a name="id3dx11effectblendvariable-interface"></a>ID3DX11EffectBlendVariable 介面

Blend 變數介面會存取 blend 狀態。

## <a name="members"></a>成員

**ID3DX11EffectBlendVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。 **ID3DX11EffectBlendVariable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectBlendVariable** 介面具有這些方法。



| 方法                                                                    | 描述                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBackingStore**](id3dx11effectblendvariable-getbackingstore.md)     | 取得 blend 狀態變數的指標。<br/>  |
| [**GetBlendState**](id3dx11effectblendvariable-getblendstate.md)         | 取得 blend 狀態介面的指標。<br/> |
| [**SetBlendState**](id3dx11effectblendvariable-setblendstate.md)         | 設定效果的 blend 狀態。<br/>             |
| [**UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md) | 還原先前設定的 blend 狀態。<br/>     |



 

## <a name="remarks"></a>備註

當將效果讀入記憶體時，就會建立 [**ID3DX11EffectVariable**](id3dx11effectvariable.md) 介面。

效果變數會儲存在備份存放區的記憶體中;套用技術時，備份存放區中的值會複製到裝置。 您可以使用其中一種方法來傳回狀態。

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

 

 





