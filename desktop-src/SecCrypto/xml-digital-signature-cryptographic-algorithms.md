---
description: CryptXML 原本就支援下列 Uri。
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: XML 數位簽章密碼編譯演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290be3708565cf144b5bf23bfcb1ddfe5252b227c12bbcebbd81b68d0fc2df07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895783"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a>XML 數位簽章密碼編譯演算法

CryptXML 原本就支援下列 Uri。 如果不屬於原生支援的密碼編譯演算法和轉換需要支援，您可以使用「密碼編譯 [API：新一代](../seccng/cng-portal.md) 」和「 [XML 數位簽章」密碼編譯延伸](xml-digital-signature-cryptographic-extensions.md) 模組來支援新的演算法。

## <a name="supported-uris"></a>支援的 Uri

摘要方法



| 常數                                 | URI 值                                                   |
|------------------------------------------|-------------------------------------------------------------|
| wszURI \_ XMLNS \_ DIGSIG \_ SHA1<br/>   | "https://www.w3.org/2000/09/xmldsig\#sha1"<br/>        |
| wszURI \_ XMLNS \_ DIGSIG \_ SHA256<br/> | "https://www.w3.org/2001/04/xmlenc\#sha256"<br/>       |
| wszURI \_ XMLNS \_ DIGSIG \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#sha384"<br/> |
| wszURI \_ XMLNS \_ DIGSIG \_ SHA512<br/> | "https://www.w3.org/2001/04/xmlenc\#sha512"<br/>       |



 

簽章方法



| 常數                                        | URI 值                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#rsa-sha1"<br/>          |
| wszURI \_ XMLNS \_ DIGSIG \_ DSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#dsa-sha1"<br/>          |
| wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA256<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"<br/>   |
| wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA384<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"<br/>   |
| wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA512<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"<br/>   |
| wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA1<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"<br/>   |
| wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA256<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"<br/> |
| wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"<br/> |
| wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA512<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"<br/> |
| wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA1<br/>    | "https://www.w3.org/2000/09/xmldsig\#hmac-sha1"<br/>         |
| wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA256<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"<br/>  |
| wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA384<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"<br/>  |
| wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA512<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"<br/>  |



 

 

 
