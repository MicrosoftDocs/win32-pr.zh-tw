---
description: 包含搜尋內容資訊。
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: FIND_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1ee5eb66928322019a455c78d71abf5461e56b1296ae79d94b83c40c2d45379e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404781"
---
# <a name="find_info-structure"></a>尋找 \_ 資訊結構

包含搜尋內容資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**tiIndex**
</dt> <dd>

要搜尋之索引的 **TAGID** 。

</dd> <dt>

**tiCurrent**
</dt> <dd>

目前所在專案的 **TAGID** 。

</dd> <dt>

**tiEndIndex**
</dt> <dd>

如果索引是唯一的，則為 FindFirst 之後最後一筆記錄的 **TAGID** 。

</dd> <dt>

**tName**
</dt> <dd>

要找出的專案類型。 請參閱 [標記類型](tag-types.md)。

</dd> <dt>

**dwIndexRec**
</dt> <dd>

用來追蹤下一個尋找作業應從索引中何處開始的內部計數器。

</dd> <dt>

**dwFlags**
</dt> <dd>

這個成員可以是0或 **SHIMDB \_ 索引 \_ 唯一索引 \_ 鍵** (0x00000001) ，表示這是唯一索引鍵索引。

</dd> <dt>

**ullKey**
</dt> <dd>

目前專案的索引鍵。

</dd> <dt>

**szName**
</dt> <dd>

如果標記類型為 **標記 \_ 類型 \_ STRINGREF**) ，則為目前的字串 (。

</dd> <dt>

**dwName**
</dt> <dd>

目前的 **DWORD** 值 (是否標記類型為 **標記 \_ 類型 \_ DWORD**) 。

</dd> <dt>

**pguidName**
</dt> <dd>

目前的 GUID 值 (如果標記類型是 **標記 \_ 類型 \_ BINARY** ，而且標記是 **標記 \_ 資料庫 \_ 識別碼**) 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




