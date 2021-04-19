---
description: 描述矩形高序位修補程式。
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: 'D3DRECTPATCH_INFO 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975682"
---
# <a name="d3drectpatch_info-structure"></a>D3DRECTPATCH \_ 資訊結構

描述矩形高序位修補程式。

## <a name="syntax"></a>語法


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**StartVertexOffsetWidth**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

開始頂點位移寬度（以頂點數目為限）。

</dd> <dt>

**StartVertexOffsetHeight**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

開始頂點位移高度（以頂點數目為限）。

</dd> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

每個頂點的寬度（以頂點的數目為限）。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

每個頂點的高度（以頂點數目為限）。

</dd> <dt>

**分散**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

虛數二維頂點陣列的寬度，其佔用的空間與頂點緩衝區相同。 如需範例，請參閱下圖。

</dd> <dt>

**Basis**
</dt> <dd>

類型： **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

[**D3DBASISTYPE**](./d3dbasistype.md)列舉型別的成員，定義矩形高序位修補程式的基礎型別。



| 值                 | 支援的訂單            | 寬度和高度                  |
|-----------------------|----------------------------|-----------------------------------|
| D3DBASIS \_ 貝塞爾      | 線性、三個和 quintic | Width = height = (DWORD) order + 1 |
| D3DBASIS \_ BSPLINE     | 線性、三個和 quintic | Width = height > (DWORD) 順序  |
| D3DBASIS \_ 插補 | 立方                      | Width = height > (DWORD) 順序  |



 

</dd> <dt>

**角度**
</dt> <dd>

類型： **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

[**D3DDEGREETYPE**](./d3ddegreetype.md)列舉型別的成員，定義矩形修補程式的程度。

</dd> </dl>

## <a name="remarks"></a>備註

下圖識別指定矩形修補程式的參數。

![矩形高序位修補程式的圖表，以及指定它的參數](images/hop-rectpatch.png)

頂點緩衝區中的每個頂點都會顯示為黑色點。 在此情況下，頂點緩衝區中有20個頂點，矩形 patch 中有16個。 Stride 是頂點緩衝區寬度的頂點數目，在此案例中為五。 第一個頂點的 x 位移稱為 StartIndexVertexWidth，在此案例中為1。 第一個 patch 頂點的 y 位移稱為 StartIndexVertexHeight，在此案例中為0。

若要將個別矩形修補程式的資料流程轉譯 (非馬賽克) ，您應該將幾何轉譯為 long 窄 (1 x N) 矩形修補程式。 這類區域 (三次方貝塞爾) 的 **D3DRECTPATCH \_ 資訊** 結構會以下列方式設定。


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
