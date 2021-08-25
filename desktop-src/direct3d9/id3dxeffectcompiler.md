---
description: ID3DXEffectCompiler 介面會從函式或頂點著色器編譯效果。
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: 'ID3DXEffectCompiler 介面 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c7a16417528d1adbd9ba54f9bd7120057654d14e0ef4bddad829e8f232445069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856738"
---
# <a name="id3dxeffectcompiler-interface"></a>ID3DXEffectCompiler 介面

**ID3DXEffectCompiler** 介面會從函式或頂點著色器編譯效果。

## <a name="members"></a>成員

**ID3DXEffectCompiler** 介面繼承自 [**ID3DXBaseEffect**](id3dxbaseeffect.md)。 **ID3DXEffectCompiler** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXEffectCompiler** 介面具有這些方法。



| 方法                                                      | 描述                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) | 編譯效果。<br/>                                                                                                               |
| [**CompileShader**](id3dxeffectcompiler--compileshader.md) | 從包含一或多個函式的效果編譯著色器。<br/>                                                            |
| [**GetLiteral**](id3dxeffectcompiler--getliteral.md)       | 取得參數的常值狀態。 常值參數的值不會在效果的存留期間變更。<br/>      |
| [**SetLiteral**](id3dxeffectcompiler--setliteral.md)       | 切換參數的常值狀態。 常值參數的值不會在效果的存留期間變更。<br/> |



 

## <a name="remarks"></a>備註

ID3DXEffectCompiler 介面的取得方式是呼叫 [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)、 [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)或 [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)。

LPD3DXEFFECTCOMPILER 型別定義為這個介面的指標。


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[效果介面](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




