---
description: 本主題中的資訊適用于 Windows Server 2003 和 Windows XP。
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: 安全通訊端層通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944130"
---
# <a name="secure-sockets-layer-protocol"></a><span data-ttu-id="173e2-103">安全通訊端層通訊協定</span><span class="sxs-lookup"><span data-stu-id="173e2-103">Secure Sockets Layer Protocol</span></span>

<span data-ttu-id="173e2-104">本主題中的資訊適用于 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="173e2-104">The information in this topic applies to Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="173e2-105">如需 Windows Server 2008 和 Windows Vista 的加密套件，請參閱 [Schannel 中的加密套件](cipher-suites-in-schannel.md)。</span><span class="sxs-lookup"><span data-stu-id="173e2-105">For cipher suites for Windows Server 2008 and Windows Vista, see [Cipher Suites in Schannel](cipher-suites-in-schannel.md).</span></span>

<span data-ttu-id="173e2-106">Schannel 支援 [*安全通訊端層 (SSL) 通訊協定*](../secgloss/s-gly.md)的版本2.0 和3.0。</span><span class="sxs-lookup"><span data-stu-id="173e2-106">Schannel supports versions 2.0 and 3.0 of the [*Secure Sockets Layer (SSL) protocol*](../secgloss/s-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="173e2-107">從 Windows 10 開始，1607和 Windows Server 2016 版，SSL 2.0 已經移除，不再受到支援。</span><span class="sxs-lookup"><span data-stu-id="173e2-107">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

 

## <a name="ssl-30"></a><span data-ttu-id="173e2-108">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="173e2-108">SSL 3.0</span></span>

<span data-ttu-id="173e2-109">SSL 3.0 是 [傳輸層安全性通訊協定](transport-layer-security-protocol.md)的前身。</span><span class="sxs-lookup"><span data-stu-id="173e2-109">SSL 3.0 is the predecessor of the [Transport Layer Security Protocol](transport-layer-security-protocol.md).</span></span>

<span data-ttu-id="173e2-110">Schannel 支援 SSL 3.0 的 [TLS 加密套件](tls-cipher-suites.md) 底下所列的加密套件。</span><span class="sxs-lookup"><span data-stu-id="173e2-110">Schannel supports the cipher suites listed under [TLS Cipher Suites](tls-cipher-suites.md) for SSL 3.0.</span></span> <span data-ttu-id="173e2-111">SSL 3.0 支援 TLS 加密套件下所列的所有加密套件，以及 \_ \_ \_ 具有 \_ FORTEZZA \_ CBC \_ SHA 的 ssl FORTEZZA KEA。</span><span class="sxs-lookup"><span data-stu-id="173e2-111">SSL 3.0 supports all of the cipher suites listed under TLS Cipher Suites as well as SSL\_FORTEZZA\_KEA\_WITH\_FORTEZZA\_CBC\_SHA.</span></span>

## <a name="ssl-20"></a><span data-ttu-id="173e2-112">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="173e2-112">SSL 2.0</span></span>

<span data-ttu-id="173e2-113">SSL 2.0 已被 TLS 取代，不應該用於新的開發。</span><span class="sxs-lookup"><span data-stu-id="173e2-113">SSL 2.0 has been superseded by TLS and should not be used for new development.</span></span>

<span data-ttu-id="173e2-114">Schannel 支援 SSL 2.0 的下列加密套件。</span><span class="sxs-lookup"><span data-stu-id="173e2-114">Schannel supports the following cipher suites for SSL 2.0.</span></span> <span data-ttu-id="173e2-115">套件會依最安全到最不安全的順序列出。</span><span class="sxs-lookup"><span data-stu-id="173e2-115">The suites are listed in order from most secure to least secure.</span></span>

-   <span data-ttu-id="173e2-116">\_ \_ \_ 使用 MD5 的 SSL RC4 128 \_</span><span class="sxs-lookup"><span data-stu-id="173e2-116">SSL\_RC4\_128\_WITH\_MD5</span></span>
-   <span data-ttu-id="173e2-117">\_ \_ \_ \_ \_ 使用 \_ MD5 的 SSL DES 192 EDE3 CBC</span><span class="sxs-lookup"><span data-stu-id="173e2-117">SSL\_DES\_192\_EDE3\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="173e2-118">\_ \_ \_ \_ \_ 使用 \_ MD5 的 SSL RC2 cbc 128 CBC</span><span class="sxs-lookup"><span data-stu-id="173e2-118">SSL\_RC2\_CBC\_128\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="173e2-119">\_ \_ \_ \_ 使用 MD5 的 SSL DES 64 CBC \_</span><span class="sxs-lookup"><span data-stu-id="173e2-119">SSL\_DES\_64\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="173e2-120">\_ \_ \_ \_ 使用 MD5 的 SSL RC4 128 EXPORT40 \_</span><span class="sxs-lookup"><span data-stu-id="173e2-120">SSL\_RC4\_128\_EXPORT40\_WITH\_MD5</span></span>

 

 
