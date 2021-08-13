---
description: 包含以字母 H 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4165b820-30fc-477e-a690-81109f161323
title: 'H (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147162a99ec4c8cc669c6cff2c39203c3da5b9d4e56802377c273e7dbe8e288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895601"
---
# <a name="h-security-glossary"></a>H (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [](u-gly.md) [](v-gly.md) [G](g-gly.md) H [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_handle_gly"></span><span id="_SECURITY_HANDLE_GLY"></span>**處理**
</dt> <dd>

用來識別或存取物件的 token，例如密碼編譯提供者的控制碼、憑證存放區、訊息或金鑰組。

</dd> <dt>

<span id="_security_hash_gly"></span><span id="_SECURITY_HASH_GLY"></span>**散 列**
</dt> <dd>

藉由套用數學函式 (*雜湊演算法*) 至任意數量的資料，即可取得固定大小的結果。  (也稱為「訊息摘要」。) 

另請參閱 *雜湊函數*。

</dd> <dt>

<span id="_security_hash_object_gly"></span><span id="_SECURITY_HASH_OBJECT_GLY"></span>**hash 物件**
</dt> <dd>

用來雜湊訊息或會話索引鍵的物件。 雜湊物件是由呼叫 **CryptCreateHash** 所建立。 物件的定義是由呼叫中指定的 CSP 所定義。

</dd> <dt>

<span id="_security_hashing_algorithm_gly"></span><span id="_SECURITY_HASHING_ALGORITHM_GLY"></span>**雜湊演算法**
</dt> <dd>

演算法，用來產生某些資料片段 (例如訊息或工作階段金鑰) 的雜湊值。 傳統的雜湊演算法包含 MD2、MD4、MD5，與 SHA-1。

</dd> <dt>

<span id="_security_hashing_functions_gly"></span><span id="_SECURITY_HASHING_FUNCTIONS_GLY"></span>**雜湊函數**
</dt> <dd>

一組函數，用來建立和終結雜湊物件、取得或設定雜湊物件的參數，以及雜湊資料和工作階段金鑰。

</dd> <dt>

<span id="_security_hash_based_message_authentication_code_gly"></span><span id="_SECURITY_HASH_BASED_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**以雜湊為基礎的訊息驗證碼**
</dt> <dd>

 (HMAC) Microsoft 密碼編譯服務提供者所執行的對稱式金鑰雜湊演算法。 HMAC 可用來確認資料的完整性，以協助確保在儲存或傳輸時，不會修改資料。 它可以搭配任何反復的密碼編譯雜湊演算法（例如 MD5 或 SHA-1）使用。 CryptoAPI 會依據演算法識別碼來參考此演算法 (CALG \_ HMAC) 和類別 (ALG \_ 類別 \_ 雜湊) 。

另請參閱 [*訊息驗證碼*](m-gly.md)。

</dd> <dt>

<span id="_security_hcsbc_gly"></span><span id="_SECURITY_HCSBC_GLY"></span>**HCSBC**
</dt> <dd>

作為憑證服務備份內容之控制碼的資料類型。 其角色是在執行備份時，維護伺服器與備份 Api 之間的內容狀態。

</dd> <dt>

<span id="_security_hmac_gly"></span><span id="_SECURITY_HMAC_GLY"></span>**Hmac**
</dt> <dd>

請參閱以 *雜湊為基礎的訊息驗證碼*。

</dd> </dl>

 

 



