---
description: 資源管理員
ms.assetid: c717b731-cf0b-45cb-bbff-695410fcf6ce
title: 資源管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d32d697d58705760002065d005f5927717055f235358c12fd0629de86e14b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870018"
---
# <a name="resource-managers"></a>資源管理員

資源管理員會使用交易管理員記錄來追蹤交易狀態。 資源管理員在處理交易時的動作如下：

-   用戶端會明確將交易傳遞給 RM。
-   RM 會使用 [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)在交易中登記。
-   然後，使用者可以繼續執行任何操作。
-   當使用者呼叫 CommitTransaction 時，KTM 會將準備 \_ 交易通知傳送至 RM。 此時，RM 會將認可交易所需的任何變更排清至磁片，但可能會失敗。 如果這些作業成功，RM 會藉由呼叫 [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)來指示它已完成準備作業。 如果這些作業失敗，RM 會藉由呼叫 [**RollBackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)來回應。
-   資源管理員會收到準備通知。
-   資源管理員會將任何與交易相關聯的資料排清至其一般記錄服務記錄檔。
-   資源管理員會呼叫 [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) 函數，並等候接收來自 KTM 的交易結果。
-   視交易的結果而定，資源管理員會收到認可或回復通知事件。 如果 resource manager 收到認可通知，它會進行永久變更，並藉由呼叫 [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) 函式來通知 KTM。 如果資源管理員收到復原通知，它會捨棄所有變更，並還原為任何交易變更之前存在的狀態，並藉由呼叫 [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)來通知 KTM。

## <a name="resource-manager-functions"></a>Resource Manager 函式

下列函式會與資源管理員搭配使用。



| 函式                                                                           | 描述                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | 建立新的資源管理員 (RM) 物件，並將 RM 與交易管理員 (TM) 建立關聯。                                                                               |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | 要求和接收資源管理員 (RM) 的通知。 RM 註冊程式會使用此函式來接收交易變更狀態時的通知。            |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | 要求和接收資源管理員 (RM) 的非同步通知。 RM 註冊程式會使用此函式來接收交易變更狀態時的通知。 |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | 開啟現有的資源管理員 (RM) 。                                                                                                                                         |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | 指出資源管理員 (RM) 已完成所有必要的處理，以保證指定交易的認可或中止作業將會成功。        |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | 表示此 resource manager 已完成其 preprepare 工作，讓其他資源管理員現在可以開始進行準備作業。                                    |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | 將指定的 i/o 完成埠與指定的資源管理員 (RM) 產生關聯。 此埠會接收所有適用于 RM 的通知。                                          |



 

 

 



