---
description: CryptXML 原本就支援下列 Uri。
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: XML 數位簽章密碼編譯演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896348375d1d1a51288980aad3793dfffc69eb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971001"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a><span data-ttu-id="f5fdb-103">XML 數位簽章密碼編譯演算法</span><span class="sxs-lookup"><span data-stu-id="f5fdb-103">XML Digital Signature Cryptographic Algorithms</span></span>

<span data-ttu-id="f5fdb-104">CryptXML 原本就支援下列 Uri。</span><span class="sxs-lookup"><span data-stu-id="f5fdb-104">CryptXML natively supports the URIs listed below.</span></span> <span data-ttu-id="f5fdb-105">如果不屬於原生支援的密碼編譯演算法和轉換需要支援，您可以使用「密碼編譯 [API：新一代](../seccng/cng-portal.md) 」和「 [XML 數位簽章」密碼編譯延伸](xml-digital-signature-cryptographic-extensions.md) 模組來支援新的演算法。</span><span class="sxs-lookup"><span data-stu-id="f5fdb-105">If support is required for cryptographic algorithms and transforms that are not part of the native support, you can use [Cryptography API: Next Generation](../seccng/cng-portal.md) and [XML Digital Signature Cryptographic Extensions](xml-digital-signature-cryptographic-extensions.md) to support new algorithms.</span></span>

## <a name="supported-uris"></a><span data-ttu-id="f5fdb-106">支援的 Uri</span><span class="sxs-lookup"><span data-stu-id="f5fdb-106">Supported URIs</span></span>

<span data-ttu-id="f5fdb-107">摘要方法</span><span class="sxs-lookup"><span data-stu-id="f5fdb-107">Digest Methods</span></span>



| <span data-ttu-id="f5fdb-108">常數</span><span class="sxs-lookup"><span data-stu-id="f5fdb-108">Constant</span></span>                                 | <span data-ttu-id="f5fdb-109">URI 值</span><span class="sxs-lookup"><span data-stu-id="f5fdb-109">URI value</span></span>                                                   |
|------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f5fdb-110">wszURI \_ XMLNS \_ DIGSIG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f5fdb-110">wszURI\_XMLNS\_DIGSIG\_SHA1</span></span><br/>   | <span data-ttu-id="f5fdb-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span></span><br/>        |
| <span data-ttu-id="f5fdb-112">wszURI \_ XMLNS \_ DIGSIG \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="f5fdb-112">wszURI\_XMLNS\_DIGSIG\_SHA256</span></span><br/> | <span data-ttu-id="f5fdb-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span></span><br/>       |
| <span data-ttu-id="f5fdb-114">wszURI \_ XMLNS \_ DIGSIG \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="f5fdb-114">wszURI\_XMLNS\_DIGSIG\_SHA384</span></span><br/> | <span data-ttu-id="f5fdb-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span></span><br/> |
| <span data-ttu-id="f5fdb-116">wszURI \_ XMLNS \_ DIGSIG \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="f5fdb-116">wszURI\_XMLNS\_DIGSIG\_SHA512</span></span><br/> | <span data-ttu-id="f5fdb-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span></span><br/>       |



 

<span data-ttu-id="f5fdb-118">簽章方法</span><span class="sxs-lookup"><span data-stu-id="f5fdb-118">Signature Methods</span></span>



| <span data-ttu-id="f5fdb-119">常數</span><span class="sxs-lookup"><span data-stu-id="f5fdb-119">Constant</span></span>                                        | <span data-ttu-id="f5fdb-120">URI 值</span><span class="sxs-lookup"><span data-stu-id="f5fdb-120">URI value</span></span>                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f5fdb-121">wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f5fdb-121">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA1</span></span><br/>     | <span data-ttu-id="f5fdb-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span></span><br/>          |
| <span data-ttu-id="f5fdb-123">wszURI \_ XMLNS \_ DIGSIG \_ DSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f5fdb-123">wszURI\_XMLNS\_DIGSIG\_DSA\_SHA1</span></span><br/>     | <span data-ttu-id="f5fdb-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span></span><br/>          |
| <span data-ttu-id="f5fdb-125">wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="f5fdb-125">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA256</span></span><br/>   | <span data-ttu-id="f5fdb-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span></span><br/>   |
| <span data-ttu-id="f5fdb-127">wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="f5fdb-127">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA384</span></span><br/>   | <span data-ttu-id="f5fdb-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span></span><br/>   |
| <span data-ttu-id="f5fdb-129">wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="f5fdb-129">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA512</span></span><br/>   | <span data-ttu-id="f5fdb-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span></span><br/>   |
| <span data-ttu-id="f5fdb-131">wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f5fdb-131">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA1</span></span><br/>   | <span data-ttu-id="f5fdb-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span></span><br/>   |
| <span data-ttu-id="f5fdb-133">wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="f5fdb-133">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA256</span></span><br/> | <span data-ttu-id="f5fdb-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span></span><br/> |
| <span data-ttu-id="f5fdb-135">wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="f5fdb-135">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA384</span></span><br/> | <span data-ttu-id="f5fdb-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span></span><br/> |
| <span data-ttu-id="f5fdb-137">wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="f5fdb-137">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA512</span></span><br/> | <span data-ttu-id="f5fdb-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span></span><br/> |
| <span data-ttu-id="f5fdb-139">wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f5fdb-139">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA1</span></span><br/>    | <span data-ttu-id="f5fdb-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span></span><br/>         |
| <span data-ttu-id="f5fdb-141">wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="f5fdb-141">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA256</span></span><br/>  | <span data-ttu-id="f5fdb-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span></span><br/>  |
| <span data-ttu-id="f5fdb-143">wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="f5fdb-143">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA384</span></span><br/>  | <span data-ttu-id="f5fdb-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span></span><br/>  |
| <span data-ttu-id="f5fdb-145">wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="f5fdb-145">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA512</span></span><br/>  | <span data-ttu-id="f5fdb-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span><span class="sxs-lookup"><span data-stu-id="f5fdb-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span></span><br/>  |



 

 

 
