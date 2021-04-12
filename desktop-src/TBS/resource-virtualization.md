---
title: 資源虛擬化
description: 資源虛擬化
ms.assetid: ead0e99a-94da-4e80-bb68-d8f4b199173d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f340b1a1bddfb3fd591452e028c80403b9c7e02f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674079"
---
# <a name="resource-virtualization"></a>資源虛擬化

TB 的主要功能是有效率地共用某些有限的 TPM 資源：金鑰、授權和傳輸會話。

建立其中一個資源的實例時，TBS 會建立資源的虛擬實例，並在結果命令資料流程中傳回這個虛擬實例的控制碼 (而非 TPM) 所傳回的實際控制碼實例。 此 TB 會在內部維護虛擬控制碼與實際控制碼之間的對應。 如果 TPM 的空間不足以保存指定類型的更多資源，則會選擇性地儲存和收回資源的現有實例，直到 TPM 可保存新的資源為止。 ) 如果不再需要舊的資源，則會在提交命令之前，先將已儲存的內容載入 (儲存和收回其他資源。

TB 中的所有虛擬化都會代表特定的內容執行。 每個內容都只允許存取專門建立的虛擬資源，以及 TPM 上對應于這些虛擬資源的實體資源。 依預設，所有虛擬資源的總數限制為500。 您可以藉由建立或修改 **HKEY \_ LOCAL \_ MACHINE**   \\ **Software** \\ **Microsoft** \\ **Tpm** 下名為 MaxResources 的 DWORD 登錄值來改變這個數位。 您可以使用效能監視器工具來追蹤 TB 資源的數目，以觀察即時的 TB 資源使用方式。 這種限制在 Windows 8 和 Windows Server 2012 中已過時。

不是由 TB (（例如計數器和 NV 存放) 區）虛擬化的有限 TPM 資源，必須在軟體堆疊間以合作方式共用。

> [!Note]  
> 此處理虛擬化會導致在計算 HMAC 授權參數中包含金鑰控制碼的命令失敗。 如此一來，在 TB 環境中，應用程式軟體就無法使用 TPM 1.2 版中已淘汰的許多命令。

 

## <a name="resource-limits"></a>資源限制

TPM 可讓呼叫端查詢其功能，以判斷哪些空間可用於特定類型的資源。 其中某些資源限制（例如金鑰的可用空間量、授權會話，以及傳輸會話）實際上是透過虛擬化來延長。 **MaxResources** 登錄設定所控制的 TBS 限制通常遠高於基礎 TPM 硬體的實際限制。 不提供任何機制來與 TPM 硬體限制分開查詢 TBS 的限制。 Windows 8 和 Windows Server 2012 已淘汰此 TB 的限制。

## <a name="keys"></a>索引鍵

TBS 會將金鑰控制碼虛擬化，如此一來，當金鑰不在使用時，可以從 TPM 透明地卸載金鑰，並在需要時將金鑰載入回 TPM。 建立金鑰時，TBS 會將虛擬控制碼與載入的金鑰產生關聯。 資源的存留期會使用相同的虛擬控制碼。 虛擬金鑰控制碼只在建立它們的內容中有效，而相關聯的資源則不會保留到內容的存留期之外。

-   使用 TPM LoadKey2 建立金鑰 \_

    如果金鑰是使用 TPM \_ LoadKey2、TPM2 \_ CREATEPRIMARY、TPM2 \_ Load 或 TPM2 \_ LoadExternal 命令所建立，則 tb 會將傳回位元組資料流程中的控制碼取代為其選擇的虛擬金鑰控制碼。 如此一來，TBS 可確保每個虛擬控制碼都是唯一的。 如果 TBS 偵測到衝突， (極不太可能的事件) ，則會從 TPM 卸載金鑰，並通知呼叫的軟體。 然後，軟體可以重新提交作業。 您可以重複此程式，直到 TBS 取得唯一的索引鍵控制碼為止。

-   清除索引鍵

    當虛擬 \_ \_ 機從用戶端內容收到該虛擬控制碼的 TPM FLUSHSPECIFIC 或 TPM2 FlushCoNtext 訊息時，會使虛擬金鑰控制碼失效。 當收到清除訊息時，如果金鑰實際存在於 TPM 上，則會在該時間從 TPM 清除金鑰。

-   暫時移除金鑰

    從 TPM 收回金鑰以騰出空間給新的專案時，TB \_ 之前會先執行 tpm SaveCoNtext 或 TPM2 \_ CoNtextSave 命令，再將它收回。

-   還原金鑰

    當參考已載入金鑰的命令提交到 TB 時，它可確保金鑰實際上存在於 TPM 上。 如果機碼不存在，則會使用對 TPM \_ LoadCoNtext 或 TPM2 CoNtextLoad 的呼叫來還原 \_ 。 如果無法將金鑰還原至 TPM，則 TBS 會傳回 TPM \_ E \_ 無效 \_ 的 KEYHANDLE 作為 tpm 結果。

TBS 會以 TPM 上所載入金鑰的實體控制碼，取代命令資料流程中與金鑰相關聯的每個虛擬控制碼。 如果在呼叫端的內容中，以 TBS 無法辨識的虛擬控制碼來提交命令，則 TBS 會為具有 TPM \_ E 無效 KEYHANDLE 的呼叫端格式化錯誤串流 \_ \_ 。

## <a name="authorization-sessions"></a>授權會話

授權會話是藉由呼叫 TPM \_ OIAP、tpm \_ OSAP 或 tpm DSAP 所建立 \_ 。 在每個案例中，傳回位元組資料流程包含新建立之授權會話的實體 TPM 控制碼。 TBS 以虛擬控制碼取代此情況。 後續參考授權會話時，TB 會以授權會話的實體控制碼取代命令資料流程中的虛擬控制碼。 TBS 可確保虛擬授權會話的存留期與實體授權會話的存留期相符。 如果用戶端嘗試使用已過期的虛擬控制碼，則會使用錯誤 TPM INVALIDAUTHHANDLE 來格式化錯誤串流 \_ 。

會話位置會受到限制，而且此 TB 可以用來儲存授權會話內容的外部位置。 如果發生這種情況，TB 會選擇授權會話使其失效，以便能夠成功儲存新的內容。 嘗試使用舊內容的應用程式將需要重新建立授權會話。

當發生下列任何一種情況時，TBS 會使虛擬授權會話失效：

-   從 TPM 傳回的命令資料流程中，與授權會話相關聯的繼續使用旗標為 **FALSE**。
-   使用授權會話的命令會失敗。
-   執行的命令會使與命令 (（例如 TPM CreateWrapKey) ）相關聯的授權會話失效 \_ 。
-   與 OSAP 或 DSAP 會話相關聯的金鑰，會透過呼叫 TPM \_ FlushSpecific 或 TPM2 FlushCoNtext 從 tpm 收回 \_ (而不考慮此命令是否源自于 tb 或更高層級的軟體) 。

    在成功執行某些不具決定性的命令之後，將會自動重新同步處理授權會話，以確保此 TB 狀態與 TPM 狀態保持一致。 受影響的命令如下：

    -   TPM \_ ORD \_ 委派 \_ 管理
    -   TPM \_ ORD \_ 委派 \_ CreateOwnerDelegation
    -   TPM \_ ORD \_ 委派 \_ LoadOwnerDelegation

在下列每個案例中，tpm 會自動清除 TPM 上的授權會話：

-   建立授權會話

    虛擬授權會話控制碼只在建立它們的內容中有效，且相關聯的資源不會在相關聯內容的存留期間保留。

-   清除授權會話

    如果虛擬授權會話收到 \_ \_ 用戶端內容中虛擬控制碼的 TPM FLUSHSPECIFIC 或 TPM2 FlushCoNtext 命令，則會使虛擬授權會話失效。 如果接收到 flush 命令時，TPM 上實際有授權會話，則此 TB 會立即從 TPM 清除實體會話。

-   暫時移除授權會話

    從 TPM 收回授權會話以騰出空間給新的實體時，TB \_ \_ 會在該授權會話上執行 TPM SAVECONTEXT 或 TPM2 CoNtextSave。

-   還原授權會話

    當授權 TPM 命令提交至 TB 時，此 TB 可確保命令中參考的所有虛擬授權會話實際上都存在於 TPM 中。 如果有任何授權會話不存在，則 TBS 會使用 TPM \_ LoadCoNtext 或 TPM2 CoNtextLoad 的呼叫來還原它們 \_ 。 如果授權會話無法還原至 TPM，則 TBS 會傳回 TPM \_ 電子 \_ 無效 \_ 的控制碼作為 tpm 結果。

TBS 會以 TPM 上載入之授權會話的實體控制碼，取代命令資料流程中與授權會話相關聯的每個虛擬控制碼。

如果在呼叫端的內容中，以 TBS 無法辨識的虛擬控制碼來提交命令，則 TBS 會為具有錯誤 TPM \_ E \_ 無效控制碼的呼叫端格式化錯誤串流 \_ 。

## <a name="transport-sessions"></a>傳輸會話

> [!Note]  
> 如這裡所述，傳輸會話的處理是 Windows Vista 和 Windows Server 2008 專用的。

 

傳輸會話是 TPM 所提供的一種機制，可讓軟體堆疊在軟體和 TPM 之間傳遞時，將命令中的資料加密。 這可防止敵人在通過硬體匯流排時攔截資料。

> [!IMPORTANT]
> 只有承載資料會加密。 仍可以識別正在執行的命令。

 

可惜的是，這種機制也可防止 TB 檢查承載資料。 在大多數情況下，這不是問題，因為 TBS 只會修改控制碼，而不是承載資料。 不過，在 TPM LoadCoNtext 的情況下 \_ ，加密會涵蓋傳回的資源控制碼。 因此，此 TB 可防止嘗試執行 \_ 傳輸會話所涵蓋的 TPM LoadCoNtext 操作。

TBS 會在傳輸會話下封鎖下列命令：

-   TPM \_ EstablishTransport
-   TPM \_ ExecuteTransport
-   TPM \_ 終止 \_ 控制碼
-   TPM \_ LoadKey
-   TPM \_ EvictKey
-   TPM \_ SaveKeyCoNtext
-   TPM \_ LoadKeyCoNtext
-   TPM \_ SaveAuthCoNtext
-   TPM \_ LoadAuthCoNtext
-   TPM \_ SaveCoNtext
-   TPM \_ LoadCoNtext
-   TPM \_ FlushSpecific

當傳輸會話涵蓋其中任何一個命令時，會傳回 \_ \_ \_ 不支援的 tpm E EMBEDDED 命令 \_ 作為 tpm 結果。

傳輸會話控制碼會以類似于金鑰控制碼和授權控制碼的方式進行虛擬化。 TPM 上可用的已儲存傳輸會話內容位置數目有限。

如果發生下列任何一種情況，則 TBS 會使虛擬傳輸會話失效：

-   從 TPM 傳回命令資料流程中與傳輸會話相關聯的繼續使用旗標為 **FALSE**。

    如同上述的授權會話，在成功執行特定的非決定性命令之後，會自動重新同步處理傳輸會話，以確保 TB 狀態與 TPM 狀態保持一致。 受影響的命令如下：

    -   TPM \_ ORD \_ 委派 \_ 管理
    -   TPM \_ ORD \_ 委派 \_ CreateOwnerDelegation
    -   TPM \_ ORD \_ 委派 \_ LoadOwnerDelegation

在上述每一種情況下，tpm 將會自動清除 TPM 上的傳輸會話：

-   建立傳輸會話

    TBS 會為用戶端所建立的每個傳輸會話建立虛擬控制碼。 虛擬傳輸控制碼只在建立它們的內容中有效，且相關聯的資源不會在相關聯內容的存留期間保留。

-   清除傳輸會話

    如果虛擬傳輸會話 \_ 從用戶端內容收到虛擬控制碼的 TPM FlushSpecific 命令，則會使其失效。 如果接收到 flush 命令時，在 TPM 上實際存在傳輸會話，則會立即從 TPM 清除實體會話。

-   暫時移除傳輸會話

    從 TPM 收回傳輸會話以騰出空間給新的實體時，TB \_ 會在該傳輸會話上執行 TPM SaveCoNtext。

-   還原傳輸會話

    將 TPM \_ ExecuteTransport 命令提交到 tb 時，tb 可確保命令中所參考的傳輸會話實際上存在於 TPM 上。 如果傳輸會話不存在，則會使用對 TPM LoadCoNtext 的呼叫來還原 \_ 。

此 TB 會以 TPM 上載入之傳輸會話的實體控制碼，取代命令資料流程中與傳輸會話相關聯的虛擬控制碼。 如果在呼叫端的內容中，以 TBS 無法辨識的虛擬控制碼來提交命令，則會使用 TPM \_ E \_ 無效控制碼來格式化呼叫端的錯誤資料流程 \_ 。

## <a name="exclusive-transport-sessions"></a>專屬傳輸會話

專屬的包裝傳輸會話是最上層軟體的一種方式，可判斷是否有任何其他軟體在一連串命令期間存取 TPM。 它們不會防止其他軟體存取 TPM，而只是讓傳輸會話的建立者有辦法判斷是否發生其他存取。 此 TB 不會執行任何特定的動作來阻礙專屬的傳輸會話，但它與它們有點不相容。 此 TB 會嘗試以透明的方式複製 TPM 的自然行為，因此不會優先于建立專屬傳輸會話的內容中使用命令。 例如，如果用戶端 B 在用戶端 A 位於獨佔傳輸會話時提交命令，則會使用戶端 A 的獨佔傳輸會話失效。

以 TB 起始的命令也可以終止獨佔傳輸會話。 當用戶端 A 在獨佔傳輸會話中，而且用戶端執行的命令呼叫不是實際存在於 TPM 中的資源時，就會發生這種情況。 這種情況會觸發 TBS 虛擬化管理員執行 TPM \_ LoadCoNtext 命令來提供該資源，以終止用戶端 a 的獨佔傳輸會話。

 

 




