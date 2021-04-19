---
description: 大量加密金鑰是藉由使用 CryptHashSessionKey 來雜湊其中一個 MAC 金鑰以及訊息內容和其他資料所產生。 使用其中一個大量加密金鑰以一般方式加密/解密訊息。
ms.assetid: 08174502-3ff1-4c1c-bcd0-46fd85882305
title: 大量資料加密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecfb55c162e5aa576d8baa3d0ccbc45e9588c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982739"
---
# <a name="bulk-data-encryption"></a>大量資料加密

[*大量加密金鑰*](../secgloss/b-gly.md)是藉由使用 [**CryptHashSessionKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey)來 [*雜湊*](../secgloss/h-gly.md)其中一個 MAC 金鑰以及訊息內容和其他資料所產生。 使用其中一個大量加密金鑰以一般方式加密/解密訊息。

使用 [*區塊密碼*](../secgloss/b-gly.md)[*時，安全通道通訊協定*](../secgloss/s-gly.md)引擎會執行所有必要的 *區塊密碼*[*填補*](../secgloss/p-gly.md)。 當呼叫 [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) 和 [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) 時，最後一個旗標一律為 **FALSE** ，而資料長度是整個區塊長度的倍數。

> [!Note]  
> CSP 絕不能在內部緩衝資料。 將資料加密 (或解密) 之後， [*純文字*](../secgloss/p-gly.md) 大小必須一律完全符合 [*加密*](../secgloss/c-gly.md)文字的大小。

 

 

 
