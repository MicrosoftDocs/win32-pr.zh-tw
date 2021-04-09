---
description: 定義目前鑲嵌模式為離散或連續模式。
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: 'D3DPATCHEDGESTYLE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854015"
---
# <a name="d3dpatchedgestyle-enumeration"></a>D3DPATCHEDGESTYLE 列舉

定義目前鑲嵌模式為離散或連續模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ 離散**
</dt> <dd>

離散邊緣樣式。 在獨立模式中，您可以指定 float 鑲嵌式，但是它會被截斷為整數。

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ 連續**
</dt> <dd>

連續邊緣樣式。 在連續模式中，會將鑲嵌指定為浮點值，而這些值可以平滑地改變，以減少「即將推出」的構件。

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，連續鑲嵌會針對相同的鑲嵌值產生與離散不同的鑲嵌模式 (這線上框模式) 更為明顯。 因此，4.0 連續與4個離散不同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




