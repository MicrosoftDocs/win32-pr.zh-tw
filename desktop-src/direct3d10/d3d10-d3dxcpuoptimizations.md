---
description: 啟用或停用 CPU 優化。
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: 'D3DXCpuOptimizations 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696744"
---
# <a name="d3dxcpuoptimizations-function"></a>D3DXCpuOptimizations 函式

啟用或停用 CPU 優化。

## <a name="syntax"></a>語法


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*啟用* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

**TRUE** 表示啟用 CPU 優化;否則 **為 FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DX \_ CPU \_ 優化**](d3dx-cpu-optimization.md)**

傳回偵測到的 CPU 類型，以及有哪些優化 (參閱 [**D3DX \_ CPU \_ 優化**](d3dx-cpu-optimization.md)) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
