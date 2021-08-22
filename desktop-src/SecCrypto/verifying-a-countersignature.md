---
description: 說明如何使用 CryptMsgVerifyCountersignatureEncoded 來驗證副署。
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: 驗證副署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23163c7b1d4345908b24fed36b6fa23bdf2cf7c46dd3faa1beaa99c76d6f0ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896242"
---
# <a name="verifying-a-countersignature"></a>驗證副署

**驗證副署**

1.  呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) 以取得已簽署訊息的控制碼。
2.  取得 countersigner 憑證 ( [**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)) 的指標。
3.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) 以從訊息中取出簽署者資訊。
4.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) 以從訊息中取出 [*副署*](../secgloss/c-gly.md) 。
5.  呼叫 [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) 來驗證副署。

如果 [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) 函式呼叫成功，則會驗證 [*副署*](../secgloss/c-gly.md) 。

 

 
