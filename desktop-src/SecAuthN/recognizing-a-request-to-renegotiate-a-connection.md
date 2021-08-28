---
description: DecryptMessage (一般) 函式會針對來自訊息寄件者的重新送出要求進行陷阱。 它會藉由解密訊息資料並傳回 SEC 的重新協商值，來通知您的應用程式 \_ \_ 。
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: 辨識重新協商連接的要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 799ed36292b9542795036a697869a00176d7f068eebb6981edd28adbec2e0d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919677"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a>辨識重新協商連接的要求

[**DecryptMessage (一般)**](decryptmessage--general.md)函式會針對來自訊息寄件者的重新送出要求進行陷阱。 它會藉由解密訊息資料並傳回 SEC 的重新協商值，來通知您的應用程式 \_ \_ 。

您的應用程式必須藉由呼叫 [**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md) (伺服器來處理這類要求) 或 [**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md) (用戶端) 和傳遞 SECBUFFER_EXTRA 中的 DecryptMessage 所傳回的 SECBUFFER_TOKEN 內容。 在這個初始呼叫傳回值之後，請繼續進行，如同您的應用程式正在建立新的連接。

 

 



