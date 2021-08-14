---
description: 當伺服器收到來自用戶端的挑戰回應時，就會進行初始驗證。
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: 使用 Microsoft Digest 的初始驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6e9582161eb43e5109af4dc223ae150e94cbddf9b3514dabcb30339a3acc36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482618"
---
# <a name="initial-authentication-using-microsoft-digest"></a>使用 Microsoft Digest 的初始驗證

當伺服器收到來自用戶端的挑戰回應時，就會進行初始驗證。 驗證挑戰回應通常牽涉到至少兩部伺服器：

-   源伺服器-接收來自用戶端的要求併發出挑戰，然後從必須驗證的用戶端收到挑戰回應。
-   驗證服務器-接收來自源伺服器的授權資訊，並執行驗證。 此伺服器通常是支援多個來源伺服器的網域控制站。

當源伺服器收到包含摘要挑戰回應的授權標頭要求時，驗證會依照下列方式繼續進行：

-   源伺服器的身分識別是針對挑戰的 nonce 所編碼的伺服器進行檢查。
-   已檢查 nonce 中編碼的時間戳記。 如果 nonce 已過期，且使用者名稱/密碼資訊有效，則原始伺服器會發出新的摘要挑戰，並將過時的指示詞設為 "true"，藉此結束驗證。 這表示只有 nonce 「過時」，且用戶端可以使用先前回應中使用的密碼來回應新的挑戰。 如果用戶端在傳送過時挑戰的挑戰回應之後收到新的挑戰，用戶端就必須產生新的挑戰回應。
-   如果強制執行重新執行偵測，則會根據伺服器維護的 nonce 會話資料庫來檢查 nc 指示詞 (nonce 計數) 。
-   驗證服務器會識別並傳送用戶端的授權資訊。
-   驗證服務器會根據源伺服器的身分識別，檢查在 nonce 中編碼之伺服器的身分識別。
-   驗證服務器是網域控制站，可抓取使用者的密碼。
-   驗證服務器會使用授權資訊、密碼和源伺服器識別，來計算用戶端應該在挑戰回應的回應指示詞中提供的值。 驗證服務器會將計算的值與用戶端的回應進行比較，以判斷驗證是否成功或失敗。

如果驗證成功，就會將使用者的 [*安全性內容*](../secgloss/s-gly.md) 和摘要 [*工作階段金鑰*](../secgloss/s-gly.md) 傳回給源伺服器。 如果驗證失敗，則源伺服器必須產生錯誤回應。 成功驗證之後，源伺服器會將要求的資源傳回給用戶端。

驗證服務器所傳回的摘要工作階段金鑰會由源伺服器快取，以便用於驗證未來的要求。 如需詳細資訊，請參閱 [使用 Microsoft Digest 驗證後續要求](authenticating-subsequent-requests-using-microsoft-digest.md)。

 

 
