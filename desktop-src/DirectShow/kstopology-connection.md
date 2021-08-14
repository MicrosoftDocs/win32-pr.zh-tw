---
description: 本主題適用于 Windows XP Service Pack 2 或更新版本。 KSTOPOLOGY \_ 連接結構描述核心串流 (KS) 篩選器內的節點連接。 節點可以連接到篩選中的另一個節點，或連接到篩選器上的釘選。
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: 'KSTOPOLOGY_CONNECTION 結構 (Ks) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: 80a7b6f046edd1cd7f602487a11d6a79c375276814f9374f4142d148699bb8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397242"
---
# <a name="kstopology_connection-structure"></a>KSTOPOLOGY \_ 連接結構

本主題適用于 Windows XP Service Pack 2 或更新版本。

**KSTOPOLOGY \_ 連接** 結構描述核心串流 (KS) 篩選器內的節點連接。 節點可以連接到篩選中的另一個節點，或連接到篩選器上的釘選。

## <a name="syntax"></a>語法


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a>成員

<dl> <dt>

**FromNode**
</dt> <dd>

連接中上游節點的索引。 如果上游連線是一個 pin，而不是節點，則值為 KSFILTER \_ node。

</dd> <dt>

**FromNodePin**
</dt> <dd>

如果 [ **FromNode** ] 欄位的值是 [KSFILTER] \_ 節點，則此欄位會指定上游釘選的索引。 否則會忽略此欄位。

</dd> <dt>

**ToNode**
</dt> <dd>

連接中下游節點的索引。 如果下游連線是一個固定的，而不是節點，則值為 KSFILTER \_ node。

</dd> <dt>

**ToNodePin**
</dt> <dd>

如果 **ToNode** 欄位的值為 KSFILTER \_ 節點，則此欄位會指定下游 pin 的索引。 否則會忽略此欄位。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Ks. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow結構](directshow-structures.md)
</dt> <dt>

[**IKsTopologyInfo：： get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




