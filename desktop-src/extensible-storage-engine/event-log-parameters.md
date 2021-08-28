---
description: 深入瞭解：事件記錄檔參數
title: 事件記錄檔參數
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: 6fdf19d493e60cf229178872f7e33710210cfbec
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985331"
---
# <a name="event-log-parameters"></a>事件記錄檔參數


_**適用于：** Windows |Windows伺服器_

## <a name="event-log-parameters"></a>事件記錄檔參數

本主題包含事件記錄檔所使用的參數。

JET_paramEventLogCache  
此參數會控制記錄檔訊息快取的大小 () （以位元組為單位），此訊息會保存資料庫引擎在 eventlog 服務停止時發出的 eventlog 訊息。 當服務變成可運作時，這些快取的訊息將會清除到 eventlog。 將會捨棄任何溢位的快取訊息。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>0</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>0-2147483647</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>No</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>No</p> | 
| <p>會影響資源：</p> | <p>Yes</p> | 
| <p>可用性：</p> | <p>全部</p> | 



*JET_paramEventLoggingLevel*  
  
此參數會設定資料庫引擎發出給 eventlog 的 eventlog 訊息詳細層級。 較高的數位將會產生更詳細的事件記錄檔訊息。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>JET_EventLoggingLevelMax</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>JET_EventLoggingDisable – JET_EventLoggingLevelMax</p> | 
| <p>範圍：</p> | <p>執行個體</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>No</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



*JET_paramEventSource*  
4  

此參數會提供應用程式特定的字串，該字串將會新增至 database engine 發出的任何事件記錄檔訊息。 這可讓事件記錄檔訊息與來源應用程式輕鬆相互關聯。 如果指定了空字串 (預設) 則會使用主應用程式的可執行檔名稱。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>""</p> | 
| <p>輸入：</p> | <p>String</p> | 
| <p>有效範圍：</p> | <p>0–259個字元</p> | 
| <p>範圍：</p> | <p>執行個體</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>No</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>全部</p> | 



*JET_paramEventSourceKey*  
49  

這個參數可以用來控制 database engine 針對其事件記錄檔訊息所使用的事件記錄檔。 依預設，所有事件記錄檔訊息都會移至應用程式事件記錄檔。 如果已設定另一個事件記錄檔的登錄機碼名稱，則會改為將事件記錄檔訊息移至該處。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>""</p> | 
| <p>輸入：</p> | <p>String</p> | 
| <p>有效範圍：</p> | <p>0–259個字元</p> | 
| <p>範圍：</p> | <p>執行個體</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>No</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>全部</p> | 



*JET_paramNoInformationEvent*  
50  

當此參數為 true 時，將會隱藏資料庫引擎通常會產生的資訊事件記錄檔訊息。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>否</p> | 
| <p>輸入：</p> | <p>Boolean</p> | 
| <p>有效範圍：</p> | <p>False, True</p> | 
| <p>範圍：</p> | <p>執行個體</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>No</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>全部</p> | 



### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
