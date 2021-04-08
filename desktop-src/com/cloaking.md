---
title: " (COM) 的掩蓋"
description: 「掩蓋」是一種 COM 安全性功能，可決定用戶端在模擬期間要將哪些身分識別導向伺服器。
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588651cfa37def4e174ef0f2fdba9b79b0c60ca8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "103853200"
---
# <a name="cloaking-com"></a> (COM) 的掩蓋

「掩蓋」是一種 COM 安全性功能，可決定用戶端在模擬期間要將哪些身分識別導向伺服器。 當設定了遮罩時，轉送伺服器會遮罩自己的身分識別，並將用戶端的身分識別提供給它代表用戶端呼叫的伺服器。 就伺服器看到的用戶端身分識別是與 proxy 相關聯的身分識別。 Proxy 的身分識別取決於數個因素，其中一個是在任何)  (設定的遮蓋類型。 安全通道安全性提供者不支援掩蓋。

下列主題提供有關掩蓋的詳細資訊：

-   [掩蓋類型](#types-of-cloaking)
-   [掩蓋如何影響用戶端身分識別](#how-cloaking-affects-client-identity)
-   [設定掩蓋](#setting-cloaking)
-   [掩蓋和模擬層級](#cloaking-and-impersonation-levels)
-   [掩蓋案例](#cloaking-scenarios)
-   [相關主題](#related-topics)

## <a name="types-of-cloaking"></a>掩蓋類型

有兩種類型的掩蓋： *靜態* 的掩蓋和 *動態* 掩蓋：

-   利用靜態掩蓋 (EOAC \_ 靜態 \_ 的掩蓋) ，伺服器會從用戶端到伺服器的第一次呼叫中看到執行緒 token。 第一次呼叫時，如果先前已在呼叫 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)期間設定 proxy 身分識別，則會使用該 proxy 身分識別。 不過，如果先前未設定 proxy 身分識別，則會使用執行緒 token。 如果沒有任何執行緒 token 存在，則會使用進程權杖。 針對所有未來的呼叫，會使用第一次呼叫所設定的身分識別。
-   使用動態掩蓋 (EOAC \_ 動態 \_ 掩蓋) ，在每次呼叫目前的執行緒權杖時 (如果有線程 token) 用來判斷用戶端的身分識別。 如果沒有線程 token，則會使用進程權杖。 這表示在模擬期間代表用戶端呼叫的伺服器會看到發出呼叫的 COM 用戶端的身分識別，這通常是所需的行為。  (當然，為了讓模擬成功，用戶端必須透過設定適當的模擬層級，讓伺服器授權單位進行模擬。 如需詳細資訊，請參閱模擬 [層級](impersonation-levels.md)。 ) 這種類型的掩蓋很昂貴。

## <a name="how-cloaking-affects-client-identity"></a>掩蓋如何影響用戶端身分識別

進行加密的呼叫，且伺服器要求用戶端輸入其身分識別時，通常會取得系結至 proxy 的身分識別。  (有時驗證服務會從真實身分識別執行轉譯，但通常 proxy 身分識別會是伺服器所見的身分識別。 ) proxy 會根據設定的遮蓋類型和其他因素，向伺服器呈現身分識別。

總而言之，用戶端的身分識別是設定掩蓋旗標的函式、進程權杖、存在或沒有線程 token 的功能，以及是否先前已設定 proxy 身分識別。 下表顯示當這些因素有所差異時，所產生的 proxy 身分識別 (用戶端身分識別) 。



| 遮蓋旗標                     | 執行緒權杖存在  | 先前設定的 Proxy 身分識別 |  (用戶端身分識別) 的 Proxy 身分識別                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| 未設定掩蓋<br/>        | 別在意<br/>  | 別在意<br/>         | 進程權杖或驗證身分識別<br/> |
| EOAC \_ 靜態 \_ 掩蓋<br/>  | 存在<br/>     | No<br/>                 | 執行緒 token<br/>                             |
| EOAC \_ 靜態 \_ 掩蓋<br/>  | 存在<br/>     | Yes<br/>                | 目前的 proxy 身分識別<br/>                   |
| EOAC \_ 靜態 \_ 掩蓋<br/>  | 不存在<br/> | No<br/>                 | 進程 token<br/>                            |
| EOAC \_ 靜態 \_ 掩蓋<br/>  | 不存在<br/> | Yes<br/>                | 目前的 proxy 身分識別<br/>                   |
| EOAC \_ 動態 \_ 掩蓋<br/> | 存在<br/>     | 別在意<br/>         | 執行緒 token<br/>                             |
| EOAC \_ 動態 \_ 掩蓋<br/> | 不存在<br/> | 別在意 <br/>        | 進程 token<br/>                            |



 

下列流程圖說明如何在不同的情況下判斷 proxy 身分識別。

![顯示判斷 proxy 身分識別流程的圖表。](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>設定掩蓋

在呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時，會將掩蓋設定為功能旗標，以設定整個進程的遮蓋。 接著會設定「掩蓋」功能，直到用戶端透過呼叫 IClientSecurity：：[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (或 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)) （可設定 proxy 的遮蓋）來變更它。

根據預設，不會設定掩飾。 若要進行設定，請將 EOAC \_ 靜態 \_ 掩蓋或 EOAC \_ 動態 \_ 掩蔽傳遞給 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)或 [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)中的 *pCapabilities* 參數。

使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)啟用靜態掩蓋時，當您第一次在 proxy 上進行呼叫時，每個 proxy 都會挑選權杖 (執行緒或進程) 。 使用 [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)啟用靜態掩蓋時，proxy 會在該時間挑選執行緒上的權杖。 如果呼叫 **SetBlanket** 時沒有可用的執行緒 token，則會使用進程權杖作為 proxy 的身分識別。 基本上， **SetBlanket** 會修正 proxy 的身分識別。

使用動態掩蓋時，無論使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 或使用 [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)來設定動態擬呼，proxy 的身分識別都會以相同的方式來決定。 如果有的話，則會使用目前的執行緒權杖;否則，會使用進程權杖。

如果透過呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定整個程式的掩蓋，而您想要使用進程權杖進行呼叫，則在進行呼叫時不會模擬。

## <a name="cloaking-and-impersonation-levels"></a>掩蓋和模擬層級

如先前所述，「掩蔽」功能會判斷在模擬期間向伺服器呈現的身分識別。 「掩蓋」提供一種方式，讓伺服器將本身以外的身分識別投射到另一部代表用戶端呼叫的伺服器。 模擬等級表示用戶端對伺服器提供多少授權單位。

沒有掩蓋的模擬可正常運作，但可能不是最佳選擇，因為在某些情況下，最終伺服器必須知道初始呼叫端的身分識別。 因為很難確保只有經過授權的用戶端可以存取遠端電腦，所以無法在不使用掩蓋的情況下達成此目的。 使用模擬而不會有掩蓋時，呈現給下游伺服器的身分識別就是立即呼叫程式的身分識別。

不過，在沒有模擬的情況下，掩蓋並不有用。 只有當用戶端已設定模擬或委派的模擬等級時，才會有意義。 使用較低的模擬層級 (，伺服器無法進行隱匿的呼叫。 ) 是否成功，取決於跨越的電腦界限數目和模擬等級，這表示伺服器必須代表用戶端執行多少授權單位。

在某些情況下，當用戶端將模擬層級設定為 RPC \_ C \_ IMP \_ 層級模擬時，伺服器就可以設定掩蓋 \_ 。 不過，某些限制是有效的。 如果原始用戶端將模擬層級設定為「RPC \_ C \_ IMP \_ 層級模擬」 \_ ，則轉送伺服器 (作為相同電腦上的用戶端) 只可在一個電腦界限上遮蓋。 這是因為模擬層級的模擬權杖只能跨一個電腦界限傳遞。 超過電腦界限後，就只能存取本機資源。 呈現給伺服器的身分識別取決於所設定的遮蓋類型。 如果未設定任何掩蓋，則呈現給伺服器的身分識別將會是發出立即呼叫的程式。

若要掩蔽多部電腦界限，您必須同時指定適當的隱匿功能旗標和委派層級模擬。 使用這種類型的模擬時，會將用戶端的本機和網路認證提供給伺服器，因此模擬權杖可以跨越任意數量的電腦界限。 同樣地，向伺服器出示的身分識別取決於設定的遮蓋類型。 如果沒有設定委派層級模擬的掩蓋，則呈現給伺服器的身分識別就是發出呼叫的進程。

例如，假設處理 A 呼叫 B，而 B 呼叫 C. B 已設定了掩蓋，而 A 已將模擬層級設定為模擬。 如果 A、B 和 C 是在同一部電腦上，則將模擬權杖從 A 傳遞到 B，然後將可運作。 但是，如果和 C 是在同一部電腦上，而 B 不是，則傳遞權杖將會在 A 和 B 之間運作，而不是從 B 到 C。從 B 到 C 的呼叫將會失敗，因為 B 在遮蓋時無法呼叫 C。 但是，如果將模擬層級設定為委派，則權杖可以從 B 傳遞到 C，而且呼叫可能會成功。

## <a name="cloaking-scenarios"></a>掩蓋案例

在下圖中，處理 A 呼叫 B，呼叫 C，呼叫 D，但未設定掩飾。 因此，每個中繼程式都會看到呼叫它的進程的身分識別。

![顯示未設定遮蓋時之進程的圖表。](images/0d2eb6cf-97d6-4c4e-b97e-abad854b1120.png)

使用靜態掩蓋時，伺服器會看到從用戶端到伺服器的第一次呼叫期間所設定的 proxy 身分識別。 下圖顯示從 B 到 C 呼叫期間設定的 proxy 身分識別範例。在後續的呼叫中，當 B 和 C 設定靜態的掩蓋時，進程 D 會看到 B 的身分識別。

![顯示靜態掩蓋進程的圖表。](images/520938e0-c4a6-4ac1-937d-02baf2007a27.png)

使用動態掩蓋時，在模擬期間呼叫端的身分識別是以目前的執行緒權杖為基礎（如果有的話）。 下圖顯示 B 和 C 設定動態遮蓋的情況，而 D 則會看見的身分識別，儘管先前的呼叫是從 B 到 C。

![顯示動態掩蓋流程的圖表。](images/d0848465-82f3-4d5a-851e-566d7800ada0.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[委派和模擬](delegation-and-impersonation.md)
</dt> </dl>

 

