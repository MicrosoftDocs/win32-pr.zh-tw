---
description: TLS 是與 SSL 3.0 密切相關的標準，有時也稱為 &\# 0034;SSL 3.1&\# 0034;。
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS 與 SSL 的比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac1a2e783b6f3355127a3148f1575f73119f6604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979297"
---
# <a name="tls-vs-ssl"></a><span data-ttu-id="d1919-103">TLS 與 SSL 的比較</span><span class="sxs-lookup"><span data-stu-id="d1919-103">TLS vs. SSL</span></span>

<span data-ttu-id="d1919-104">TLS 是與 SSL 3.0 密切相關的標準，有時也稱為「SSL 3.1」。</span><span class="sxs-lookup"><span data-stu-id="d1919-104">TLS is a standard closely related to SSL 3.0, and is sometimes referred to as "SSL 3.1".</span></span> <span data-ttu-id="d1919-105">TLS 取代 SSL 2.0，應該用於新的開發。</span><span class="sxs-lookup"><span data-stu-id="d1919-105">TLS supersedes SSL 2.0 and should be used in new development.</span></span> <span data-ttu-id="d1919-106">從 Windows 10 開始，1607和 Windows Server 2016 版，SSL 2.0 已經移除，不再受到支援。</span><span class="sxs-lookup"><span data-stu-id="d1919-106">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

<span data-ttu-id="d1919-107">需要高層級互通性的應用程式應支援 SSL 3.0 和 TLS。</span><span class="sxs-lookup"><span data-stu-id="d1919-107">Applications that require a high level of interoperability should support SSL 3.0 and TLS.</span></span> <span data-ttu-id="d1919-108">因為這兩個通訊協定之間的相似之處，所以不會在此檔中包含 SSL 詳細資料，除非它們與 TLS 不同。</span><span class="sxs-lookup"><span data-stu-id="d1919-108">Because of the similarities between these two protocols, SSL details are not included in this documentation, except where they differ from TLS.</span></span> <span data-ttu-id="d1919-109">以下是來自 [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt)：</span><span class="sxs-lookup"><span data-stu-id="d1919-109">The following is from [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span></span>

<span data-ttu-id="d1919-110">「此通訊協定和 SSL 3.0 之間的差異並不大，但它們的重要性足以讓 TLS 1.0 和 SSL 3.0 不會 (交互操作，不過 TLS 1.0 所併入的機制，可讓 TLS 的執行可回到 SSL 3.0) 。」</span><span class="sxs-lookup"><span data-stu-id="d1919-110">"The differences between this protocol and SSL 3.0 are not dramatic, but they are significant enough that TLS 1.0 and SSL 3.0 do not interoperate (although TLS 1.0 does incorporate a mechanism by which a TLS implementation can back down to SSL 3.0)."</span></span>

 

 



