---
description: 描述列舉所包含的資料。
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: 'D3DXPARAMETER_TYPE 列舉 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322639"
---
# <a name="d3dxparameter_type-enumeration"></a>D3DXPARAMETER \_ 類型列舉

描述列舉所包含的資料。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ VOID**
</dt> <dd>

參數是 void 指標。

</dd> <dt>

<span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT \_ BOOL**
</dt> <dd>

參數是布林值。 任何傳入 [**ID3DXConstantTable：： SetBool**](id3dxconstanttable--setbool.md)、 [**ID3DXConstantTable：： SetBoolArray**](id3dxconstanttable--setboolarray.md)、 [**ID3DXConstantTable：： SetValue**](id3dxconstanttable--setvalue.md)、 [**ID3DXConstantTable：： SetVector**](id3dxconstanttable--setvector.md)或 [**ID3DXConstantTable：： SetVectorArray**](id3dxconstanttable--setvectorarray.md) 的非零值，在寫入常數資料表之前，都會對應到 1 (TRUE) 。否則，常數資料表中的值會設定為0。

</dd> <dt>

<span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ INT**
</dt> <dd>

參數是整數。 傳遞至 [**ID3DXConstantTable：： SetValue**](id3dxconstanttable--setvalue.md)、 [**ID3DXConstantTable：： SetVector**](id3dxconstanttable--setvector.md)或 [**ID3DXConstantTable：： SetVectorArray**](id3dxconstanttable--setvectorarray.md) 的任何浮點值，都會在寫入常數資料表之前，) 四捨五入 (為零個小數位數。

</dd> <dt>

<span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ 浮點數**
</dt> <dd>

參數是浮點數。

</dd> <dt>

<span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT \_ 字串**
</dt> <dd>

參數是字串。

</dd> <dt>

<span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT \_ 材質**
</dt> <dd>

參數是紋理。

</dd> <dt>

<span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**
</dt> <dd>

參數是1D 紋理。

</dd> <dt>

<span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**
</dt> <dd>

參數是2D 材質。

</dd> <dt>

<span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**
</dt> <dd>

參數是3D 紋理。

</dd> <dt>

<span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**
</dt> <dd>

參數是 cube 紋理。

</dd> <dt>

<span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT \_ 取樣器**
</dt> <dd>

參數是取樣器。

</dd> <dt>

<span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**
</dt> <dd>

參數是1D 取樣器。

</dd> <dt>

<span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**
</dt> <dd>

參數是2D 取樣器。

</dd> <dt>

<span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**
</dt> <dd>

參數是3D 取樣器。

</dd> <dt>

<span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**
</dt> <dd>

參數是 cube 取樣器。

</dd> <dt>

<span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ 無效**
</dt> <dd>

參數是圖元著色器。

</dd> <dt>

<span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**
</dt> <dd>

參數是頂點著色器。

</dd> <dt>

<span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**
</dt> <dd>

參數是圖元著色器片段。

</dd> <dt>

<span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**
</dt> <dd>

參數是頂點著色器片段。

</dd> <dt>

<span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**\_不支援 D3DXPT**
</dt> <dd>

不支援參數。

</dd> <dt>

<span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




