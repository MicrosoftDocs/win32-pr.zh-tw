---
description: 描述編碼雜湊訊息所需的工作。
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: 編碼和解碼雜湊訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91d165634c1ae00a59f2c77b1fc5a36b53dbd96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975412"
---
# <a name="encoding-and-decoding-a-hashed-message"></a>編碼和解碼雜湊訊息

雜湊資料是由任何類型的內容和內容的 [*雜湊*](../secgloss/h-gly.md) 所組成。 只有在建立雜湊之後，才需要確認訊息內容尚未經過修改，才能使用它。

建立雜湊訊息時，可能會有多個雜湊演算法和多個雜湊。 下圖描述編碼雜湊訊息所需的工作。 程式如下圖所述。

![建立雜湊訊息](images/hashmsg.png)

**建立雜湊訊息**

1.  取得要雜湊之資料的指標。
2.  選取要使用的雜湊演算法。
3.  使用雜湊演算法，透過雜湊函數來放置資料。
4.  包含要雜湊處理的原始資料、雜湊演算法，以及編碼訊息中的雜湊。

若要使用低層級的訊息函式來完成剛剛所述的工作，請使用下列程式。

**使用低層級訊息函式來雜湊和編碼訊息**

1.  建立或取出要進行雜湊處理的內容。
2.  取得密碼編譯提供者。
3.  將 [**CMSG \_ 雜湊 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) 結構初始化。
4.  呼叫 [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) 以取得編碼訊息 BLOB 的大小。 為它配置記憶體。
5.  呼叫 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)，傳入 CMSG \_ 雜湊的 *DwMsgType* 參數，以及 CMSG 參數 [**的 \_ 雜湊 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info)指標 。 由於這個呼叫，您會取得已開啟之訊息的控制碼。
6.  呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)，傳入在步驟5中抓取的控制碼，以及要進行雜湊處理和編碼的資料指標。 您可以視需要多次呼叫這個函式，以完成編碼程式。
7.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入在步驟5中抓取的控制碼和適當的參數類型，以存取所需的編碼資料。 例如，傳入 CMSG \_ CONTENT \_ PARAM 以取得整個 [*PKCS \# 7*](../secgloss/p-gly.md) 訊息的指標。

    如果此編碼的結果是做為另一個編碼訊息的 [*內部資料*](../secgloss/i-gly.md) ，例如封包訊息，則 \_ \_ 必須傳遞 CMSG 的 BARE 內容 \_ 參數。 如需顯示此情況的範例，請參閱 [編碼封包訊息的替代程式碼](alternate-code-for-encoding-an-enveloped-message.md)。

8.  藉由呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)來關閉訊息。

此程式的結果是編碼的訊息，其中包含原始資料、雜湊演算法和該資料的 [*雜湊*](../secgloss/h-gly.md) 。 在步驟7中，會取得編碼訊息 [*BLOB*](../secgloss/b-gly.md) 的指標。

下列兩個程式會解碼並確認雜湊資料。

**解碼雜湊資料**

1.  取得編碼 BLOB 的指標。
2.  呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)，傳遞必要的引數。
3.  呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 一次，並傳入步驟2中抓取的控制碼，以及要解碼之資料的指標。 這會根據訊息類型，對訊息採取適當的動作。
4.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入步驟2中抓取的控制碼，以及適當的參數類型來存取所需的解碼資料。 例如，傳入 CMSG \_ content \_ PARAM 以取得已解碼內容的指標。

**確認雜湊**

1.  呼叫 [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)，傳入 CMSG \_ CTRL \_ 確認 \_ 雜湊來驗證雜湊。
2.  呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) 以關閉訊息。

如需範例程式，請參閱 [範例 C 程式：編碼和解碼雜湊的訊息](example-c-program-encoding-and-decoding-a-hashed-message.md)。

 

 
