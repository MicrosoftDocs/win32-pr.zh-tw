---
description: 下列函式會搭配交易使用。
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: 核心交易管理員函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221bcc13bb1cfb1f8cc67eb4d16f40a27799b921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852360"
---
# <a name="kernel-transaction-manager-functions"></a>核心交易管理員函數

下列函式會搭配交易使用。



| 函式                                                            | 描述                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | 要求認可指定的交易。                                           |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | 要求認可指定的交易。                                           |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | 建立新的交易對象。                                                               |
| [**GetTransactionId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | 取得指定之交易的識別碼。                                                   |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | 傳回指定之交易的要求資訊。                              |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | 開啟現有的交易。                                                                  |
| [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | 指出資源管理員 (RM) 已成功完成回復交易。 |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | 要求回復指定的交易。                                         |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | 要求回復指定的交易。 此函數會以非同步方式傳回。   |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | 設定指定之交易的交易資訊。                                 |



 

下列函式可用於登記。



| 函式                                                                          | 描述                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | 表示 RM 已完成認可交易管理員 (TM) 所要求的交易。                                                                                                                                                                                                                                                                        |
| [**CommitEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | 認可指定之登記的交易。                                                                                                                                                                                                                                                                                                                                |
| [**GetEnlistmentId**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | 取得指定之登記的識別碼。                                                                                                                                                                                                                                                                                                                                         |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | 建立登記、設定其初始狀態，並使用指定的存取權開啟登記的控制碼。                                                                                                                                                                                                                                                                       |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | 從 KTM 抓取修復資料的不透明結構。 藉由呼叫 [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) 函式，修復資訊會代表 RM 儲存在記錄中。 失敗之後，RM 可以使用 [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) 函式來取得資訊。 |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | 開啟現有的登錄物件，並將控制碼傳回給登記。                                                                                                                                                                                                                                                                                                         |
| [**PrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | 由高階 TM 呼叫，表示其預先準備工作已完成。                                                                                                                                                                                                                                                                                                   |
| [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | 由高階 TM 呼叫，表示其預先準備工作已完成。                                                                                                                                                                                                                                                                                                   |
| [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | 復原登記的狀態。                                                                                                                                                                                                                                                                                                                                                      |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | 要求將指定的登記轉換成隻讀登記。 唯讀登記無法參與交易的結果，也不會永久記錄以進行復原。                                                                                                                                                                                 |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | 復原與登記相關聯的指定交易。 無法針對唯讀登記呼叫此函數。                                                                                                                                                                                                                                                |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | 從 KTM 設定不透明、使用者定義的修復資料結構。 藉由呼叫 [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)，可代表 RM 將復原資訊儲存在記錄中。 失敗之後，RM 可以使用 [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) 來取得資訊。                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | 表示 RM 會拒絕單一階段要求。 當 TM 收到此呼叫時，它會起始兩階段認可，並將準備要求傳送到所有已登錄的 RMs。                                                                                                                                                                                                             |



 

下列函式會與資源管理員搭配使用。



| 函式                                                                           | 描述                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | 建立新的 RM 物件，並將 RM 與 (TM) 的交易管理員建立關聯。                                                                                  |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | 要求並收到適用于 RM 的通知。 RM 註冊程式會使用此函式來接收交易變更狀態時的通知。                 |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | 要求和接收 RM 的非同步通知。 RM 會使用此函式來註冊，以在交易變更狀態時接收通知。 |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | 開啟現有的 RM。                                                                                                                                            |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | 表示 RM 已完成所有必要的處理，以保證指定交易的認可或中止作業將會成功。           |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | 表示此 RM 已完成其 preprepare 工作，讓其他 RMs 現在可以開始進行準備作業。                                                |
| [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | 從其記錄檔復原 RM 的狀態。                                                                                                                         |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | 將指定的 i/o 完成埠與指定的 RM 產生關聯。 此埠會接收所有適用于 RM 的通知。                                             |



 

下列函數會與交易管理員一起使用。



| 函式                                                                            | 描述                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | 建立新的 TM 物件，並傳回具有指定存取權的控制碼。     |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | 從 TM 取得虛擬時鐘值。                                    |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | 取得指定 TM 的識別碼。                                 |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | 開啟現有的 TM。                                                       |
| [**OpenTransactionManagerById**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | 開啟現有的 TM。                                                       |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | 從其記錄檔復原 TM 的狀態。                                    |
| [**RenameTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | 重新命名 TM。                                                               |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | 將 TM 的狀態從其記錄檔復原到指定的虛擬時鐘值。 |



 

 

 



