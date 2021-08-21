---
description: 深入瞭解： JetBeginExternalBackupInstance 函數
title: JetBeginExternalBackupInstance 函式
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55fc5a204ce321f0be5073f2c4c9ab2a80a11a822b3bf23c87441770c3a1857b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118073016"
---
# <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance 函式

**JetBeginExternalBackupInstance** 函式會在引擎和資料庫處於線上狀態且為使用中時，起始外部備份。

**Windows xp： JetBeginExternalBackupInstance** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的資料庫實例。

針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。 在此情況下，這種全域實例的使用是隱含的。

針對 Windows XP 和更新版本，只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變體 (Windows 2000 相容性模式) 只支援一個實例。 否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。

*grbit*

指定零或多個下列選項的位群組。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>此旗標已被取代。 使用此位會導致傳回 JET_errInvalidgrbit。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>建立增量備份，而不是完整備份。 這表示只會備份自上次完整或增量備份之後的記錄檔。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>保留供未來使用。 針對 Windows XP 定義。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

因為呼叫此函式，所以系統可能會產生成功或失敗的代碼。 如需此 API 的完整錯誤清單，請參閱[可擴展的儲存體引擎錯誤碼](./extensible-storage-engine-error-codes.md)。

請參閱 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)。

#### <a name="remarks"></a>備註

**JetBeginExternalBackupInstance** 是一系列函式中的第一個函式，必須呼叫這些函式，以執行 (非 VSS 型) 備份的線上功能。 另請參閱 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) 和 [JetStopBackupInstance](./jetstopbackupinstance-function.md)。

外部備份可以用來執行完整、增量或差異備份。

備份將會是模糊的，在此情況下，備份將會與交易記錄中的單一時間點一致，但目前不可能控制確切的時間點。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p><strong>程式庫</strong></p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
