---
description: 深入瞭解： JET_DBINFOMISC3 結構
title: JET_DBINFOMISC3 結構
TOCTitle: JET_DBINFOMISC3 Structure
ms:assetid: ffb23ac1-21ad-4dc6-98f8-aa4e6ef395ac
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294148(v=EXCHG.10)
ms:contentKeyID: 32765762
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
ms.openlocfilehash: 9b3f0d56702da29b4ddd0557c7d8f1f18e8addd8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987285"
---
# <a name="jet_dbinfomisc3-structure"></a>JET_DBINFOMISC3 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_dbinfomisc3-structure"></a>JET_DBINFOMISC3 結構

**JET_DBINFOMISC3** 結構會保存資料庫的其他相關資訊。 這是包含在資料庫標頭中的資訊。

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
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
    } JET_DBINFOMISC3;
```

### <a name="members"></a>成員

**ulVersion**

建立資料庫之資料庫引擎的原生版本。 請參閱 [JetGetVersion](./jetgetversion-function.md) ，以取得目前資料庫引擎的原生版本。

**ulUpdate**

追蹤可回溯相容的累加式資料庫格式更新。


| <p>ulVersion、ulUpdate =</p> | <p>意義</p> | 
|------------------------------|----------------|
| <p>0x620，0</p> | <p>原始作業系統 Beta 格式 (4/22/97) 。</p> | 
| <p>0x620，1</p> | <p>在目錄中新增條件式索引編制和舊的 (5/29/97) 的資料行。</p> | 
| <p>0x620，2</p> | <p>在 fLocalizedText 中新增旗標 (6/5/97) 。</p> | 
| <p>0x620、3</p> | <p>將 SPLIT_BUFFER 新增至空間樹狀結構的根頁面 (10/30/97) 。</p> | 
| <p>0x620，2</p> | <p>還原修訂以使 ESE97 維持 (1/28/98) 的向前相容性。</p> | 
| <p>0x620、3</p> | <p>將新的標記資料行新增至 catalog ( "CallbackData" 和 "CallbackDependencies" ) 。</p> | 
| <p>0x620，4</p> | <p>SLV 支援： signSLV、db 標頭中的 fSLVExists (5/5/98) 。</p> | 
| <p>0x620，5</p> | <p>新的 SLV 空間樹狀結構 (5/29/98) 。</p> | 
| <p>0x620、6</p> | <p>SLV space map (10/12/98) 。</p> | 
| <p>0x620，7</p> | <p>4位元組 IDXSEG (12/10/98) 。</p> | 
| <p>0x620、8</p> | <p> (1/25/99) 的新範本資料行格式。</p> | 
| <p>0x620、9</p> | <p>已排序的範本資料行 (6/24/99) 。</p> | 
| <p>0x620，A</p> | <p>合併的程式碼基底 (3/26/2003) 。</p> | 
| <p>0x620，B</p> | <p>新的總和檢查碼格式 (1/08/2004) 。</p> | 
| <p>0x620、C</p> | <p>將 4/8kb 頁面的最大金鑰長度增加至1000/2000 個位元組， (1/15/2004) 。</p> | 
| <p>0x620，D</p> | <p>目錄空間提示，space_header v2 (7/15/2007) 。</p> | 
| <p>0x620，E</p> | <p>將新的節點/範圍格式新增至空間管理員，將其用於空間的保留集區 (8/9/2007) 。</p> | 
| <p>0x620、F</p> | <p>將內建的 long 值壓縮 (10/30/2007) 。</p> | 
| <p>0x620，10</p> | <p>壓縮 (12/05/2007) 的分隔 long 值。</p> | 
| <p>0x620，11</p> | <p> (12/29/2007) 的大型頁面新的 LV 區塊大小。</p> | 



**signDb**

資料庫 (的簽章，包括建立時間) 。 此結構是28個位元組。

**dbstate**

這是資料庫狀態。

此成員可以使用下列選項。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_dbstateJustCreated<br />1</p> | <p>剛建立資料庫。</p> | 
| <p>JET_dbstateDirtyShutdown<br />2</p> | <p>資料庫需要執行硬或軟復原才能成為可用或可移動的。 其中一個不應嘗試移動處於此狀態的資料庫。</p> | 
| <p>JET_dbstateCleanShutdown<br />3</p> | <p>資料庫處於乾淨狀態。 您可以在沒有任何記錄檔的情況下附加資料庫。</p> | 
| <p>JET_dbstateBeingConverted<br />4</p> | <p>正在升級資料庫。</p> | 
| <p>JET_dbstateForceDetach<br />5</p> | <p>內部。</p> | 



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

**genMinRequired**

表示重新執行記錄所需的最小記錄檔產生。 這通常與檢查點產生相同。

**genMaxRequired**

表示重新執行記錄所需的最大記錄檔產生。

**logtimeGenMaxCreate**

代表 genMax 記錄檔的建立日期和時間。

**ulRepairCount**

在此資料庫上呼叫修復的次數。

**logtimeRepair**

代表上次執行修復的日期和時間。

**ulRepairCountOld**

上次磁碟重組之前，在此資料庫上執行修復的次數。

**ulECCFixSuccess**

修正一個位錯誤並產生良好頁面的次數。

**logtimeECCFixSuccess**

代表修正最後一個 bit 錯誤的日期和時間，並產生良好的頁面。

**ulECCFixSuccessOld**

代表修正一個位錯誤的次數，並在最後一次修復前產生良好的頁面。

**ulECCFixFail**

修正一個位錯誤並產生錯誤頁面的次數。

**logtimeECCFixFail**

代表修正最後一個 bit 錯誤的日期和時間，並導致錯誤的頁面。

**ulECCFixFailOld**

修正一個位錯誤的次數，並在最後一次修復前產生錯誤的頁面。

**ulBadChecksum**

找到不可更正的 ECC/總和檢查碼錯誤的次數。

**logtimeBadChecksum**

表示找到最後一個不可更正的 ECC/總和檢查碼錯誤的日期和時間。

**ulBadChecksumOld**

在最後一次修復之前發現不可更正的 ECC/總和檢查碼錯誤的次數。

**genCommitted**

目前的記錄產生。 如果 JET_paramWaypointLatency 為非零，則此值可能小於 genMaxRequired。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
