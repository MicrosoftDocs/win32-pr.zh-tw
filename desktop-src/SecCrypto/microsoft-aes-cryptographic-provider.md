---
description: Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援與 Microsoft 基底密碼編譯提供者相同的功能，稱為「基底提供者」。
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Microsoft AES 密碼編譯提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2449c53cb828a94c8dd596133c3a8c21c9b0388
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581866"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Microsoft AES 密碼編譯提供者

Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援與 Microsoft 基底密碼編譯提供者相同的功能，稱為「基底提供者」。 AES 提供者透過更長的金鑰和其他演算法，支援更強的安全性。 它可以與所有 CryptoAPI 版本搭配使用。

**Windows XP：** Microsoft AES 密碼編譯提供者的名稱為 Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 。

為了維持與先前的提供者版本之間的回溯相容性，提供者名稱（如 Wincrypt .h 標頭檔中所定義）會保留版本1.0 指定，即使已寄出此提供者的較新版本也一樣。 若要判斷使用中的提供者版本，請呼叫 [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) ，並將 *dwParam* 參數設定為 PP \_ 版本。 如果傳回0x0200，則會使用2.0 版。

|                   | 值                    |
|-------------------|--------------------------|
| **提供者類型** | >PROV \_ RSA \_ AES           |
| **提供者名稱** | MS \_ ENH \_ RSA \_ AES \_ >PROV  |



 

下表強調基底提供者、強式提供者和 AES 提供者之間的差異。 所顯示的 [*金鑰長度*](../secgloss/k-gly.md) 為預設金鑰長度。



| 演算法                                                                                | 基底提供者金鑰長度 | 強式提供者金鑰長度 | AES 提供者金鑰長度                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| RSA 公開金鑰簽章演算法                                                       | 512位                 | 1024位                 | 1024位                                  |
| RSA 公開金鑰交換演算法                                                        | 512位                 | 1024位                 | 1024位                                  |
| RC2 區塊加密演算法                                                           | 40位                  | 128 位元                   | 可以設定128位 Salt 長度。<br/> |
| RC4 串流加密演算法                                                          | 40位                  | 128 位元                   | 可以設定128位 Salt 長度。<br/> |
| DES                                                                                      | 56位                  | 56位                    | 56位                                     |
| [*三重 DES*](../secgloss/t-gly.md) (2 金鑰)  | 不支援            | 112位                   | 112位                                    |
| 三重 DES (3 金鑰)                                                                        | 不支援            | 168位                   | 168位                                    |



 

如需支援之演算法的完整清單，請參閱 [AES 提供者演算法](aes-provider-algorithms.md)。

強式提供者、增強的提供者和 AES 提供者與基底提供者回溯相容，不同之處在于提供者只能產生預設金鑰長度的 RC2 或 RC4 金鑰。 基底提供者的預設長度是40位。 AES 提供者的預設長度是128位。 因此 AES 提供者無法建立具有基底提供者相容金鑰長度的金鑰。 不過，AES 提供者可以匯入最多128位的 RC2 和 RC4 金鑰。 因此，AES 提供者可以匯入和使用使用基底提供者所產生的40位金鑰。

 

 
