---
description: 交易是定義工作邏輯單位的物件。
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: " (核心交易管理員的交易) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471d2ece52d510c1a77baa59ee3af980c4e4630a17d0911fdcbe590bad78903f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913878"
---
# <a name="transactions"></a>交易

交易是定義工作邏輯單位的物件。 只要有控制碼參考交易，交易就會處於作用中狀態，如果尚未認可或回復交易，則會將它視為使用中。 如果已建立交易，並且在認可或回復之前關閉了它的所有控制碼，就會回復交易。

請考慮使用者模式交易式用戶端的案例，此用戶端會建立交易來界定其作業範圍，然後在一或多個資源管理員上執行更新。 發生下列情況：

1.  用戶端會呼叫 [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) 函數來建立交易，並接收該交易的控制碼作為傳回值。

    交易可以由任意數目的進程開啟或繼承;因此，每個進程都會參與交易。 任何這些處理常式的失敗都會導致交易中止。

    此交易可能還不是持續性。 如果交易使用的是假設性中止記錄，則只有在系統失敗時，才會復原已達到備妥狀態的交易。

2.  用戶端必須明確地將交易傳遞給資源管理員。
3.  用戶端會使用一或多個 RMs （例如交易式檔案系統）來執行其所有交易作業。
4.  用戶端會呼叫 [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) 函數。
5.  資源管理員會接收來自 KTM 的通知，以準備和認可其資料。

## <a name="transactions-and-threads"></a>交易和執行緒

交易與執行緒不同。 多個執行緒或進程可以是單一交易的一部分。 相反地，執行緒可以是不同時間內數個不同交易的一部分。

## <a name="transaction-functions"></a>交易函數

下列函式會搭配交易使用。



| 函式                                                            | 描述                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | 要求認可指定的交易。                                         |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | 要求認可指定的交易。                                         |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | 建立新的交易對象。                                                             |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | 傳回指定之交易的要求資訊。                            |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | 開啟現有的交易。                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | 要求回復指定的交易。                                       |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | 要求回復指定的交易。 此函數會以非同步方式傳回。 |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | 設定指定之交易的交易資訊。                               |



 

 

 



