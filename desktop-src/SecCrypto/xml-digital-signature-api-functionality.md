---
description: CryptXML 提供一組低層級的 Api，可讓應用程式建立及驗證信封、封套和卸離的簽章。 您可以使用 CryptXML 來建立及驗證儲存在 signature 物件元素中的內容，包括資訊清單。
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: XML 數位簽章 API 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989437"
---
# <a name="xml-digital-signature-api-functionality"></a>XML 數位簽章 API 功能

CryptXML 提供一組低層級的 Api，可讓應用程式建立及驗證信封、封套和卸離的簽章。 您可以使用 CryptXML 來建立及驗證儲存在 signature 物件元素中的內容，包括資訊清單。 公開/私用、共用金鑰或 [*x.509*](../secgloss/x-gly.md) 憑證或憑證鏈可以用來簽署和驗證 XML [*數位簽章*](../secgloss/d-gly.md)。

使用 CryptXML 來驗證外部參考的應用程式 (以檔內容以外的外部檔或檔案為目標的參考，) 必須解析外部 Uri 並取出要子集的資料。

如需 CryptXML 所支援的密碼編譯演算法的詳細資訊，請參閱 [XML 數位簽章密碼編譯演算法](xml-digital-signature-cryptographic-algorithms.md)。

CryptXML 可支援具有下列識別碼的標準化演算法。



| 常數                                              | URI 值                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| wszURI \_ 標準化 \_ C14N<br/>             | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315"<br/>               |
| wszURI \_ 標準化 \_ C14NC<br/>            | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"<br/> |
| wszURI \_ 標準化 \_ EXSLUSIVE \_ C14N<br/>  | "https://www.w3.org/2001/10/xml-exc-c14n\#"<br/>                      |
| wszURI \_ 標準化 \_ EXSLUSIVE \_ C14NC<br/> | "https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"<br/>          |



 

CryptXML 提供封裝簽章轉換的支援。



| 常數                                       | URI 值                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| wszURI \_ XMLNS \_ 轉換的 \_ 封包<br/> | "https://www.w3.org/2000/09/xmldsig\#enveloped-signature"<br/> |



 

根據預設，CryptXML 不支援 XPath 或 XSLT 轉換。 如有必要，應用程式可以在 CryptXML 上執行這些轉換。

 

 
