---
description: 說明如何建立 HMAC。
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: 建立 HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364314081bd1d84d6d9bfff889c234470cc6775c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974512"
---
# <a name="creating-an-hmac"></a>建立 HMAC

**計算 HMAC**

1.  藉由呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)，取得 Microsoft [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的指標。
2.  藉由呼叫 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)來建立 [*HMAC*](../secgloss/h-gly.md)[*雜湊物件*](../secgloss/h-gly.md)的控制碼。 \_在 *Algid* 參數中傳遞 CALG HMAC。 在 *hKey* 參數中傳遞 [*對稱金鑰*](../secgloss/s-gly.md)的控制碼。 此對稱金鑰是用來計算 HMAC 的金鑰。
3.  藉由呼叫 [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) ，並將 *dwParam* 參數設定為 [HP HMAC 資訊] 值，以指定要使用的雜湊類型 \_ \_ 。 *>pbdata* 參數必須指向已初始化的 [**HMAC \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info)結構。
4.  呼叫 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) 以開始計算資料的 HMAC。 第一次呼叫 **CryptHashData** 時，會使用 XOR 運算子搭配內部字串和資料來結合索引鍵值。 XOR 運算的結果會經過雜湊處理，然後在對) **CryptHashData** 的呼叫中傳遞的 *>pbdata* 參數所指向的 HMAC (的目標資料會雜湊處理。 如有必要，您可以接著對 **CryptHashData** 進行後續的呼叫，以完成目標資料的雜湊。
5.  使用設定為 HP HASHVAL 的 *dwParam* 參數呼叫 [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) \_ 。 此呼叫會導致內部雜湊完成，並使用 XOR 搭配索引鍵來結合外部字串。 XOR 運算的結果會經過雜湊處理，然後在上一個步驟中完成的內部雜湊 (結果) 雜湊。 外部雜湊接著會完成，並在 *>pbdata* 參數和 *dwDataLen* 參數中的長度傳回。

> [!Note]  
> 請勿將相同的 [*對稱*](../secgloss/s-gly.md) ([*會話*](../secgloss/s-gly.md)) 金鑰用於訊息加密和 [*訊息驗證碼*](../secgloss/m-gly.md) (MAC) 產生。 使用相同的金鑰會大幅增加攻擊者解碼訊息的風險。

 

 

 
