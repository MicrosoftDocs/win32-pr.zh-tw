---
description: CNG API 提供一組執行基本密碼編譯作業的函式，例如建立雜湊或加密和解密資料。 如需這些函式的詳細資訊，請參閱 CNG 密碼編譯基本函數。
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: 密碼編譯基本類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0f390b36bc500bf80b5b2ef0065651cf99f5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510884"
---
# <a name="cryptographic-primitives"></a>密碼編譯基本類型

CNG API 提供一組執行基本密碼編譯作業的函式，例如建立雜湊或加密和解密資料。 如需這些函式的詳細資訊，請參閱 [CNG 密碼編譯基本函數](cng-cryptographic-primitive-functions.md)。

CNG 實行了許多密碼編譯演算法。 演算法的每個演算法或類別都會公開自己的基本 API。 您可以同時安裝指定演算法的多個實值;不過，在任何指定的時間，都只會有一個預設的實作為預設值。

CNG 中的每個演算法類別都是由基本路由器表示。 使用 CNG 基本函式的應用程式會在使用者模式中 Bcrypt.dll 連結到路由器二進位檔案，或在呼叫函式之前 Ksecdd.sys 在核心模式中。 各種路由器常式都會管理所有的演算法基本專案。 這些路由器會追蹤系統上所安裝的每個演算法執行，並將每個函式呼叫路由至適當的基本提供者模組。

CNG 提供下列演算法類別的基本類型。



| 演算法類別                                                                                                                                                  | Description                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>亂數產生器<br/> | 可插入的亂數字產生 (RNG) 。<br/>                                                         |
| <span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>散 列<br/>                                                                 | 用於雜湊的演算法，例如 SHA1 和 SHA2。<br/>                                               |
| <span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>對稱式加密<br/>             | 用於對稱式加密的演算法，例如 AES、3DES 和 RC4。<br/>                             |
| <span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>非對稱式加密<br/>         | 非對稱 (公開金鑰) 支援加密的演算法，例如 RSA。<br/>                          |
| <span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>簽名<br/>                                                         | 簽署演算法，例如 DSA 和 ECDSA。 此類別也可以搭配 RSA 使用。<br/>                 |
| <span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>秘密合約<br/>                             | 秘密協定演算法，例如 Diffie-Hellman (DH) 和橢圓曲線 Diffie-Hellman (ECDH) 。<br/> |



 

下圖顯示 CNG 密碼編譯基本專案的設計和功能。

![cng 密碼編譯基本專案的設計和功能](images/ssdk-cng1c.png)

標頭檔 Bcrypt 會將 **MS \_ 基本 \_ 提供者** 常數定義為 "Microsoft 基本提供者"。 若要使用 Microsoft 基本提供者，請將此值傳遞給 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)。

 

 




