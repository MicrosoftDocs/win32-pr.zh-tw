---
description: 深入瞭解： JET_DBINFOMISC 結構
title: JET_DBINFOMISC 結構
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
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
ms.openlocfilehash: 649e16e956e5dcd272e6201f779cdddd352a7bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510946"
---
# <a name="jet_dbinfomisc-structure"></a>JET_DBINFOMISC 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_dbinfomisc-structure"></a>JET_DBINFOMISC 結構

**JET_DBINFOMISC** 結構會保存資料庫的其他相關資訊。 這是包含在資料庫標頭中的資訊。

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
    } JET_DBINFOMISC;
```

### <a name="members"></a>成員

**ulVersion**

建立資料庫之資料庫引擎的原生版本。 請參閱 [JetGetVersion](./jetgetversion-function.md) ，以取得目前資料庫引擎的原生版本。

**ulUpdate**

追蹤可回溯相容的累加式資料庫格式更新。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ulVersion、ulUpdate =</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x620，0</p></td>
<td><p>原始作業系統 Beta 格式 (4/22/97) 。</p></td>
</tr>
<tr class="even">
<td><p>0x620，1</p></td>
<td><p>在目錄中新增條件式索引編制和舊的 (5/29/97) 的資料行。</p></td>
</tr>
<tr class="odd">
<td><p>0x620，2</p></td>
<td><p>在 fLocalizedText 中新增旗標 (6/5/97) 。</p></td>
</tr>
<tr class="even">
<td><p>0x620、3</p></td>
<td><p>將 SPLIT_BUFFER 新增至空間樹狀結構的根頁面 (10/30/97) 。</p></td>
</tr>
<tr class="odd">
<td><p>0x620，2</p></td>
<td><p>還原修訂以使 ESE97 維持 (1/28/98) 的向前相容性。</p></td>
</tr>
<tr class="even">
<td><p>0x620、3</p></td>
<td><p>將新的標記資料行新增至目錄， (&quot; CallbackData &quot; 和 &quot; CallbackDependencies &quot;) 。</p></td>
</tr>
<tr class="odd">
<td><p>0x620，4</p></td>
<td><p>SLV 支援： signSLV、db 標頭中的 fSLVExists (5/5/98) 。</p></td>
</tr>
<tr class="even">
<td><p>0x620，5</p></td>
<td><p>新的 SLV 空間樹狀結構 (5/29/98) 。</p></td>
</tr>
<tr class="odd">
<td><p>0x620、6</p></td>
<td><p>SLV space map (10/12/98) 。</p></td>
</tr>
<tr class="even">
<td><p>0x620，7</p></td>
<td><p>4位元組 IDXSEG (12/10/98) 。</p></td>
</tr>
<tr class="odd">
<td><p>0x620、8</p></td>
<td><p> (1/25/99) 的新範本資料行格式。</p></td>
</tr>
<tr class="even">
<td><p>0x620、9</p></td>
<td><p>已排序的範本資料行 (6/24/99) 。</p></td>
</tr>
<tr class="odd">
<td><p>0x623，0</p></td>
<td><p>新的空間管理員 (5/15/99) 。</p></td>
</tr>
</tbody>
</table>


**signDb**

資料庫 (的簽章，包括建立時間) 。 此結構是28個位元組。

**dbstate**

這是資料庫狀態。

此成員可以使用下列選項。

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
<td><p>JET_dbstateJustCreated<br />
1</p></td>
<td><p>剛建立資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateDirtyShutdown<br />
2</p></td>
<td><p>資料庫需要執行硬或軟復原才能成為可用或可移動的。 其中一個不應嘗試移動處於此狀態的資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateCleanShutdown<br />
3</p></td>
<td><p>資料庫處於乾淨狀態。 您可以在沒有任何記錄檔的情況下附加資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateBeingConverted<br />
4</p></td>
<td><p>正在升級資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateForceDetach<br />
5</p></td>
<td><p>內部。</p></td>
</tr>
</tbody>
</table>


**lgposConsistent**

如果資料庫處於已變更狀態，則為 Null。 這是資料庫最後一次進入正常關機狀態時所使用的記錄檔位置。

**logtimeConsistent**

如果資料庫處於已變更狀態，則為 Null。 這是資料庫上次進入正常關機狀態的時間。

**logtimeAttach**

上次使用 [JetAttachDatabase](./jetattachdatabase-function.md)連接資料庫的時間。

**lgposAttach**

上次使用 [JetAttachDatabase](./jetattachdatabase-function.md)附加資料庫時所使用的記錄檔位置。

**logtimeDetach**

上次與 [JetDetachDatabase](./jetdetachdatabase-function.md)卸離資料庫的時間。

**lgposDetach**

上次資料庫與 [JetDetachDatabase](./jetdetachdatabase-function.md)卸離時，所使用的記錄檔位置。

**signLog**

支援 ESE 基礎結構，而且無法在您的程式碼中使用。

**bkinfoFullPrev**

支援 ESE 基礎結構，而且無法在您的程式碼中使用。

**bkinfoIncPrev**

支援 ESE 基礎結構，而且無法在您的程式碼中使用。

**bkinfoFullCur**

支援 ESE 基礎結構，而且無法在您的程式碼中使用。

**fShadowingDisabled**

支援 ESE 基礎結構，而且無法在您的程式碼中使用。

**fUpgradeDb**

支援 ESE 基礎結構，而且無法在您的程式碼中使用。

**dwMajorVersion**

表示更新資料庫索引時的 Windows NT 版本號碼。 用來更新索引。

**dwMinorVersion**

表示更新資料庫索引時的 Windows NT 版本號碼。 用來更新索引。

**dwBuildNumber**

表示更新資料庫索引時的 Windows NT 版本號碼。 用來更新索引。

**lSPNumber**

表示更新資料庫索引時的 Windows NT 版本號碼。 用來更新索引。

**cbPageSize**

資料庫頁面大小。 0表示頁面大小為 4 KB。

只有當 JET_DbInfoMisc 已傳遞至 [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) 或 [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)時，才會抓取此值。

### <a name="requirements"></a>規格需求

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
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
