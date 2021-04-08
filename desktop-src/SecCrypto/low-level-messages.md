---
description: 低層級訊息函式會針對已接收的傳輸和解碼資料來編碼資料。 低層級訊息函式也會解密並驗證已接收訊息的簽章。
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: 低層級訊息函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690743"
---
# <a name="low-level-message-functions"></a>低層級訊息函數

[*低層級訊息函式*](../secgloss/l-gly.md)會針對已接收的傳輸和解碼資料來編碼資料。 低層級訊息函式也會解密並驗證已接收訊息的簽章。

使用低層級的訊息開啟函式開啟訊息時，它會保持開啟且可用 (維護其 [*狀態*](../secgloss/s-gly.md)) 直到關閉為止。 這可讓您使用多個呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 函式來分次訊息。

使用低層級的訊息函式需要比使用簡化的訊息函式更多的函式呼叫 (請參閱) 的 [簡化訊息](simplified-messages.md) 。 如果使用簡化的訊息函式，則會在 API 的函式內執行更多工作。

使用低層級訊息函式牽涉到額外的工作，以呼叫其他憑證或密碼編譯功能。 例如，可能需要呼叫憑證函式的資料，才能初始化這些低層級訊息函式所使用的結構。 簡化的訊息函數會在內部初始化許多這些結構。

下表列出具有程式描述的區段，以及使用低層級訊息函式的 C 程式碼範例。



| 區段                                                                               | 目錄                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [低層級訊息函數](cryptography-functions.md) | 列出低層級的訊息函數。             |
| [簽署資料](signing-data.md)                                                      | 詳述簽署資料所需的工作。             |
| [編碼封包資料](encoding-enveloped-data.md)                                | 詳細說明編碼封包資料所需的工作。 |
| [解碼封包資料](decoding-enveloped-data.md)                                | 詳細說明解碼封包資料所需的工作。 |



 

 

 
