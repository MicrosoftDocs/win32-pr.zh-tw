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
ms.openlocfilehash: 455b46465733a906b879dcedc4b5a2f4e6ef1f9e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472474"
---
# <a name="meta-parameters"></a>中繼參數


_**適用于：** Windows |Windows伺服器_

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


| <p>系統參數</p> | <p>新的預設值</p> | 
|-------------------------|--------------------------|
| <p>JET_paramMaxSessions</p> | <p>30000</p> | 
| <p>JET_paramMaxOpenTables</p> | <p>2147483647</p> | 
| <p>JET_paramMaxCursors</p> | <p>2147483647</p> | 
| <p>JET_paramMaxVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramMaxTemporaryTables</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileSize</p> | <p>64</p> | 
| <p>JET_paramLogBuffers</p> | <p>1</p> | 
| <p>JET_paramDbExtensionSize</p> | <p>16</p> | 
| <p>JET_paramPageTempDBMin</p> | <p>14</p> | 
| <p>JET_paramCacheSizeMax</p> | <p>16</p> | 
| <p>JET_paramCheckpointDepthMax</p> | <p>65536</p> | 
| <p>JET_paramLRUKHistoryMax</p> | <p>10</p> | 
| <p>JET_paramOutstandingIOMax</p> | <p>16</p> | 
| <p>JET_paramStartFlushThreshold</p> | <p>1</p> | 
| <p>JET_paramStopFlushThreshold</p> | <p>2</p> | 
| <p>JET_paramNoInformationEvent</p> | <p>1</p> | 
| <p>JET_paramCacheSizeMin</p> | <p>16</p> | 
| <p>JET_paramPreferredVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileCreateAsynch</p> | <p>0</p> | 
| <p>JET_paramGlobalMinVerPages</p> | <p>1</p> | 
| <p>JET_paramPageHintCacheSize</p> | <p>32</p> | 
| <p>JET_paramDisablePerfmon</p> | <p>1</p> | 
| <p>JET_paramEnableFileCache</p> | <p>1</p> | 
| <p>JET_paramEnableViewCache</p> | <p>1</p> | 
| <p>JET_paramVerPageSize</p> | <p>1024</p> | 
| <p>JET_paramEnableAdvanced</p> | <p>0</p> | 
| <p>JET_paramCheckpointIOMax</p> | <p>8</p> | 



Small Configuration 也有其他對資料庫引擎的影響，包括：

  - 系統參數所管理的所有資源都會視需要從堆積進行配置

  - 資料庫引擎所使用的其他內部資源大小縮小

  - 將各種維護活動調整回來以避免背景執行緒活動


| | | <p>預設值：3</p> | <p>1 (舊版) </p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-1</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>是</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>從 Windows Server 2008 和 Windows Vista 開始</p> | 



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


| | | <p>預設值：3</p> | <p>是</p> | | <p>輸入：</p> | <p>Boolean</p> | | <p>有效範圍：</p> | <p>False, True</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>是</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>從 Windows Server 2008 和 Windows Vista 開始</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
