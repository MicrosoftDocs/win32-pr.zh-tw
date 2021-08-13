---
description: 使用非同步查詢機制時，由 D3DDEVINFO ResourceManager 收集的資源統計資料 \_ 。
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: 'D3DRESOURCESTATS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc992c5b8246ce302cda8924b8521c923575c8914c83b35c8c1e789e4bc1c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527470"
---
# <a name="d3dresourcestats-structure"></a>D3DRESOURCESTATS 結構

使用非同步查詢機制時，由 [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md) 收集的資源統計資料。

## <a name="syntax"></a>語法


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a>成員

<dl> <dt>

**bThrashing**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

指出是否發生節流。

</dd> <dt>

**ApproxBytesDownloaded**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

資源管理員所下載的大約位元組數目。

</dd> <dt>

**NumEvicts**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

已收回的物件數目。

</dd> <dt>

**NumVidCreates**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

在視訊記憶體中建立的物件數目。

</dd> <dt>

**LastPri**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

上次收回物件的優先順序。

</dd> <dt>

**NumUsed**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

設定至裝置的物件數目。

</dd> <dt>

**NumUsedInVidMem**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

已在視訊記憶體中設定至裝置的物件數目。

</dd> <dt>

**WorkingSet**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

視訊記憶體中的物件數目。

</dd> <dt>

**WorkingSetBytes**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

視訊記憶體中的位元組數目。

</dd> <dt>

**TotalManaged**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

受管理物件的總數。

</dd> <dt>

**TotalBytes**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Managed 物件的總位元組數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[ (Direct3D 9) 的非同步通知 ](asynchronous-notification.md)
</dt> </dl>

 

 
