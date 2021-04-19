---
description: 此結構包含記憶體壓力報告的資料。
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: 'Microsoft 媒體基礎的 D3DMEMORYPRESSURE 結構 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106990511"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>Microsoft 媒體基礎的 D3DMEMORYPRESSURE 結構 (D3d9types) 

包含記憶體壓力報告的資料。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>成員

<dl> <dt>

**BytesEvictedFromProcess**
</dt> <dd>

進程在查詢期間收回的位元組數目。

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

因為慣用記憶體區段內的空間不足，所以放置在非最非最非最佳記憶體區段中的位元組總數。

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

放在非最佳記憶體中之記憶體配置的整體效率。 此值以百分比表示。 例如，值95表示放置在 nonpreferred 記憶體區段中的配置為95% 的效率。 此數位不應視為確切的度量。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端 | \[僅限 Windows 7 桌面應用程式\]                                                              |
| 最低支援的伺服器 | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]                                                 |
| 標頭                  | D3d9types (包含 D3d9)  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片結構](direct3d-video-structures.md)
</dt> <dt>

[記憶體壓力報告](memory-pressure-reporting.md)
</dt> </dl>

 

 




