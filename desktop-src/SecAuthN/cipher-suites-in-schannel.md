---
description: 加密套件是一組密碼編譯演算法。
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: TLS/SSL (Schannel SSP) 的加密套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa8b47aed266c49ac306adfd2aef78af269a39
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986454"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a><span data-ttu-id="7c524-103">TLS/SSL (Schannel SSP) 的加密套件</span><span class="sxs-lookup"><span data-stu-id="7c524-103">Cipher Suites in TLS/SSL (Schannel SSP)</span></span>

<span data-ttu-id="7c524-104">加密套件是一組密碼編譯演算法。</span><span class="sxs-lookup"><span data-stu-id="7c524-104">A cipher suite is a set of cryptographic algorithms.</span></span> <span data-ttu-id="7c524-105">TLS/SSL 通訊協定的安全通道 SSP 執行會使用加密套件中的演算法來建立金鑰和加密資訊。</span><span class="sxs-lookup"><span data-stu-id="7c524-105">The schannel SSP implementation of the TLS/SSL protocols use algorithms from a cipher suite to create keys and encrypt information.</span></span> <span data-ttu-id="7c524-106">加密套件會為下列每個工作指定一種演算法：</span><span class="sxs-lookup"><span data-stu-id="7c524-106">A cipher suite specifies one algorithm for each of the following tasks:</span></span>

-   <span data-ttu-id="7c524-107">金鑰交換</span><span class="sxs-lookup"><span data-stu-id="7c524-107">Key exchange</span></span>
-   <span data-ttu-id="7c524-108">大量加密</span><span class="sxs-lookup"><span data-stu-id="7c524-108">Bulk encryption</span></span>
-   <span data-ttu-id="7c524-109">訊息驗證</span><span class="sxs-lookup"><span data-stu-id="7c524-109">Message authentication</span></span>

<span data-ttu-id="7c524-110">[*金鑰交換演算法*](/windows/desktop/SecGloss/k-gly) 可保護建立共用金鑰所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="7c524-110">[*Key exchange algorithms*](/windows/desktop/SecGloss/k-gly) protect information required to create shared keys.</span></span> <span data-ttu-id="7c524-111">這些演算法是非對稱的 ([*公開金鑰演算法*](/windows/desktop/SecGloss/p-gly)) ，適用于相對較少量的資料。</span><span class="sxs-lookup"><span data-stu-id="7c524-111">These algorithms are asymmetric ([*public key algorithms*](/windows/desktop/SecGloss/p-gly)) and perform well for relatively small amounts of data.</span></span>

<span data-ttu-id="7c524-112">大量加密演算法會加密在用戶端與伺服器之間交換的訊息。</span><span class="sxs-lookup"><span data-stu-id="7c524-112">Bulk encryption algorithms encrypt messages exchanged between clients and servers.</span></span> <span data-ttu-id="7c524-113">這些演算法是 [*對稱*](/windows/desktop/SecGloss/s-gly) 的，且適用于大量的資料。</span><span class="sxs-lookup"><span data-stu-id="7c524-113">These algorithms are [*symmetric*](/windows/desktop/SecGloss/s-gly) and perform well for large amounts of data.</span></span>

<span data-ttu-id="7c524-114">[訊息驗證](message-authentication-codes-in-schannel.md) 演算法會產生訊息 [*雜湊*](/windows/desktop/SecGloss/h-gly) 和簽章，以確保訊息的 [*完整性*](/windows/desktop/SecGloss/i-gly) 。</span><span class="sxs-lookup"><span data-stu-id="7c524-114">[Message authentication](message-authentication-codes-in-schannel.md) algorithms generate message [*hashes*](/windows/desktop/SecGloss/h-gly) and signatures that ensure the [*integrity*](/windows/desktop/SecGloss/i-gly) of a message.</span></span>

<span data-ttu-id="7c524-115">開發人員會使用 [**ALG \_ 識別碼**](/windows/desktop/SecCrypto/alg-id) 資料類型來指定這些元素。</span><span class="sxs-lookup"><span data-stu-id="7c524-115">Developers specify these elements by using [**ALG\_ID**](/windows/desktop/SecCrypto/alg-id) data types.</span></span> <span data-ttu-id="7c524-116">如需詳細資訊，請參閱 [指定 Schannel 密碼和加密強度](specifying-schannel-ciphers-and-cipher-strengths.md)。</span><span class="sxs-lookup"><span data-stu-id="7c524-116">For more information, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="7c524-117">在舊版的 Windows 中，TLS 加密套件和橢圓形曲線是使用單一字串來設定的：</span><span class="sxs-lookup"><span data-stu-id="7c524-117">In earlier versions of Windows, TLS cipher suites and elliptical curves were configured by using a single string:</span></span>

![顯示密碼套件單一字串的圖表。](images/tls-cipher-suite.png)

<span data-ttu-id="7c524-119">不同的 Windows 版本支援不同的 TLS 加密套件和優先權順序。</span><span class="sxs-lookup"><span data-stu-id="7c524-119">Different Windows versions support different TLS cipher suites and priority order.</span></span> <span data-ttu-id="7c524-120">請參閱對應的 Windows 版本，以取得 Microsoft Schannel 提供者選擇的預設順序。</span><span class="sxs-lookup"><span data-stu-id="7c524-120">See the corresponding Windows version for the default order in which they are chosen by the Microsoft Schannel Provider.</span></span>

<span data-ttu-id="7c524-121">**Windows Server 2022：** 如需支援的加密套件的相關資訊，請參閱 [Windows Server 2022 中的 TLS 加密套件](tls-cipher-suites-in-windows-server-2022.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-121">**Windows Server 2022:** For information about supported cipher suites, see [TLS Cipher Suites in Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)</span></span>

<span data-ttu-id="7c524-122">**Windows 10，版本1903：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1903 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1903.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-122">**Windows 10, version 1903:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)</span></span>

<span data-ttu-id="7c524-123">**Windows 10 版本1809：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1809 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1809.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-123">**Windows 10, version 1809:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)</span></span>

<span data-ttu-id="7c524-124">**Windows 10，版本1803：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1803 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1803.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-124">**Windows 10, version 1803:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)</span></span>

<span data-ttu-id="7c524-125">**Windows 10，版本1709：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1709 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1709.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-125">**Windows 10, version 1709:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)</span></span>

<span data-ttu-id="7c524-126">**Windows 10，版本1703：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1703 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1703.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-126">**Windows 10, version 1703:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)</span></span>

<span data-ttu-id="7c524-127">**Windows Server 2016 和 Windows 10 1607 版：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1607 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1607.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-127">**Windows Server 2016 and Windows 10, version 1607:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)</span></span>

<span data-ttu-id="7c524-128">**Windows 10，版本1511：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1511 中的 TLS 加密套件](tls-cipher-suites-in-windows-10-v1511.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-128">**Windows 10, version 1511:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)</span></span>

<span data-ttu-id="7c524-129">**Windows 10，版本1507：** 如需支援的加密套件的相關資訊，請參閱 [Windows 10 v1507 中的 TLS 加密套件](./tls-cipher-suites-in-windows-10--version-1507.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-129">**Windows 10, version 1507:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)</span></span>

<span data-ttu-id="7c524-130">**Windows Server 2012 R2 和 Windows 8.1：** 如需支援的加密套件的相關資訊，請參閱 [Windows 8.1 中的 TLS 加密套件](tls-cipher-suites-in-windows-8-1.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-130">**Windows Server 2012 R2 and Windows 8.1:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 8.1](tls-cipher-suites-in-windows-8-1.md)</span></span>

<span data-ttu-id="7c524-131">**Windows Server 2012 和 Windows 8：** 如需支援的加密套件的相關資訊，請參閱 [Windows 8 中的 TLS 加密套件](tls-cipher-suites-in-windows-8.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-131">**Windows Server 2012 and Windows 8:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 8](tls-cipher-suites-in-windows-8.md)</span></span>

<span data-ttu-id="7c524-132">**Windows Server 2008 R2 和 windows 7：** 如需支援的加密套件的相關資訊，請參閱 [Windows 7 中的 TLS 加密套件](tls-cipher-suites-in-windows-7.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-132">**Windows Server 2008 R2 and Windows 7:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 7](tls-cipher-suites-in-windows-7.md)</span></span>

<span data-ttu-id="7c524-133">**Windows Server 2008 和 Windows Vista：** 如需支援的加密套件的相關資訊，請參閱 [Windows Vista 中的 TLS 加密套件](schannel-cipher-suites-in-windows-vista.md)</span><span class="sxs-lookup"><span data-stu-id="7c524-133">**Windows Server 2008 and Windows Vista:** For information about supported cipher suites, see [TLS Cipher Suites in Windows Vista](schannel-cipher-suites-in-windows-vista.md)</span></span>

<span data-ttu-id="7c524-134">**Windows Server 2003 和 WINDOWS XP：** 如需支援的加密套件的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="7c524-134">**Windows Server 2003 and Windows XP:** For information about supported cipher suites, see the following topics.</span></span>

| <span data-ttu-id="7c524-135">主題</span><span class="sxs-lookup"><span data-stu-id="7c524-135">Topic</span></span>                                                                         | <span data-ttu-id="7c524-136">描述</span><span class="sxs-lookup"><span data-stu-id="7c524-136">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c524-137">TLS 加密套件</span><span class="sxs-lookup"><span data-stu-id="7c524-137">TLS Cipher Suites</span></span>](tls-cipher-suites.md)<br/>                         | <span data-ttu-id="7c524-138">有關 Windows Server 2003 和 Windows XP 中的 TLS 通訊協定所提供之加密套件的資訊。</span><span class="sxs-lookup"><span data-stu-id="7c524-138">Information about the cipher suites available with the TLS protocol in Windows Server 2003 and Windows XP.</span></span><br/>              |
| [<span data-ttu-id="7c524-139">安全通訊端層通訊協定</span><span class="sxs-lookup"><span data-stu-id="7c524-139">Secure Sockets Layer Protocol</span></span>](secure-sockets-layer-protocol.md)<br/> | <span data-ttu-id="7c524-140">SSL 2.0 和3.0 的一般資訊，包括 Windows Server 2003 和 Windows XP 中的可用加密套件。</span><span class="sxs-lookup"><span data-stu-id="7c524-140">General information about SSL 2.0 and 3.0, including the available cipher suites in Windows Server 2003 and Windows XP.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="7c524-141">在 Windows 10 之前，會使用橢圓曲線附加加密套件字串來決定曲線的優先順序。</span><span class="sxs-lookup"><span data-stu-id="7c524-141">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="7c524-142">Windows 10 支援橢圓曲線優先順序順序設定，因此不需要橢圓曲線尾碼，而是在提供時由新的橢圓曲線優先順序順序覆寫，以允許組織使用群組原則，以相同的加密套件來設定不同版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="7c524-142">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>

 

