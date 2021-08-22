---
description: 包含 Blob 的陣列。
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: 'BLOB_TABLE 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e0615ad9c11657a47d9eaa87035207cb499634cd4ded6ae484d6f5d256c23e15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144341"
---
# <a name="blob_table-structure"></a>BLOB \_ 資料表結構

**Blob \_ 資料表** 結構包含 blob 的陣列。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**dwNumBlobs**
</dt> <dd>

許多 Blob 之後的指標。

</dd> <dt>

**hBlobs**
</dt> <dd>

BLOB 陣列的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




