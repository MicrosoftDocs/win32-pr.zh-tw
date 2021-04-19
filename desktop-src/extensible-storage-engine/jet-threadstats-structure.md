---
description: 深入瞭解： JET_THREADSTATS 結構
title: JET_THREADSTATS 結構
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979975"
---
# <a name="jet_threadstats-structure"></a>JET_THREADSTATS 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_threadstats-structure"></a>JET_THREADSTATS 結構

**JET_THREADSTATS** 結構包含目前線程上資料庫引擎所執行之工作的累計統計資料。 這項資訊會透過 [JetGetThreadStats](./jetgetthreadstats-function.md)傳回。

**Windows Vista：**  在 Windows Vista 中引進 **JET_THREADSTATS** 結構。

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a>成員

**cbStruct**

傳回 **JET_THREADSTATS** 結構的大小（以位元組為單位）。

**注意** **JET_THREADSTATS** 結構會在未來擴充，以包含更多統計資料。 新的統計資料會加入至結構的結尾，而且可以使用增加的輸出緩衝區大小來抓取。 有更多的 **cbStruct** 值可以推斷出額外的統計資料。

**cPageReferenced**

資料庫引擎在目前線程上造訪的資料庫頁面總數。

**cPageRead**

目前線程上資料庫引擎從磁片提取的資料庫頁面總數。

**cPagePreread**

目前線程上的資料庫引擎從磁片預先提取的資料庫頁面總數。

**cPageDirtied**

資料庫引擎在目前的執行緒上修改的資料庫頁面總數（沒有不成文變更）。

**cPageRedirtied**

在目前的執行緒上，資料庫引擎已修改資料庫頁面（具有不成文變更）的總數。

**cLogRecord**

目前線程上的資料庫引擎所產生的交易記錄檔記錄總數。

**cbLogRecord**

目前線程上資料庫引擎所產生的交易記錄檔記錄大小總計（以位元組為單位）。

### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JetGetThreadStats](./jetgetthreadstats-function.md)
