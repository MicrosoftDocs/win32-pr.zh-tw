---
description: 解碼封包訊息所需的一般工作。
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: 解碼封包資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df9df80b2a4bc1e3c9d6894bc83624908468edb63f7d0283ee3dca1b50a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767805"
---
# <a name="decoding-enveloped-data"></a>解碼封包資料

下圖說明解碼封包訊息所需的一般工作，並在後面的清單中加以說明。

![解碼封包資料](images/decemsg.png)

使用金鑰傳輸金鑰管理來解碼封包資料的事件順序（如上圖所示）如下所示：

-   已抓取 [*數位封包*](../secgloss/d-gly.md) 訊息的指標。
-   即會開啟 [*憑證存放區*](../secgloss/c-gly.md) 。
-   從訊息中，會抓取收件者識別碼 (我的識別碼) 。
-   收件者識別碼用來取得憑證。
-   已抓取與該憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md) 。
-   私密金鑰用來將 [*對稱*](../secgloss/s-gly.md) 式 ([*會話*](../secgloss/s-gly.md)) 機碼解密。
-   從訊息中取出加密演算法。
-   使用私密金鑰和加密演算法可解密資料。

下列程式使用低層級的訊息函式來完成剛剛列出的工作。

**解碼封包訊息**

1.  取得編碼 BLOB 的指標。
2.  呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)，傳遞必要的引數。
3.  呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 一次，並傳入步驟2中抓取的控制碼，以及要解碼之資料的指標。 這會根據訊息類型，對訊息採取適當的動作。
4.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入在步驟2和 CMSG 類型參數中抓取的控制碼， \_ \_ 以驗證訊息是否為封包資料類型。
5.  再次呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入 CMSG \_ 內部 \_ 內容 \_ 類型參數， \_ 以取得 [*內部內容*](../secgloss/i-gly.md)的資料類型。
6.  如果內部內容資料類型是 **資料**，請繼續解密並解碼內容。 否則，請執行適用于內容資料類型的解碼程式。
7.  假設內部內容類型是 "data"，請將 [**CMSG \_ ctrl \_ 解密 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) 資料結構和呼叫 [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)，並傳入 CMSG \_ ctrl \_ 解密和結構位址。 將會解密內容。
8.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入 CMSG \_ content \_ PARAM 以取得已解碼內容資料 BLOB 的指標， (**位元組** 字串) 。
9.  呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) 以關閉訊息。

此程式的結果是會將訊息解碼和解密，並將指標取出至內容資料 BLOB。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[範例 C 程式：編碼封包、簽署的訊息](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
