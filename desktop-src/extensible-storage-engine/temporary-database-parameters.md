---
description: 深入瞭解：暫存資料庫參數
title: 暫存資料庫參數
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: 427ed51c2757075ccb28fd70e5554c49dc8db4e8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986821"
---
# <a name="temporary-database-parameters"></a>暫存資料庫參數


_**適用于：** Windows |Windows伺服器_

## <a name="temporary-database-parameters"></a>暫存資料庫參數

本主題包含用於暫存資料庫的參數。

*JET_paramEnableTempTableVersioning*  
46  

此參數控制臨時表中交易的使用。 當此參數為 false 時，臨時表會更快，但無法回復在交易中所做的任何更新。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>對</p> | 
| <p>輸入：</p> | <p>Boolean</p> | 
| <p>有效範圍：</p> | <p>False, True</p> | 
| <p>範圍：</p> | <p>執行個體</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>Yes</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>Yes</p> | 
| <p>可用性：</p> | <p>全部</p> | 



*JET_paramPageTempDBMin*  
19  

此參數會控制暫存資料庫的初始大小。 大小是在資料庫頁面中。 大小為零表示應該使用一般資料庫的預設大小。

小型應用程式通常需要將暫存資料庫設定為盡可能小。 將此參數設定為14將可以達到最小的暫存資料庫。 請注意，將 **JET_paramMaxTemporaryTables** 設定為零，也可以完全消除暫存資料庫。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>0</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>0-2147483647</p> | 
| <p>範圍：</p> | <p>執行個體</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>Yes</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>Yes</p> | 
| <p>會影響資源：</p> | <p>Yes</p> | 
| <p>可用性：</p> | <p>全部</p> | 



*JET_paramTempPath*  
1  

此參數表示將包含實例之暫存資料庫之資料夾或檔案的相對或絕對檔案系統路徑。 如果路徑是要包含暫存資料庫的資料夾，則必須以反斜線字元作為結尾。 暫存資料庫是用來保存在處理 ESE API 資訊呼叫、建立索引或儲存臨時表內容的過程中所產生的暫時性資料。

**注意**  如果指定相對路徑，則會相對於裝載使用資料庫引擎的應用程式之進程的目前工作目錄。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>".tmp"</p> | 
| <p>輸入：</p> | <p>路徑 (字串) </p> | 
| <p>有效範圍：</p> | <p>0–247個字元</p> | 
| <p>範圍：</p> | <p>執行個體</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>Yes</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>Yes</p> | 
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

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
