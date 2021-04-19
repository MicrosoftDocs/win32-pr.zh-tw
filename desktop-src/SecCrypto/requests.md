---
description: 憑證服務支援以 PKCS \# 10 格式和 Keygen (Netscape) 格式為基礎的憑證要求。 憑證服務也支援 \# (CMS) 要求的 PKCS 7 更新要求和密碼編譯訊息語法。
ms.assetid: 6321ce99-f5d1-4d72-a062-99cffb543731
title: Requests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7870e09d930fb06d50f0cc8acfff1270db1c92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997822"
---
# <a name="requests"></a><span data-ttu-id="c11fe-104">Requests</span><span class="sxs-lookup"><span data-stu-id="c11fe-104">Requests</span></span>

<span data-ttu-id="c11fe-105">憑證服務支援[](../secgloss/c-gly.md)以 PKCS \# 10 格式和 Keygen (Netscape) 格式為基礎的憑證要求。</span><span class="sxs-lookup"><span data-stu-id="c11fe-105">Certificate Services supports [*certificate requests*](../secgloss/c-gly.md) based on the PKCS \#10 format and the Keygen (Netscape) format.</span></span> <span data-ttu-id="c11fe-106">憑證服務也支援 \# (CMS) 要求的 PKCS 7 更新要求和密碼編譯訊息語法。</span><span class="sxs-lookup"><span data-stu-id="c11fe-106">Certificate Services also supports PKCS \#7 renewal requests and Cryptographic Message Syntax (CMS) requests.</span></span>

<span data-ttu-id="c11fe-107">憑證服務也會提供 [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) 介面，其中包含提交憑證要求的方法，以及 (是否已核准接收所產生之已發行憑證的) 。</span><span class="sxs-lookup"><span data-stu-id="c11fe-107">Certificate Services also provides an [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) interface, which contains methods for submitting a certificate request and (if the request is approved) for receiving the resulting issued certificate.</span></span>

<span data-ttu-id="c11fe-108">[憑證註冊控制項](certificate-enrollment-control.md)中提供其他安全性相關的介面。</span><span class="sxs-lookup"><span data-stu-id="c11fe-108">Additional security-related interfaces are available in the [Certificate Enrollment Control](certificate-enrollment-control.md).</span></span>

 

 
