---
description: 密碼編譯訊息語法可以用來編碼封包訊息。
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: 編碼封包資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dc20fc7483ba1ef364d8b59824d26bd14d458d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556585"
---
# <a name="encoding-enveloped-data"></a>編碼封包資料

封包資料包含一或多個收件者之任何類型和加密內容加密工作階段金鑰的加密內容。 封包訊息會保留訊息秘密的內容，並只允許指定的人員或實體取得內容。

 (CMS) 的密碼編譯訊息語法可以用來編碼封包訊息。 CMS 支援三種金鑰管理技術：金鑰傳輸、金鑰協定和先前散發的對稱金鑰加密金鑰 (KEK) 。 先前散發的對稱 KEK 也稱為「郵寄清單金鑰散發」。

在這三種技術中，會產生單一工作階段金鑰來加密封包訊息。 金鑰管理問題會處理寄件者加密工作階段金鑰的方式，並由接收者解密。 您可以使用混合的金鑰管理技術，將單一加密的訊息散發給許多收件者。

金鑰傳輸金鑰管理使用預定接收者的公開金鑰來加密工作階段金鑰。 接收者會使用與用來加密的公開金鑰相關聯的私密金鑰來解密工作階段金鑰。 然後接收者會使用解密的工作階段金鑰來解密封包資料。 使用金鑰傳輸時，接收者尚未確認傳送端身分識別的資訊。

在金鑰協定管理中，會產生暫時的暫時 Diffie-Hellman 私密金鑰，並使用此金鑰來加密工作階段金鑰。 與暫時私密金鑰對應的公開金鑰會包含在郵件的收件者資訊中。 收件者會使用收到的暫時金鑰來解密工作階段金鑰，並使用此解密的工作階段金鑰來解密封包訊息。 使用暫時金鑰協定搭配接收者的私密金鑰時，訊息接收者會在傳送者的身分識別上確認資訊。

針對使用先前分散式 [*對稱金鑰*](../secgloss/s-gly.md)的金鑰管理，每個訊息都包含以先前分散式金鑰加密金鑰加密的內容加密金鑰。 接收者會使用先前散發的金鑰加密金鑰來解密內容加密金鑰，然後使用解密的內容加密金鑰來解密封包訊息。

下圖顯示用於編碼封包資料的一般 CMS 事件序列。

![編碼封包資料](images/envelmsg.png)

-   將會取出 [*純文字*](../secgloss/p-gly.md) 訊息的指標。
-   產生對稱 ([*會話*](../secgloss/s-gly.md)) 金鑰。
-   [*對稱金鑰*](../secgloss/s-gly.md)和指定的加密演算法會用來加密訊息資料。
-   即會開啟 [*憑證存放區*](../secgloss/c-gly.md) 。
-   收件者的憑證會從存放區中取出。
-   從收件者的憑證中取出 [*公開金鑰*](../secgloss/p-gly.md) 。
-   使用收件者的公開金鑰，對稱金鑰會加密。
-   從收件者的憑證中，會取出收件者的識別碼。
-   數位封包訊息中包含下列資訊：資料加密演算法、加密的資料、加密的對稱金鑰，以及收件者資訊結構。

若要使用低層級的訊息函數來完成剛剛列出的一般工作，請使用下列程式。

**編碼封包訊息**

1.  建立或抓取內容。
2.  取得密碼編譯提供者。
3.  取得收件者憑證。
4.  將 [**CMSG 的 \_ 封裝 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) 結構初始化。
5.  呼叫 [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) 以取得編碼訊息 BLOB 的大小。 為它配置記憶體。
6.  呼叫 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)，傳入 CMSG \_ 的 *dwMsgType* 封包，以及 [**CMSG \_ 封包 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) 的指標以進行 *pvMsgEncodeInfo*。 由於這個呼叫，您將會取得已開啟之訊息的控制碼。
7.  呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)，傳入步驟6中抓取的控制碼，以及要加密、封裝和編碼的資料指標。 您可以視需要多次呼叫這個函式，以完成編碼程式。
8.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入步驟6中取出的控制碼和適當的參數類型，以存取所需的編碼資料。 例如，傳入 CMSG \_ CONTENT \_ PARAM 以取得整個 PKCS \# 7 訊息的指標。

    如果此編碼的結果是當做另一個編碼訊息的 [*內部資料*](../secgloss/i-gly.md) 使用，例如封包訊息，則 \_ 必須傳遞 CMSG 的 BARE \_ 內容 \_ 參數參數。 如需範例，請參閱 [編碼封包訊息的替代程式碼](alternate-code-for-encoding-an-enveloped-message.md)。

9.  藉由呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)來關閉訊息。

此程式的結果是編碼的訊息，其中包含加密的資料、以收件者公開金鑰加密的 [*對稱金鑰*](../secgloss/s-gly.md) ，以及收件者資訊資料結構。 加密內容和收件者加密對稱金鑰的組合是該收件者的 [*數位信封*](../secgloss/d-gly.md) 。 您可以針對多個收件者將任何類型的內容封包。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[範例 C 程式：編碼封包、簽署的訊息](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
