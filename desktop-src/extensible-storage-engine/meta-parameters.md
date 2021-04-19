---
description: 深入瞭解：中繼參數
title: 中繼參數
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
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
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986314"
---
# <a name="meta-parameters"></a>中繼參數


_**適用于：** Windows |Windows Server_

## <a name="meta-parameters"></a>中繼參數

本主題包含用來控制其他參數的參數。

JET_paramConfiguration  
129  
此參數會針對整組系統參數公開多組預設值。 當此參數設定為特定設定時，所有系統參數值都會重設為該設定的預設值。 如果設定特定實例的設定，則全域系統參數將不會重設為其預設值。

此外，參數本身也可能對資料庫引擎的行為產生其他影響。

目前有兩個支援的設定：

  - Small Configuration (0) ：資料庫引擎已針對記憶體使用量優化。

  - 舊版設定 (1) ：資料庫引擎有其傳統預設值。

Small Configuration 會將下列系統參數的預設值變更為指定的值：

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>系統參數</p></th>
<th><p>新的預設值</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_paramMaxSessions</p></td>
<td><p>30000</p></td>
</tr>
<tr class="even">
<td><p>JET_paramMaxOpenTables</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramMaxCursors</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="even">
<td><p>JET_paramMaxVerPages</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramMaxTemporaryTables</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="even">
<td><p>JET_paramLogFileSize</p></td>
<td><p>64</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramLogBuffers</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>JET_paramDbExtensionSize</p></td>
<td><p>16</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramPageTempDBMin</p></td>
<td><p>14</p></td>
</tr>
<tr class="even">
<td><p>JET_paramCacheSizeMax</p></td>
<td><p>16</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCheckpointDepthMax</p></td>
<td><p>65536</p></td>
</tr>
<tr class="even">
<td><p>JET_paramLRUKHistoryMax</p></td>
<td><p>10</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramOutstandingIOMax</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>JET_paramStartFlushThreshold</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramStopFlushThreshold</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>JET_paramNoInformationEvent</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCacheSizeMin</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>JET_paramPreferredVerPages</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramLogFileCreateAsynch</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>JET_paramGlobalMinVerPages</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramPageHintCacheSize</p></td>
<td><p>32</p></td>
</tr>
<tr class="even">
<td><p>JET_paramDisablePerfmon</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramEnableFileCache</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>JET_paramEnableViewCache</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramVerPageSize</p></td>
<td><p>1024</p></td>
</tr>
<tr class="even">
<td><p>JET_paramEnableAdvanced</p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCheckpointIOMax</p></td>
<td><p>8</p></td>
</tr>
</tbody>
</table>


Small Configuration 也有其他對資料庫引擎的影響，包括：

  - 系統參數所管理的所有資源都會視需要從堆積進行配置

  - 資料庫引擎所使用的其他內部資源大小縮小

  - 將各種維護活動調整回來以避免背景執行緒活動

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>1 (舊版) </p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-1</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>從 Windows Server 2008 和 Windows Vista 開始</p></td>
</tr>
</tbody>
</table>


JET_paramEnableAdvanced  
130  
這個參數是用來控制 database engine 接受或拒絕系統參數子集之變更的時間。 此參數會搭配 JET_paramConfiguration 使用，以防止某些系統參數從選取的設定的預設值中移除。

當此參數設定為 False 時，將會保護下列系統參數，不要設定：

  - JET_paramMaxSessionsfon

  - JET_paramMaxOpenTables

  - JET_paramPreferredMaxOpenTables

  - JET_paramMaxCursors

  - JET_paramMaxVerPages

  - JET_paramMaxTemporaryTables

  - JET_paramLogBuffers

  - JET_paramWaitLogFlush

  - JET_paramLogCheckpointPeriod

  - JET_paramLogWaitingUserMax

  - JET_paramDbExtensionSize

  - JET_paramPageTempDBMin

  - JET_paramPageFragment

  - JET_paramBatchIOBufferMax

  - JET_paramCacheSizeMax

  - JET_paramLRUKCorrInterval

  - JET_paramLRUKHistoryMax

  - JET_paramLRUKPolicy

  - JET_paramLRUKTimeout

  - JET_paramLRUKTrxCorrInterval

  - JET_paramOutstandingIOMax

  - JET_paramStartFlushThreshold

  - JET_paramStopFlushThreshold

  - JET_paramCacheSize

  - JET_paramCacheSizeMin

  - JET_paramPreferredVerPages

  - JET_paramBackupChunkSize

  - JET_paramBackupOutstandingReads

  - JET_paramLogFileCreateAsynch

  - JET_paramRecordUpgradeDirtyLevel

  - JET_paramGlobalMinVerPages

  - JET_paramPageHintCacheSize

  - JET_paramVersionStoreTaskQueueMax

  - JET_paramDBAPageAvailMin

  - JET_paramMaxRandomIOSize

  - JET_paramCachedClosedTables

  - JET_paramEnableFileCache

  - JET_paramEnableViewCache

  - JET_paramVerPageSize

  - JET_paramCheckpointIOMax

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>對</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>從 Windows Server 2008 和 Windows Vista 開始</p></td>
</tr>
</tbody>
</table>


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

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
