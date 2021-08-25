---
description: 報告執行時間的軟體頂點處理已處理和裁剪的三角形數目。
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: 'D3DDEVINFO_D3DVERTEXSTATS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3DVERTEXSTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80edbdcdeea5df6ff020c0c4cc2179db5152c15cc4965efe6580db7fd7bdcc48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894528"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>D3DDEVINFO \_ D3DVERTEXSTATS 結構

報告執行時間的軟體頂點處理已處理和裁剪的三角形數目。

## <a name="syntax"></a>語法


```C++
typedef struct D3DDEVINFO_D3DVERTEXSTATS {
  DWORD NumRenderedTriangles;
  DWORD NumExtraClippingTriangles;
} D3DDEVINFO_D3DVERTEXSTATS, *LPD3DDEVINFO_D3DVERTEXSTATS;
```



## <a name="members"></a>成員

<dl> <dt>

**NumRenderedTriangles**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

未在此框架中裁剪的三角形總數。

</dd> <dt>

**NumExtraClippingTriangles**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

裁剪所產生的新三角形數目。

</dd> </dl>

## <a name="remarks"></a>備註

使用 debug runtime 和軟體頂點處理來取得特定場景的非裁剪和裁剪的基本專案數目。 通常會根據防護頻段 (（如果有的話）來裁剪基本專案) 。 裁剪保護區會以 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)中的 GuardBandLeft 設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
