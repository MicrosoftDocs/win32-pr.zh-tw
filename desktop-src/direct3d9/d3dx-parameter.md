---
description: 這些旗標會提供有關效果參數的其他資訊。
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: 'D3DX_PARAMETER (D3dx9effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001790"
---
# <a name="d3dx_parameter"></a>D3DX \_ 參數

這些旗標會提供有關效果參數的其他資訊。

[**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)會使用效果參數常數。



| 常數                                                                                                                                                                                           | 描述                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**D3DX \_ 參數 \_ 注釋**</dt> </dl> | 此參數會標示為批註。 請參閱 [使用批註將資訊新增至效果參數](using-an-effect.md)。<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**D3DX \_ 參數 \_ 常值**</dt> </dl>          | 此參數會標示為常值。 在編譯之後，常值參數無法變更，讓編譯器可以優化其使用方式。 共用參數不可標記為常值。 請參閱 [ (Direct3D 9) 的使用方式和常 ](usages-and-literals.md)值。 <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**共用的 D3DX \_ 參數 \_**</dt> </dl>             | 參數的值將由相同命名空間中的所有效果所共用。 變更其中一個效果的值，會在所有的共用效果中變更。 請參閱 [共用參數](cloning-and-sharing.md)。 **D3DX \_無法 \_** 使用 **D3DX \_ 參數 \_ 常** 值或 **D3DX \_ 參數 \_ 注釋** 來合併參數共用。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果常數](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




