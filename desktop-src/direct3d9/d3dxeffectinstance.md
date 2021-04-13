---
description: 用於管理一組預設效果參數的資料類型。
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: 'D3DXEFFECTINSTANCE 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322931"
---
# <a name="d3dxeffectinstance-structure"></a>D3DXEFFECTINSTANCE 結構

用於管理一組預設效果參數的資料類型。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a>成員

<dl> <dt>

**pEffectFilename**
</dt> <dd>

類型： **LPSTR**

</dd> <dd>

效果檔案的名稱。

</dd> <dt>

**NumDefaults**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

預設參數的數目。

</dd> <dt>

**pDefaults**
</dt> <dd>

類型： **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**

</dd> <dd>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)元素陣列的指標，其中每個專案都包含效果參數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果結構](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
