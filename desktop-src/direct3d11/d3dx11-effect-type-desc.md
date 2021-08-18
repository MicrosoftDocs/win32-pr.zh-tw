---
title: 'D3DX11_EFFECT_TYPE_DESC 結構 (D3dx11effect .h) '
description: 描述效果變數型別。
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc045b40105a698c9d051de791991c49d2b6d0dd4672d50f344e8781999dd5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989958"
---
# <a name="d3dx11_effect_type_desc-structure"></a>D3DX11 \_ 效果 \_ 類型 \_ DESC 結構

描述效果變數型別。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**TypeName**
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

類型的名稱，例如 "float4" 或 "Mystruct>) "。

</dd> <dt>

**類別**
</dt> <dd>

Type： **[ **D3D10 \_ 著色器 \_ 變數 \_ 類別**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

變數類別 (查看 [**D3D10 \_ 著色器 \_ 變數 \_ 類別**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)) 。

</dd> <dt>

**類型**
</dt> <dd>

類型： **[ **D3D10 \_ 著色器 \_ 變數 \_ 類型**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

變數型別 (查看 [**D3D10 \_ 著色器 \_ 變數 \_ 類型**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)) 。

</dd> <dt>

**元素**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

如果不是陣列) ，此類型中的元素數目 (0。

</dd> <dt>

**成員**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

成員數目 (0 （如果不是結構) ）。

</dd> <dt>

**資料列**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

如果不是數值基本) ，此類型中的資料列數目 (0。

</dd> <dt>

**資料行**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

這種類型的資料行數目 (0 （如果不是數值基本) ）。

</dd> <dt>

**PackedSize**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

當緊密壓縮時，表示此資料類型所需的位元組數目。

</dd> <dt>

**UnpackedSize**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

在常數緩衝區中配置時，此資料類型所佔用的位元組數目。

</dd> <dt>

**分散**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

在常數緩衝區中配置時，要在元素之間搜尋的位元組數目。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX11 \_ 效果 \_ 類型 \_ DESC 可搭配 [ **ID3DX11EffectType：： GetDesc** 使用](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11結構](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

