---
description: 已提供一組高階函式來簡化及縮短完成一般訊息操作工作所需的程式碼數量。
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: 簡化的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbacaac4dd8ef32b7bab1ff4e57ad04aa1263c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113544"
---
# <a name="simplified-messages"></a>簡化的訊息

已提供一組高階函式來簡化及縮短完成一般訊息操作工作所需的程式碼數量。 這些函式稱為「簡化的訊息函數」。 所有簡化訊息函數的名稱都包含 "Message" 這個字。

[*簡化的訊息*](../secgloss/s-gly.md) 函式比基底加密函式或低層級訊息函式的層級更高。 它們會將數個基本密碼編譯、低層級訊息和憑證函式包裝成單一函式，以特定方式執行特定工作，例如加密 PKCS \# 7 訊息或簽署訊息。 簡化的訊息函數可讓您快速開始使用 CryptoAPI，方法是減少完成工作所需的函式呼叫數目。

下表列出包含詳細程式描述的章節，或使用簡化訊息函式的 C 程式範例。



| 區段                                                                                                                                         | 目錄                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [簡化的訊息函數](cryptography-functions.md)                                                         | 列出簡化的訊息函數。                                                     |
| [建立已簽署的訊息](creating-a-signed-message.md)                                                                                      | 詳細說明建立已簽署訊息的程式。                                           |
| [簽署資料的程式](procedure-for-signing-data.md)                                                                                    | 提供使用簡化的訊息函式來建立已簽署訊息的程式。 |
| [驗證已簽署的訊息](verifying-a-signed-message.md)                                                                                    | 詳細說明在已簽署的訊息上驗證簽章的流程。                          |
| [加密訊息](../secauthn/encrypting-a-message.md)                                                                                           | 詳述加密和解密訊息所需的工作。                                  |
| [解密訊息](../secauthn/decrypting-a-message.md)                                                                                           | 詳細說明解密訊息所需的工作。                                              |
| [範例 C 程式：使用 CryptEncryptMessage 和 CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) | 提供用來加密和解密訊息的程式和範例程式碼。               |



 

 

 
