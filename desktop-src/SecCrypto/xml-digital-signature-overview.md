---
description: XML 是描述結構化資料的業界標準。 XML 數位簽章是數位簽章的 XML 標記法，可讓您驗證 XML 檔和外部參考資料的來源和完整性。
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: XML 數位簽章總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001378"
---
# <a name="xml-digital-signature-overview"></a><span data-ttu-id="925b1-104">XML 數位簽章總覽</span><span class="sxs-lookup"><span data-stu-id="925b1-104">XML Digital Signature Overview</span></span>

<span data-ttu-id="925b1-105">XML 是描述結構化資料的業界標準。</span><span class="sxs-lookup"><span data-stu-id="925b1-105">XML is an industry standard for describing structured data.</span></span> <span data-ttu-id="925b1-106">XML 數位簽章是 [*數位簽章*](../secgloss/d-gly.md) 的 xml 標記法，可讓您驗證 XML 檔和外部參考資料的來源和完整性。</span><span class="sxs-lookup"><span data-stu-id="925b1-106">An XML Digital Signature is an XML representation of a [*digital signature*](../secgloss/d-gly.md) that provides the ability to verify the origin and integrity of XML document and externally referenced data.</span></span> <span data-ttu-id="925b1-107">XML 數位簽章可以用來簽署任意資料，包括 XML 檔或片段、HTML 網頁、純文字或二進位編碼的資料（例如 JPEG 檔案）。</span><span class="sxs-lookup"><span data-stu-id="925b1-107">XML digital signatures can be used to sign arbitrary data, including an XML document or fragment, an HTML page, plain text, or binary-encoded data such as a JPEG file.</span></span>

<span data-ttu-id="925b1-108">CryptXML 數位簽章 API 所支援的 XML 數位簽章格式是由 XML 簽章語法和處理 (第二版) W3C 建議所指定。</span><span class="sxs-lookup"><span data-stu-id="925b1-108">The XML digital signature format supported by the CryptXML digital signature API is specified by the XML Signature Syntax and Processing (Second Edition) W3C recommendation.</span></span>

<span data-ttu-id="925b1-109">CryptXML 數位簽章可支援所需的簽章類型、密碼編譯演算法、正常化演算法和指定的封包轉換。</span><span class="sxs-lookup"><span data-stu-id="925b1-109">The CryptXML digital signature implements support for the required signature types, cryptographic algorithms, canonicalization algorithms, and the specified enveloped transform.</span></span>

<span data-ttu-id="925b1-110">開發人員可以藉由建立密碼編譯延伸模組 Dll，來擴充 CryptXML 所支援的一組預設密碼編譯演算法。</span><span class="sxs-lookup"><span data-stu-id="925b1-110">Developers can extend the default set of cryptographic algorithms supported by CryptXML by creating cryptographic extension DLLs.</span></span> <span data-ttu-id="925b1-111">開發人員也可以在 CryptXML API 之上建立自己的自訂轉換和標準化演算法。</span><span class="sxs-lookup"><span data-stu-id="925b1-111">Developers can also create their own custom transforms and canonicalization algorithms on top of CryptXML API.</span></span> <span data-ttu-id="925b1-112">開發人員可以使用 CryptXML Api 搭配 Windows 憑證 Api。</span><span class="sxs-lookup"><span data-stu-id="925b1-112">Developers can use the CryptXML APIs with the Windows certificate APIs.</span></span>

 

 
