---
description: 深入瞭解： i/o 參數
title: I/o 參數
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 62cc1183f14e3de113ff5f34eaf6367bc2ff0f9a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981981"
---
# <a name="io-parameters"></a>I/o 參數


_**適用于：** Windows |Windows伺服器_

## <a name="io-parameters"></a>I/o 參數

本主題包含用於輸入和輸出 (i/o) 的參數。

*JET_paramAccessDeniedRetryPeriod*  
53  

**Windows XP 和更新版本：** 此參數會設定時間長度 () （以毫秒為單位），資料庫引擎會使用此時間來存取已鎖定的檔案，然後 JET_errFileAccessDenied 失敗。 這段時間延遲的設計目的，是為了解決防毒軟體的問題，這些軟體可能會在關閉後短暫開啟一些資料庫引擎的檔案。

**注意**  由於上述重試邏輯的結果，任何附加至資料庫或使用資料庫引擎所使用之記錄檔的嘗試，都會導致此大小的延遲，然後 API 呼叫才會傳回 (合法) 失敗。 如果這是常見的案例，則可以使用這個參數來關閉該延遲。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>10000</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>0-4294967295</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>Yes</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>Yes</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>Windows XP 及更新版本</p> | 



*JET_paramCreatePathIfNotExist*  
100  

當這個參數設定為 true 時，資料庫引擎所使用之檔案系統路徑中遺失的任何資料夾都會以無訊息模式建立。 否則，使用遺失檔案系統路徑的作業將會失敗，並 JET_errInvalidPath。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>否</p> | 
| <p>輸入：</p> | <p>Boolean</p> | 
| <p>有效範圍：</p> | <p>False, True</p> | 
| <p>範圍：</p> | <p>執行個體</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>Yes</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>No</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>全部</p> | 



*JET_paramEnableFileCache*  
126  

當此參數為 **True** 時，資料庫引擎會使用 Windows 檔案快取作為其所有不同檔案的讀取快取。 它也會使用它做為暫存資料庫的寫入快取，或使用已停用復原開啟的資料庫。 資料庫引擎必須停用一般資料庫、交易記錄檔和檢查點檔案的寫入快取，以保護資料庫的交易完整性。

請務必注意，使用 Windows 檔案快取會為資料庫檔案新增第二個快取的分層。 資料庫快取仍會使用自己的記憶體來快取資料庫檔案。 這種模式的目的是讓應用程式使用小型專用快取來設定 database engine，並允許 Windows 捐贈備用記憶體，以進一步改善資料庫資料的快取。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>否</p> | 
| <p>輸入：</p> | <p>Boolean</p> | 
| <p>有效範圍：</p> | <p>False, True</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>No</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>Yes</p> | 
| <p>可用性：</p> | <p>WindowsVista 和更新版本</p> | 



*JET_paramIOPriority*  
152  

此參數可控制 ESE 處理 i/o 作業的方式。 這些值可以設定為 0 (一般作業 JET_IOPriorityNormal) ，或針對低優先順序作業的 1 (JET_IOPriorityLow) 。 當優先權設定為 JET_IOPriorityLow 時，ESE 會使用 Windows Vista 中提供的新執行緒 i/o 優先權功能，來減少執行緒的 i/o 優先順序，以便在新的低優先順序發行後續的 i/o 作業。

**Windows Vista：** JET_paramIOPriority 是 Windows Vista 引進。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>0</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>0 - 1</p> | 
| <p>範圍：</p> | <p>執行個體</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>Yes</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>Windows Vista</p> | 



*JET_paramOutstandingIOMax*  
30 

此參數控制一次可在主機作業系統中佇列的資料庫檔案 i/o 數量。

較大的參數值可大幅協助大型資料庫應用程式的效能。

**Windows XP 和 Windows Server 2003：** Windows XP 和 Windows Server 2003 會忽略此參數，且不會影響資料庫引擎的操作。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p><strong>Windows 2000：</strong> 64</p><p><strong>Windows Vista：</strong> 1024</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p><strong>Windows 2000：</strong> 8 –2147483647</p><p><strong>Windows Vista：</strong> 0-65536</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>No</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>Yes</p> | 
| <p>可用性：</p> | <p>全部</p> | 



*JET_paramMaxCoalesceReadSize*  
164  

合併的讀取作業可分組的最大位元組數目。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>262144</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>0-1073741824</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteSize*  
165  

合併寫入作業可分組的最大位元組數目。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>393216</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>0-1073741824</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceReadGapSize*  
166  

結合的寫入 i/o 作業可能會有空隙的最大位元組數目。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>262144</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>0-1073741824</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteGapSize*  
167  

結合的讀取 i/o 作業可能會有空隙的最大位元組數目。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>393216</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>0-1073741824</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
