---
description: CAPICOM 使用數位憑證來建立簽章、建立封包訊息時加密會話加密金鑰，以及在收到包訊息時將加密的工作階段金鑰解密。
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: 使用憑證存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f687286d40e64e590079d872a0134742d552b66a9926a1febeb5c42ae2ad7566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971610"
---
# <a name="using-certificate-stores"></a>使用憑證存放區

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

CAPICOM 使用 [*數位憑證*](../secgloss/d-gly.md) 來建立簽章、建立封包訊息時加密會話加密金鑰，以及在收到包訊息時將加密的工作階段金鑰解密。 根據預設，CAPICOM 會使用我存放區中的憑證，其具有相關聯的私密金鑰來建立 [*數位簽章*](../secgloss/d-gly.md) 和工作階段金鑰解密。 在大多數情況下，應用程式永遠不需要開啟或直接處理憑證存放區。

不過，建立封裝訊息的應用程式會使用每個預定的封包訊息收件者的 [*公開金鑰*](../secgloss/p-gly.md) 。 這些金鑰是取自預定收件者的憑證。 因此，若要建立一組預定收件者的封包訊息，則會在憑證存放區中收集這些收件者的憑證。

下表列出一般保存在使用者工作站上的標準憑證存放區。



| 市集        | Description                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| My           | 包含個人憑證。 這些憑證通常會有相關聯的私密金鑰。                                                                                                                                                                                                                                                                             |
| 其他人 | 包含使用者通常會將封包訊息傳送至或從中接收簽署訊息的憑證。                                                                                                                                                                                                                                                     |
| Ca 和根目錄  | 包含使用者 [*信任的證書*](../secgloss/r-gly.md) 頒發機構單位頒發證書給其他人的憑證。 這些存放區中的憑證通常是由作業系統或使用者的網路系統管理員所提供。 根存放區中的憑證通常是自我簽署的。 |



 

您 \_ \_ 可以為字串提供不同的存放區名稱，以建立、開啟及保存其他的 CAPICOM 目前使用者存放區。 如果該名稱的存放區不存在，就會建立並開啟空的存放區。 如果存放區存在，則會開啟該存放區，而且目前儲存在存放區中的任何憑證都可供使用。

下列各節顯示憑證存放區工作的範例：

-   [開啟 Active Directory 儲存和正在抓取憑證](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [將憑證新增至憑證存放區](adding-certificates-to-a-certificate-store.md)
-   [使用不同位置的商店](using-stores-in-different-locations.md)
-   [收集和驗證憑證](collecting-and-verifying-certificates.md)

 

 
