---
description: 使用憑證信任清單 () Ctl 的優點之一，就是可以將應用程式設計成可以根據信任的憑證自動驗證已簽署的訊息，而不需要竟然想使用者的對話方塊。
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: 使用 Ctl 驗證已簽署的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a660bcd7e17a168b25048e61684aabc2d3ef3124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971822"
---
# <a name="verifying-signed-messages-by-using-ctls"></a>使用 Ctl 驗證已簽署的訊息

使用 [*憑證信任清單*](../secgloss/c-gly.md) () ctl 的優點之一，就是可以將應用程式設計成可以根據信任的憑證自動驗證已簽署的訊息，而不需要竟然想使用者的對話方塊。 它也可讓網路系統管理員控制來源受到信任。

您可以使用下列程式，透過 CTL 驗證已簽署訊息的簽章。

**使用 CTL 驗證已簽署的訊息**

1.  解碼訊息，如下所示：

    1.  取得已接收訊息的指標， (編碼的 [*BLOB*](../secgloss/b-gly.md)) 。
    2.  呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)，傳遞必要的引數。
    3.  呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 一次，並傳入步驟 b 中抓取的控制碼，以及要解碼之資料的指標。 這會根據訊息類型，對訊息採取適當的動作。

2.  確認已解碼、已簽署訊息的簽章，並取得簽署者憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的指標。

    這可以藉由呼叫 [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner)來完成，並傳遞在步驟1c 中取出的訊息控制碼做為 *hCryptMsg* 參數。 如果函式呼叫傳回 **TRUE**，就會驗證簽章，並在 *ppSigner* 參數中傳回簽署者 [**PCCERT \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的指標。

3.  確認簽署者是受信任的來源，如下所示：

    1.  開啟包含適當 CTL 的憑證存放區。
    2.  藉由呼叫 [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)來取得 [**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)的指標。
    3.  若要確認簽署者是受信任的來源，請呼叫 [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)，並傳遞在上一個步驟的 *pCtlCoNtext* 參數中所抓取的指標、 \_ \_ dwSubjectType 參數中的 CTL 憑證主體 \_ 類型，以及在 *pvSubject* 參數的步驟2中抓取的憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)指標。  如果函式呼叫傳回 **TRUE**，則傳遞至函式的憑證 **\_ 內容** 是 CTL 中受信任的來源。

 

 
