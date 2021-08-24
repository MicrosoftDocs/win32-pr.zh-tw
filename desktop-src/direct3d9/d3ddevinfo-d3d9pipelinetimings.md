---
description: 管線中處理資料的時間百分比。
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: 'D3DDEVINFO_D3D9PIPELINETIMINGS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4d938fd2e1ca0f52d2ea7787f54b430a84907ad5f04f066bc90f0867825745a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676738"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>D3DDEVINFO \_ D3D9PIPELINETIMINGS 結構

管線中處理資料的時間百分比。

## <a name="syntax"></a>語法


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a>成員

<dl> <dt>

**VertexProcessingTimePercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

執行頂點著色器所花費的時間百分比。

</dd> <dt>

**PixelProcessingTimePercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

花費在執行圖元著色器的時間百分比。

</dd> <dt>

**OtherGPUProcessingTimePercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

執行其他處理所花費的時間百分比。

</dd> <dt>

**GPUIdleTimePercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

未處理任何時間的時間百分比。

</dd> </dl>

## <a name="remarks"></a>備註

為了達到最佳效能，建議使用平衡負載。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
