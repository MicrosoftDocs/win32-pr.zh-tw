---
description: 描述編碼已簽署訊息的程式。
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: 編碼簽署的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4a542fe0890a6ee9d51ebc1a5ee6b98bab4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194177"
---
# <a name="encoding-signed-data"></a>編碼簽署的資料

[*帶正負*](../secgloss/s-gly.md) 號的資料是由零個或更多個簽署者之內容的任何類型和加密訊息 [*雜湊*](../secgloss/h-gly.md) 的內容所組成。 產生的雜湊可以確認原始訊息在簽署後未經過修改，且該特定人員或實體已簽署資料。

下圖描述編碼已簽署訊息的程式。 下圖中的清單描述這些步驟。

訊息可能會有多個「簽署者」、「雜湊演算法」和「憑證」。 雖然圖例只顯示憑證、 [*crl*](../secgloss/c-gly.md)和 [*ctl*](../secgloss/c-gly.md) 都可以使用相同的進程。 它們可放在顯示憑證的任何位置。

![編碼已簽署的訊息](images/signmsg2.png)

編碼 [*簽署資料*](../secgloss/s-gly.md) 的一般程式如下所示。

**編碼簽署的資料**

1.  必要時，會 (建立資料) ，並抓取其指標。
2.  開啟的 [*憑證存放區*](../secgloss/c-gly.md) 包含簽署者的憑證。
3.  取得憑證的私密金鑰。 在使用憑證之前，必須在憑證上設定兩個屬性。 一個是用來將憑證系結至特定的 CSP，並在該 CSP 內系結至特定的私密金鑰 [*容器*](../secgloss/k-gly.md)。 另一個用來指出呼叫 [*雜湊*](../secgloss/h-gly.md) 作業時要使用的雜湊演算法。 這些只需要設定一次。
4.  憑證的屬性會決定雜湊演算法。
5.  透過雜湊函數傳送資料，即可建立資料的雜湊。
6.  簽章是使用私密金鑰（透過憑證上的屬性取得）的加密雜湊所建立。
7.  已完成、已簽署的訊息中包含下列資料：
    -   要簽署的原始資料
    -   雜湊演算法
    -   簽章
    -   簽署者資訊結構，其中包括簽署者識別碼 (憑證簽發者和序號) 
    -   簽署者的憑證 (選用) 

此程式說明簡單的案例。 更複雜的案例牽涉到訊息中包含已驗證的屬性。 當內容類型是除了 **位元組** 字串的任何內容，或至少有一個已驗證的屬性與任何資料類型時，需要兩個標準的已驗證屬性：內容 (資料) 類型，以及內容的雜湊。 在這些情況下， [*CryptoAPI*](../secgloss/c-gly.md) 會自動提供這兩個必要的屬性。 低層級訊息函式會將已驗證的屬性雜湊、使用私密金鑰來加密雜湊，並將其提供為簽章。

使用下列程式，使用低層級的訊息函式來完成剛剛列出的工作。

**編碼已簽署的訊息**

1.  建立或抓取內容。
2.  取得密碼編譯提供者。
3.  取得簽署者憑證。
4.  將 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構初始化。
5.  將 [**CMSG \_ 簽署的 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) 結構初始化。
6.  呼叫 [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) 以取得編碼訊息 BLOB 的大小。 為它配置記憶體。
7.  呼叫 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)，傳入 CMSG \_ 帶正負號 *的 dwMsgType* ，以及 [**CMSG 簽署的 \_ \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)指標以取得已開啟之訊息的控制碼。
8.  呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)，傳入步驟7中取出的控制碼，以及要簽署及編碼的資料指標。 您可以視需要多次呼叫這個函式，以完成編碼程式。
9.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入步驟7中取出的控制碼和適當的參數類型，以存取所需的編碼資料。 例如，傳入 CMSG \_ CONTENT \_ PARAM 以取得整個 [*PKCS \# 7*](../secgloss/p-gly.md) 訊息的指標。

    如果此編碼的結果是當做另一個編碼訊息的 [*內部資料*](../secgloss/i-gly.md) 使用，例如封包訊息，則 \_ 必須傳遞 CMSG 的 BARE \_ 內容 \_ 參數參數。 如需顯示此情況的範例，請參閱 [編碼封包訊息的替代程式碼](alternate-code-for-encoding-an-enveloped-message.md)。

10. 藉由呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)來關閉訊息。

此程式的結果是編碼的訊息，其中包含原始資料、該資料的加密雜湊 (簽章) 和簽署者資訊。 另外還有指向所需編碼 BLOB 的指標。

如需 C 編碼的詳細資料，請參閱 [c 程式範例：簽署、編碼、解碼和驗證訊息](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)。

 

 
