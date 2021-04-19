---
description: 解碼已簽署資料的進程。
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: 解碼簽署的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981134"
---
# <a name="decoding-signed-data"></a>解碼簽署的資料

下列一般處理常式會將 [*已簽署的資料*](../secgloss/s-gly.md) 型別解碼。

**解碼已簽署的訊息**

1.  取得編碼 BLOB 的指標。
2.  呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)，傳遞必要的引數。
3.  呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 一次，並傳入步驟2中抓取的控制碼，以及要解碼之資料的指標。 這會根據訊息類型，對訊息採取適當的動作。
4.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入步驟2中抓取的控制碼和適當的參數類型，以存取已解碼的資料。 例如，傳入 CMSG \_ content \_ PARAM 以取得已解碼內容的指標。

下列一般程式會驗證已解碼、已簽署訊息的簽章。

**驗證已解碼、已簽署訊息的簽章**

1.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入訊息控制碼和 CMSG \_ 簽署者 \_ cert \_ info \_ 參數，以從訊息取得簽署者的憑證 [**\_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 。
2.  呼叫 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 以開啟使用訊息中的憑證初始化的暫存存放區。
3.  呼叫 [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) ，以從訊息中包含的憑證取得簽署者的憑證 [**\_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 。
4.  呼叫 [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)，傳入 CMSG \_ CTRL 驗證簽章 \_ \_ 來驗證簽章。
5.  呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) 以關閉訊息。

這些程式的結果是簽章經過驗證，而且會將指標抓取至在程式的步驟4中取得的解碼訊息內容，以解碼已簽署的訊息。

如需 C 編碼的詳細資料，請參閱 [c 程式範例：簽署、編碼、解碼和驗證訊息](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)。

 

 
