---
description: 處理著色器資料的時間百分比。
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: 'D3DDEVINFO_D3D9STAGETIMINGS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: eb4302b86d31c074f58fd003601557864aee152da9e532771336097f4228ea61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676728"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a>D3DDEVINFO \_ D3D9STAGETIMINGS 結構

處理著色器資料的時間百分比。

## <a name="syntax"></a>語法


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a>成員

<dl> <dt>

**MemoryProcessingPercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

著色器花費在記憶體存取上的時間百分比。

</dd> <dt>

**ComputationProcessingPercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

時間處理的百分比 (在暫存器中移動資料，或) 執行數學運算。

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

 

 
