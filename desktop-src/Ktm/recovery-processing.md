---
description: 在中斷正常交易處理的任何類型的失敗之後，KTM 和每個資源管理員都必須執行復原作業。 復原是交易參與者在每個交易狀態的一致觀點上抵達的進程。
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: 復原處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8e74d4f8bff3e56af03b017522212e7a02e232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988764"
---
# <a name="recovery-processing"></a>復原處理

在中斷正常交易處理的任何類型的失敗之後，KTM 和每個資源管理員都 *必須執行復原* 作業。 復原是交易參與者在每個交易狀態的一致觀點上抵達的進程。

資源管理員可能不 *確定* 交易的結果，也就是當失敗時，他們收到交易 \_ 通知 \_ 準備通知、已準備好儲存，但尚未收到 (或已接收但未記錄) 交易的最終結果。 同樣地，如果交易已備妥，但尚未收到 (或已接收但未記錄) 結果，則可不確定 KTM。 復原時，所有已傳送但未認可的結果都必須重新傳送。 例如，如果資源管理員收到交易 \_ 通知 \_ 認可通知並呼叫 [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) 函式，RM 可能仍會在復原時收到重複的交易 \_ 通知 \_ 認可通知。

為了讓交易在資源管理員或系統失敗後正確復原，每次資源管理員都必須在每次啟動時執行下列動作：

1.  呼叫 [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) 函式，以使用其唯一的持續名稱重新開啟其 resource manager 控制碼。 這會通知 KTM，資源管理員正在執行，且可供執行復原。 如果沒有任何登記要復原， **OpenResourceManager** 的呼叫可能會失敗。 呼叫 [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) 以重新建立 RM 物件。
2.  呼叫 [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)。 資源管理員會針對需要執行復原作業的每個登錄接收 [**交易 \_ 通知 \_ 復原**](notification-mask.md) 通知事件，後面接著交易 \_ 通知 \_ 上次 \_ 復原。 通知事件包含交易和登記的全域唯一識別碼。
3.  呼叫 [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) 函式，以重新開啟 resource MANAGER 收到交易 \_ 通知復原通知的每個登記控制碼 \_ 。
4.  針對 [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)開啟的每個登記，呼叫 [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)。 這會導致交易 \_ 通知 \_ 認可或交易 \_ 通知 \_ INDOUBT 通知重新傳遞。
5.  如果 RM 收到交易 \_ 通知 \_ 認可，rm 可以藉由呼叫 [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)來完成交易。

    如果 RM 收到交易 \_ 通知 \_ INDOUBT，rm 應該等待結果通知抵達。

6.  對於 RM 不會收到交易通知復原通知的任何交易， \_ \_ 但先前收到的交易 \_ 通知 \_ 的準備通知，RM 應該處理交易，就如同已回復一樣。

> [!Note]
>
> 資源管理員可在執行復原的過程中，登記或建立新的交易。

 

KTM 使用 *假設的 abort* 交易模型。 下列案例說明這種行為。 假設 KTM 和資源管理員存在於同一部電腦上。 假設 KTM 發出交易的準備通知，但在 KTM 記錄準備通知之前，系統損毀。 進一步假設資源管理員會在系統損毀之前，收到並記錄準備通知。 系統還原之後，KTM 就不知道交易，因為它永遠不會記錄準備階段。 資源管理員已瞭解交易，因為它已接收、處理和記錄準備通知。 當 KTM 發出其復原通知時，資源管理員不會包含有問題之交易的修復通知。 使用假設性中止模型，在此情況下，資源管理員會將備妥的交易視為在交易未收到執行復原的通知時中止。

 

 



