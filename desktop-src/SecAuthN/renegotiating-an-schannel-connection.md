---
description: 若要變更連接的屬性（例如，加密套件或用戶端驗證），您可以要求 &\# 0034; 重做&\# 0034; 或重新協商連接。
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: 重新交涉 Schannel 連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b904400f5a440046214c39ea736c296685e0e56859f43b3a458f621d2a07d273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919397"
---
# <a name="renegotiating-an-schannel-connection"></a>重新交涉 Schannel 連線

若要變更連接的屬性（例如，加密套件或用戶端驗證），您可以要求「重做」或重新協商連接。

如果您想要變更的屬性是以認證來控制，您必須先取得新的認證，然後再重新協商連接。 如需詳細資訊，請參閱 [取得 Schannel 認證](obtaining-schannel-credentials.md)。

若要從用戶端應用程式要求重做，請呼叫 [**InitializeSecurityCoNtext (Schannel)**](./initializesecuritycontext--schannel.md) 函數。 伺服器應用程式會呼叫 [**AcceptSecurityCoNtext (Schannel)**](acceptsecuritycontext--schannel.md) 函數。 設定參數，如下所示：

-   在 *phCoNtext* 參數中指定現有的 [*安全性內容*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY)。
-   只有在建立內容時， (用戶端) 在 *pszTargetName* 參數) 指定相同的伺服器名稱 (。
-   使用 *phCredential* 參數（如果適用）來指定新的認證。
-   如果您想要變更與認證無關的內容屬性，請使用 *fCoNtextReq* 參數來指定這些屬性。

呼叫適當的函式之後，您的應用程式應該將結果傳送至用戶端，並使用 [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) 函式繼續處理傳入訊息。

[**DecryptMessage (schannel)**](decryptmessage--schannel.md)函式在 \_ \_ 您的應用程式準備好進行應用程式時，將會傳回秒的重新協商。 當您收到 SEC 次 \_ 重新 \_ 協商傳回碼時，您的應用程式必須將 [**AcceptSecurityCoNtext (schannel)**](acceptsecuritycontext--schannel.md) (伺服器) 或 [**InitializeSecurityCoNtext (schannel)**](./initializesecuritycontext--schannel.md) (用戶端) ，並傳遞 SECBUFFER_EXTRA 中從 DecryptMessage 傳回的 SECBUFFER_TOKEN 內容。 在這個呼叫傳回值之後，請繼續進行，如同您的應用程式正在建立新的連接。

 

 
