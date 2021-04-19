---
description: 深入瞭解： JET_LOGINFO 結構
title: JET_LOGINFO 結構
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106982052"
---
# <a name="jet_loginfo-structure"></a>JET_LOGINFO 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_loginfo-structure"></a>JET_LOGINFO 結構

**JET_LOGINFO** 結構會傳回一組交易記錄檔的結構化資訊，這些記錄檔應該是備份檔案集的一部分。 **JET_LOGINFO** 結構是一組最基本的資訊，需要用來表示以 [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)抓取的一系列記錄，或針對使用 [JetExternalRestore2](./jetexternalrestore2-function.md)進行硬復原的指定。

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a>成員

**cbSize**

結構的大小（以位元組為單位）。

這個成員可以在未來擴充此結構，同時啟用回溯相容性。 它應該一律設定為 sizeof ( JET_LOGINFO ) 。

**ulGenLow**

還原的最低 (或最舊的) 記錄檔編號。 不帶正負號長度的完整精確度應該保留下來，但在目前的引擎版本中，這個數位是從0x00000 到0xFFFFF 的範圍內的十六進位數位。 這可能會在未來的版本中變更。

**ulGenHigh**

還原的最高 (或最新的) 記錄檔編號。 不帶正負號長度的完整精確度應該保留，但在目前的引擎版本中，這個數位是從0x00000 到0xFFFFF 的十六進位數位。 這可能會在未來的版本中變更。

**szBaseName**

用來命名交易記錄檔的前置詞。

這個成員傳回的值一律等於產生此資訊之實例 [JET_paramBaseName](./transaction-log-parameters.md) 的設定。

### <a name="remarks"></a>備註

交易記錄檔會根據實例的基底名稱和記錄檔的產生編號來命名。 名稱的格式為 BBBXXXXX。日誌。 BBB 會對應至記錄檔的基底名稱，且長度一律為三個字元。 XXXXX 對應到記錄檔的產生編號（以零填補的十六進位形式），且長度一律為五個字元。 記錄檔是由引擎永遠提供給交易記錄檔的副檔名。

建議您不要使用此結構化資訊，因為它會讓應用程式對交易記錄檔的這個命名配置具有透徹的瞭解。 如果未來的命名配置變更，則這種應用程式將無法正常運作。 您可以想像，記錄格式將會變更為在未來加入8個十六進位數位。 應用程式應該改為使用 [JetGetLogInfo](./jetgetloginfo-function.md) 所傳回之檔案名的明確清單。

### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista 或 Windows XP。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008 或 Windows Server 2003。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JET_LOGINFO_W</strong> (Unicode) 和 <strong>JET_LOGINFO_A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
