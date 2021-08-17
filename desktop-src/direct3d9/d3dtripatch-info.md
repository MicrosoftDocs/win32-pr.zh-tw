---
description: 描述三角形高序位修補程式。
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: 'D3DTRIPATCH_INFO 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c20a846d13cd45bb8a1629fca0e958d3042aacf148c24b0633dd19fb5462bd66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850110"
---
# <a name="d3dtripatch_info-structure"></a>D3DTRIPATCH \_ 資訊結構

描述三角形高序位修補程式。

## <a name="syntax"></a>語法


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**StartVertexOffset**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

以頂點數目起始頂點位移。

</dd> <dt>

**NumVertices**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

頂點數目。

</dd> <dt>

**Basis**
</dt> <dd>

類型： **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

[**D3DBASISTYPE**](./d3dbasistype.md)列舉型別的成員，它會定義三角形高序位修補程式的基礎型別。 此成員唯一有效的值為 D3DBASIS \_ 貝塞爾。

</dd> <dt>

**角度**
</dt> <dd>

類型： **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

[**D3DDEGREETYPE**](./d3ddegreetype.md)列舉型別的成員，定義三角形高序位修補程式的程度型別。



| 值                | 頂點數目 |
|----------------------|--------------------|
| D3DDEGREE \_ 立方     | 10                 |
| D3DDEGREE \_ 線性    | 3                  |
| D3DDEGREE \_ 二次 | N/A                |
| D3DDEGREE \_ QUINTIC   | 21                 |



 

N/A-無法使用。 不支援。

</dd> </dl>

## <a name="remarks"></a>備註

例如，下圖識別三次方貝塞爾三角形修補程式的頂點順序和區段編號。 頂點順序可決定 [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)所使用的區段編號。 位移是頂點緩衝區中第一個三角形 patch 頂點的位元組數目。

![具有九個頂點的三角形高序位修補程式圖](images/hop-tripatch-info.png)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
