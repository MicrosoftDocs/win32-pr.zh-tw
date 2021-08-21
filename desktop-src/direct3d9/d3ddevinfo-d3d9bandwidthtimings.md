---
description: 協助您瞭解應用程式效能的輸送量計量。
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: 'D3DDEVINFO_D3D9BANDWIDTHTIMINGS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f9c92a3eae10ef289e53764c7568f826640edf66c3351edaadf3d922515a3eda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565028"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS 結構

協助您瞭解應用程式效能的輸送量計量。

## <a name="syntax"></a>語法


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a>成員

<dl> <dt>

**MaxBandwidthUtilized**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

從主機 CPU 到 GPU 的頻寬或最大資料傳輸速率。 這通常是連接 CPU 和 GPU 的 PCI 或 AGP 匯流排的頻寬。

</dd> <dt>

**FrontEndUploadMemoryUtilizedPercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

將資料從主機 CPU 上傳至 GPU 時的記憶體使用量百分比。

</dd> <dt>

**VertexRateUtilizedPercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

頂點輸送量百分比。 這是與理論最大頂點處理速率相較之下，所處理的頂點數目。

</dd> <dt>

**TriangleSetupRateUtilizedPercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

三角形的設定輸送量百分比。 這是與理論最大三角形設定速率相較之下，針對點陣設定的三角形數目。

</dd> <dt>

**FillRateUtilizedPercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

圖元填滿輸送量百分比。 這是相較于理論圖元填滿而填滿的圖元數目。

</dd> </dl>

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

 

 
