---
description: 除了憑證和憑證撤銷清單 (CRL) ，CryptoAPI 憑證存放區也支援 (CTL) 的憑證信任清單。
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: 憑證信任清單總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7906f02e9af3534445c5b1d6a48c94653feb78b57c71a23acfd9af51477cd050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771104"
---
# <a name="certificate-trust-list-overview"></a>憑證信任清單總覽

除了憑證和 [*憑證撤銷清單*](../secgloss/c-gly.md) (CRL) ， [*CryptoAPI*](../secgloss/c-gly.md) [*憑證存放區*](../secgloss/c-gly.md) 也支援 (CTL) 的 [*憑證信任清單*](../secgloss/c-gly.md) 。 CTL 是由受信任實體所簽署之預先定義的專案清單。 CTL 是憑證的 [*雜湊*](../secgloss/h-gly.md) 清單或檔案名清單。 清單中的所有專案都會由受信任的簽署實體進行驗證和核准。 [**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)結構類似于憑證和 CRL 內容結構。 CTL 內容可以保存到憑證存放區。

CryptoAPI CTL 是受信任實體簽署的專案清單。 專案清單可以是任何專案，例如憑證的雜湊清單或檔案名清單。 在大部分的情況下，CTL 是雜湊的憑證內容清單。 清單中的所有專案都會通過簽署實體的驗證和核准。 Ctl 的主要用途是使用 CTL 作為受信任 [*根憑證*](../secgloss/r-gly.md)的來源，以驗證已簽署的訊息。

[**Ctl \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)結構類似于憑證和 crl 內容結構; 不過，與憑證和 crl 內容結構不同的是， **Ctl \_ 內容** 結構包含 **hCryptMsg** 成員。 這個控制碼是藉由呼叫任何傳回 **ctl \_ 內容** 結構的函式來開啟，讓您可以使用訊息函數來驗證 CTL 的簽章。 這是必要的驗證，以確保 CTL 不是惡意實體所種植的假 CTL。

如需建立已簽署 CTL 並將其儲存至憑證存放區的程式，請參閱 [建立、簽署和儲存 ctl](creating-signing-and-storing-a-ctl.md)。 另請參閱 [驗證 CTL](verifying-a-ctl.md) 和使用 ctl 進行逐步驗證程式來 [驗證已簽署的訊息](verifying-signed-messages-by-using-ctls.md) 。

 

 
