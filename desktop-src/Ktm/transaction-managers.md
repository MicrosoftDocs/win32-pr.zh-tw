---
description: 交易管理員 (TM) 是記錄檔的實例。 在 KTM 中，TM 物件指定了 TM 的記錄檔和一些功能。 在特定節點上通常會有許多 TM 物件。  (RMs) 的資源管理員必須與特定 TM 相關聯。
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: 交易管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313215816642201c75ae5f0facae3bf98799c8d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978926"
---
# <a name="transaction-managers"></a>交易管理員

交易管理員 (TM) 是記錄檔的實例。 在 KTM 中，TM 物件指定了 TM 的記錄檔和一些功能。 在特定節點上通常會有許多 TM 物件。  (RMs) 的資源管理員必須與特定 TM 相關聯。 有三種類型的 Tm：

-   Volatile TM，沒有記錄檔。
-   一般 TM （具有記錄檔），用於協調一或多個 RMs 的交易。
-   優質的交易管理員。

## <a name="volatile-transaction-managers"></a>Volatile 交易管理員

Volatile TM 是唯讀或暫時性 RMs 的 TM。 它沒有記錄檔，而且不會保存跨系統重新開機的交易狀態。

## <a name="transaction-managers"></a>交易管理員

Tm 有記錄、一或多個永久性或 volatile RMs，或兩者都有。 TM 會跨系統重新開機來保存交易的狀態，直到交易完成為止。 使用「假設-中止」模型，因此會回復在 TM 物件關閉時作用中但未備妥的交易。 當您第一次開啟 TM 時，必須藉由呼叫 [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) 函式來復原 tm。

## <a name="superior-transaction-managers"></a>優質的交易管理員

絕佳的 TM 是 TM，適用于其他的 tm。 它會協調交易。 它也會發出 **交易通知，讓 \_ \_** 核心交易管理員 (KTM) 的通知。 Microsoft Distributed Transaction Coordinator (DTC) ，就是絕佳 TM 的範例。 這種功能有額外的復原時間責任。 在復原期間，RM 必須先呼叫 [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) 函式來重新開啟登記。 如果認可交易，它也必須提供 (或重新傳遞) 交易的結果;藉由呼叫 [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) 函式或 [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) 函式，即可自由傳遞結果。 此義務在收到相關聯的 **交易 \_ 通知 \_ 認可 \_ 完成** 或 **交易 \_ 通知 \_ 回復 \_ 完成** 通知事件之前，不會結束。如果上層 TM 無法在復原時執行這些作業，KTM 將會清除復原階段結束時尚未接收結果的任何交易。 不過，這可能會導致交易結果不一致。

## <a name="transaction-manager-functions"></a>交易管理員函數

下列函數會與交易管理員一起使用。



| 函式                                                                            | 描述                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | 建立新的交易管理員 (TM) 物件，並傳回具有指定存取權的控制碼。  |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | 從交易管理員取得虛擬時鐘值。                                      |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | 取得指定之交易管理員的識別碼。                                   |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | 開啟現有的交易管理員。                                                         |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | 從記錄檔復原交易管理員的狀態。                                      |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | 將交易管理員的狀態從其記錄檔復原到指定的虛擬時鐘值。 |



 

 

 



