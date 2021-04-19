---
description: 自動代理快取
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: 自動代理快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0492bec116bad8a82da0e961cf6d851d27c787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984728"
---
# <a name="autoproxy-cache"></a>自動代理快取

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)函式會針對指定的 URL，以每個要求為基礎執行自動代理程式查閱。 如果傳回多個 proxy，用戶端應用程式應該在傳送要求之前測試每個 proxy (如需詳細資訊，請參閱 WinHTTP 中的自動代理程式問題中， [目前唯一支援的 Proxy 伺服器](autoproxy-issues-in-winhttp.md) 一節) 。 當用戶端指定自動 proxy 探索時，本主題中的資訊適用于 **WinHttpGetProxyForUrl** 的呼叫。

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 可選擇性地找到自動代理程式 URL，並從該網站下載自動代理程式腳本。 WinHttp 使用自動代理腳本來尋找 proxy 伺服器。 針對指定的會話，會快取自動代理程式 URL 和自動代理程式腳本。 每個會話只會快取一個自動代理程式 URL 和腳本。 一般而言，會快取自動代理腳本和 URL，直到與該電腦相關聯的 IP 位址變更為止。 如果在呼叫 **WinHttpGetProxyForUrl** 期間偵測到新的 IP 位址，則呼叫會嘗試找出新的自動代理程式 URL 和腳本，並快取結果。 每個會話只應允許一位使用者，如此一來，快取的資料就不會與電腦上的其他使用者共用。 如需詳細資訊，請參閱 [WinHTTP 會話總覽](winhttp-sessions-overview.md)。

當呼叫 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 時，如果進程外服務在使用中，則會將快取的自動代理程式 URL 和腳本提供給整部電腦使用。 但是，如果使用跨進程服務，而且 *pAutoProxyOptions* 結構中的 **fAutoLogonIfChallenged** 旗標為 true，則不會快取自動代理程式 URL 和腳本。 因此，將 **fAutoLogonIfChallenged** 成員設為 **TRUE** 時，呼叫 **WinHttpGetProxyForUrl** 會導致額外的額外負荷作業，這些作業可能會影響效能。 您可以使用下列步驟來改善效能。

**改善效能**

1.  呼叫 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) ，並將 fAutoLogonIfChallenged 參數設定為 **false**。 系統會快取自動代理程式 URL 和腳本，以供未來呼叫 **WinHttpGetProxyForUrl**。
2.  如果步驟1失敗，發生 **錯誤 \_ WINHTTP \_ 登入 \_ 失敗** 時，請呼叫 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) ，並將 **fAutoLogonIfChallenged** 成員設為 **TRUE**。

 

 



