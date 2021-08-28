---
description: 深入瞭解：錯誤處理參數
title: 錯誤處理參數
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
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
ms.openlocfilehash: 698854aa81ddd7a44fcf58dd250444e657d44a0c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982011"
---
# <a name="error-handling-parameters"></a>錯誤處理參數


_**適用于：** Windows |Windows伺服器_

## <a name="error-handling-parameters"></a>錯誤處理參數

本主題包含用於錯誤處理的參數。

*JET_paramErrorToString* 70  

這個參數可以用來將 [JET_ERR](./jet-err.md) 轉換成字串。 這是使用 [JetGetSystemParameter](./jetgetsystemparameter-function.md) 的特殊呼叫來完成，其中整數輸出緩衝區包含要轉換 (為輸入參數的 [JET_ERR](./jet-err.md) 值) 而且字串輸出緩衝區會傳回相符的錯誤字串。 字串看起來會像這樣：「JET_errSuccess，成功的作業」。 字串是由字串的符號名稱、逗號，以及錯誤的簡單文字描述所組成。 描述字串本身可以包含逗號。 如果無法辨識錯誤，則字串會是「未知的錯誤，未知的錯誤」。

**注意**  此參數是唯讀的。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>特殊</p> | 
| <p>輸入：</p> | <p>特殊</p> | 
| <p>有效範圍：</p> | <p>特殊</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>No</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>No</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>No</p> | 
| <p>影響效能：</p> | <p>No</p> | 
| <p>會影響資源：</p> | <p>No</p> | 
| <p>可用性：</p> | <p>全部</p> | 


*JET_paramExceptionAction*  
98  

此參數會控制資料庫引擎擲回例外狀況時所發生的狀況，或資料庫引擎所呼叫的程式碼。 當設定為 JET_ExceptionMsgBox 時，會擲回任何例外狀況至 Windows 未處理的例外狀況篩選準則。 這會導致應用程式失敗時處理例外狀況。 其目的是要避免應用程式程式碼錯誤地嘗試攔截並忽略 database engine 所產生的例外狀況。 因為可能發生資料庫損毀，所以無法允許這種情況。 如果應用程式希望適當地處理這些例外狀況，則可以將此參數設定為 JET_ExceptionNone 來停用保護。


| 標籤 | 值 |
|--------|-------|
| <p>預設值：3</p> | <p>JET_ExceptionMsgBox</p> | 
| <p>輸入：</p> | <p>整數</p> | 
| <p>有效範圍：</p> | <p>JET_ExceptionMsgBox，JET_ExceptionNone</p> | 
| <p>範圍：</p> | <p>全球</p> | 
| <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p><strong>Windows 2000、Windows XP 和 Windows Server 2003：</strong> 不</p><p><strong>Windows Vista：</strong> 是的</p> | 
| <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p><strong>Windows 2000、Windows XP 和 Windows Server 2003：</strong> 不</p><p><strong>Windows Vista：</strong> 是的</p> | 
| <p>會影響實體版面配置：</p> | <p>No</p> | 
| <p>會影響可靠性：</p> | <p>Yes</p> | 
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

[錯誤處理常數](./error-handling-constants.md)  
[可擴充的儲存體引擎錯誤碼](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
