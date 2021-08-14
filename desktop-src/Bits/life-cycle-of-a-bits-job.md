---
title: BITS 工作的生命週期
description: 當您建立作業時，會開始 BITS 工作的生命週期。
ms.assetid: b765a8ef-74bd-475e-9cd9-e9e2cf4f0305
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: 3182aec8eb4f4697ded8cfa5e44385e1fd34531779fa850fca8a9bbb52ac110f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173483"
---
# <a name="bits-job-states"></a>BITS 作業狀態
有四種類型 [**的位：**](/windows/desktop/api/Bits/ne-bits-bg_job_state)開始、動作、傳輸和最終。 當作業執行時，它會在不同狀態類別的狀態之間轉換。 一旦作業處於最終狀態之後，就不會移出最後的狀態，也不會顯示在 [作業列舉](/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs)中。

## <a name="state-changing-methods"></a>狀態變更方法
作業有四個狀態變更方法： [**取消**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)、 [**完成**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)、 [**繼續**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)和 [**暫**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend)止。 只要作業不是最終狀態，您就可以呼叫任何狀態變更方法。 

「 [**暫停**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend) 」方法是用來將作業切換至暫停狀態。 當工作暫停時，其所有傳輸都會停止，而且在您呼叫 Resume 之前不會繼續。
已暫停的工作只會保持暫止狀態。

[**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)方法是用來啟動已暫止的工作。 錯誤或暫時性錯誤狀態中的作業將會設定為重試。 目前處於動作狀態的作業將會維持在該狀態。

[**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)方法是用來取消作業。 狀態會切換為 [已取消]。 目前傳送的任何檔案都不會完成。 所有完全傳輸和部分傳送的檔案將會遭到刪除。

[**完成**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)的方法將會完成傳輸。 將會保留任何完整下載的檔案;未完全傳輸的檔案將會被刪除。

您必須呼叫 [取消] 或 [完成]，才能將作業移至最終狀態並清除。 未轉換為最終狀態的作業將會浪費系統資源。 BITS 最終將會自動取消舊的作業。 預設 [JobInactivityTimeout](/windows/desktop/Bits/group-policies) 是在90天后取消作業。


## <a name="starting-state"></a>開始狀態 
啟動狀態為 [已 **暫停**]。 您可以從這裡將檔案新增至作業，並設定作業和檔案屬性。 若要開始傳送作業，請在作業上呼叫 Resume。 如果您繼續執行不含任何檔案的作業，則會傳回 BG_E_EMPTY 錯誤碼，而且工作會保持暫停狀態。

## <a name="action-states"></a>動作狀態
已 **排入佇列**、 **連接** 和 **傳輸** 狀態會顯示您作業目前的內部活動。 已排入佇列的作業已準備好進行排程，可能正在等候 BITS 排程器或等候使用者登入。 正在連線的作業正在嘗試連接到伺服器，以開始傳輸檔案。 正在傳送的作業會主動上傳或下載檔案。

**暫時性錯誤** 狀態表示作業已嘗試，但無法傳送檔案。 這可能是因為網路原則的緣故。作業可能會因為目前的網路太昂貴而遭到封鎖。 系統可能也會封鎖系統原因，例如系統處於省電模式或遊戲模式，或因為沒有網際網路連線能力。 

處於暫時性錯誤狀態的工作會在適當時自動以 BITS 重試。 BITS 包含 [MinimumRetryDelay](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) 和 [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) 值，可控制重試作業的時間，以及 bits 最後將停止重試的時間。


## <a name="transferred-states"></a>已傳送狀態
當不再傳送完成時，會發生傳送的狀態。 您必須取消或完成處於此狀態的作業。 您也可以新增更多檔案來傳送和呼叫 Resume () ，但這不是常見的作法。

當傳送完成時，會發生 **錯誤** 狀態 () 不會重試，但未完全成功。 所有檔案都必須傳送才能成功;如果有任何永久失敗，作業將會發生錯誤。 您通常會呼叫 [取消] 或 [完成]，將工作移至最終狀態。 實際的差異在於，當您呼叫 Cancel 時，將會刪除任何成功傳輸的檔案，但如果您呼叫 Complete，將不會刪除任何成功傳輸的檔案。

處於錯誤狀態的原因包括 
* 在暫時性錯誤狀態中保持太長的時間， (超出 [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) 設定) 。
* 取得 BG_E_TOKEN_REQUIRED 的錯誤，並需要協助程式 [權杖](/windows/desktop/Bits/helper-tokens-for-bits-transfer-jobs)

常見的作法是重新設定錯誤作業，然後呼叫 Resume 以重試作業。 例如，您的應用程式可能需要透過 [SetRemoteName](/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename)更新檔案的遠端名稱。

當傳送完成且成功時，就會發生 **傳輸** 狀態。 您必須呼叫 Complete 才能完成工作;若為下載工作，在您呼叫 Complete 之後，將無法使用下載的檔案。 這項規則的例外狀況是 (高效能工作的工作，而且您仍應呼叫完整的) 。

## <a name="final-states"></a>最終狀態
當工作處於最終狀態時，您就無法呼叫任何狀態變更方法。 作業會在您呼叫 Complete () 之後 **認可** ，而且所有完成的下載檔案都將可供使用。 作業將會在您呼叫 Cancel () 後 **取消** ，而且所有下載的檔案都將被刪除。 


## <a name="life-cycle-of-a-bits-job"></a>BITS 工作的生命週期

當您建立作業時，會開始 BITS 工作的生命週期。 作業是包含一或多個要傳送之檔案的容器。 作業也有屬性，可指定 BITS 如何傳送檔案，以及如何與您的應用程式互動。 例如，您可以指定作業的優先順序、作業為上傳或下載作業，以及您想要接收通知的事件。

在您建立作業之後，請新增一或多個檔案 (上傳工作只能包含一個) 到該作業的檔案，並視需要變更應用程式的任何屬性值。 當您將檔案新增至工作時，請同時指定本機 (用戶端) 和遠端 (伺服器) 的檔案名。 遠端檔案名必須使用 HTTP、HTTPS 或 SMB 通訊協定。 作業內的檔案會依序 (先出) 來處理。

BITS 會在建立作業時自動暫停作業。 您必須繼續工作，才能在傳送佇列中啟用它。 您可以隨時暫停或繼續作業。 繼續作業可將工作從暫停狀態移至佇列狀態。 作業會保持佇列狀態，直到排程器判斷它是否為作業轉換檔案。 所有的前景作業都會與一個背景工作同時執行。 BITS 會以序列方式處理前景工作中的檔案。

當作業轉換檔案時，此作業會移至 [連線] 狀態，而 BITS 會連接到遠端伺服器 (在 [遠端檔案名]) 中指定。 如果 BITS 能夠連線到遠端伺服器，則作業會移至「傳輸中」狀態，直到其時間配量結束、傳輸完成、發生錯誤或應用程式暫停作業為止。

作業會在已排入佇列、連接和傳輸狀態之間移動，直到 BITS 傳送作業中的所有檔案為止。 屆時，作業會移至已傳送的狀態。 BITS 會使用迴圈配置資源排程來排程相同優先權層級的作業。 每項作業都會有一段時間來處理其檔案。 如果作業未在其時間配量內完成，則作業會回到已排入佇列的狀態，並啟動佇列中的下一個工作。 這可防止大型作業封鎖較小的作業。 作業主要是在先進先出 (FIFO) 基礎上進行處理;不過，BITS 無法保證 FIFO 處理，因為迴圈配置資源排程、作業錯誤和服務重新開機。

在應用程式呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法，將檔案的擁有權從 BITS 傳送給使用者之前，用戶端無法使用傳送的檔案。 當伺服器順利接收到檔案時，Upload 作業也會設定為 [已傳送] 狀態。 Upload-回復作業會在檔案成功傳送至伺服器之後設定為 [已傳送] 狀態，且從伺服器應用程式的回復已成功傳送至用戶端。

如果發生錯誤，工作會移至嚴重或暫時性錯誤狀態。 嚴重錯誤是指 BITS 無法從復原或需要介入來修正的錯誤。 如果應用程式能夠修正錯誤，應用程式會繼續作業，而 BITS 會將作業移至佇列狀態。 暫時性錯誤是可自行解決的錯誤。 BITS 會重試處於暫時性錯誤狀態的工作，直到傳輸成功或作業超時為止。當應用程式指定的期間內未進行任何進度時，作業就會超時。 如果作業超時，BITS 會將作業移到嚴重錯誤狀態。

如需有關工作狀態的詳細資訊，請參閱 [**BG \_ 工作 \_ 狀態**](/windows/desktop/api/Bits/ne-bits-bg_job_state)。
