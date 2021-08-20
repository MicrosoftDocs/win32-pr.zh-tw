---
description: 驅動程式中處理資料的時間百分比。 當驅動程式正在等候其他資源時，這些統計資料可能有助於找出案例。
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: 'D3DDEVINFO_D3D9INTERFACETIMINGS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d7261096ed373620b8438ccce2d353ccf21f1c236028e8c829951fc64ee3725a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989028"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>D3DDEVINFO \_ D3D9INTERFACETIMINGS 結構

驅動程式中處理資料的時間百分比。 當驅動程式正在等候其他資源時，這些統計資料可能有助於找出案例。

## <a name="syntax"></a>語法


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a>成員

<dl> <dt>

**WaitingForGPUToUseApplicationResourceTimePercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

驅動程式花費在等候 GPU 完成使用鎖定的資源 (且未指定) 的 [D3DLOCK \_ DONOTWAIT](d3dlock.md) 時，所花費的時間百分比。

</dd> <dt>

**WaitingForGPUToAcceptMoreCommandsTimePercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

驅動程式在驅動程式可以傳送更多之前，等候 GPU 完成處理某些命令所花費的時間百分比。 這表示驅動程式的空間不足，無法將命令傳送至 GPU。

</dd> <dt>

**WaitingForGPUToStayWithinLatencyTimePercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

驅動程式花費在等候 GPU 延遲降至小於三個轉譯畫面的時間百分比。

如果應用程式是 GPU 受限的，則驅動程式必須在 GPU 于三個框架內進行時，才會停止 CPU。 這可防止應用程式將許多秒鐘的轉譯呼叫排入佇列，這可能會大幅增加使用者輸入新資料的時間，以及使用者看到該輸入的結果之間的延遲。 一般而言，驅動程式可以追蹤呼叫 [**的次數，**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 以防止佇列超過三個轉譯工作的畫面格。

</dd> <dt>

**WaitingForGPUExclusiveResourceTimePercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

驅動程式花費在等候無法進行管線處理的資源 (的時間百分比，以平行) 方式運作。 基於效能考慮，應用程式可能會想要避免使用非管線資源。

</dd> <dt>

**WaitingForGPUOtherTimePercent**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

驅動程式等候其他 GPU 處理所花費的時間百分比。

</dd> </dl>

## <a name="remarks"></a>備註

這些計量有助於識別驅動程式何時正在等候，以及它正在等待的時間。 高百分比不一定是問題。

這些系統全域計量可能會或可能不會執行。 根據特定的硬體而定，這些計量可能不會同時支援多個查詢。

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

 

 
