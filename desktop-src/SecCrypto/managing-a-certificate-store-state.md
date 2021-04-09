---
description: 有幾個函式會提供服務來管理憑證存放區狀態。
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: 管理憑證存放區狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d66e40817f0f92f48e8841455998eff4dbffd6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103945736"
---
# <a name="managing-a-certificate-store-state"></a>管理憑證存放區狀態

有幾個函式會提供服務來管理 [*憑證存放區*](../secgloss/c-gly.md)[*狀態*](../secgloss/s-gly.md)。

若要取得憑證的存取權，您必須透過呼叫 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 或 [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)來開啟其儲存所在的憑證存放區。

通常會在快取的記憶體中開啟憑證存放區。 它可以是新的存放區，也可以從本機登錄、在遠端電腦上的登錄、磁片檔案、PKCS \# 7 訊息或其他其他來源載入其內容。

CryptoAPI 憑證存放區功能也可讓存放區維護快取記憶體外的憑證，例如，Microsoft 憑證伺服器資料庫所提供的憑證的外部資料庫。

[**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)函式（ *lpszStoreProvider）* 的其中一個參數會決定已開啟的存放區類型，以及用來開啟該存放區的提供者。 如需使用各種提供者來開啟憑證存放區的範例，請參閱 [開啟憑證存放區的範例 C 程式碼](example-c-code-for-opening-certificate-stores.md)。

[**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) 會關閉憑證存放區。 當憑證存放區關閉時，該存放區中的每個憑證內容都會將其 [*參考計數*](../secgloss/r-gly.md) 減少一。 針對參考計數為零的憑證釋放記憶體。

\_使用 CertCloseStore 設定 CERT CLOSE \_ STORE \_ FORCE 旗標會 \_ 關閉憑證存放區，並釋出所有憑證內容的記憶體，而不論其參考計數為何。 [](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) 在某些情況下（例如在多執行緒程式中），這不是理想的做法。 如果 \_ \_ 已設定 CERT CLOSE 存放區 \_ 檢查旗標 \_ ，則會關閉存放區，但如果仍配置給參考計數尚未縮減為零之憑證的記憶體，則函式會傳回警告值。 如果憑證的參考計數大於零，則會釋放該憑證內容的複本。 使用 [**CertFreeCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)、 [**CertFreeCRLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)和 [**CertFreeCTLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) 來釋出任何保持開啟的憑證。

> [!Note]
> [*憑證內容*](../secgloss/c-gly.md)是一種類型 [**CERT \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的結構，其在其他成員中是編碼 [*憑證 BLOB*](../secgloss/c-gly.md)的指標和憑證 [**\_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)結構的指標。 **CERT \_ 資訊** 結構包含最重要的憑證資料。 如需 [*憑證*](../secgloss/c-gly.md)、 [*憑證撤銷清單*](../secgloss/c-gly.md) (CRL) 和 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 內容結構的詳細資訊，請參閱 [編碼和解碼憑證內容](encoding-and-decoding-a-certificate-context.md)。
> 
> 每個憑證內容也會包含一個 [*參考計數*](../secgloss/r-gly.md) ，指出已指派內容位址的複本數目。 每次以任何方式複製憑證內容時，其參考計數就會遞增一。 每次釋放憑證內容的指標時，憑證內容中的參考計數會減一。 當憑證內容上的參考計數到達零時，保留內容的記憶體會解除配置。 當該內容在存放區中，且使用 CERT \_ CLOSE \_ store \_ FORCE 旗標關閉存放區時，配置給憑證內容的記憶體也會解除配置 \_ 。 如果內容的記憶體已解除配置，且該內容的指標仍在使用中，則這些指標將不再有效。

 

[**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) 會增加存放區上的 [*參考計數*](../secgloss/r-gly.md) 。

[**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) 會將存放區的內容儲存至磁片檔案或記憶體位置，以及

[**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) 會在開啟時管理存放區。 當某個儲存區的保存狀態已由某個其他進程變更時，就可以通知具有開啟存放區的應用程式。 如果將新憑證從網域控制電腦複製到本機電腦存放區，就會發生這種情況。

當探索到變更時，快取的存放區可以重新同步處理其快取存放區，以符合存放區的保存狀態。 [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) 也支援在快取存放區中的變更不會自動儲存時，將快取的存放區變更複製到永久儲存區的進程。

憑證存放區類似的憑證內容可以有擴充屬性。 [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) 會將擴充屬性加入至憑證存放區。 [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) 會抓取證書存儲上設定的任何屬性。 目前，唯一預先定義的憑證存放區屬性是存放區的當地語系化名稱。

 

 
