---
description: 安全通道通訊協定需要認證，以驗證服務器和用戶端（選擇性）。
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Schannel 認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944132"
---
# <a name="schannel-credentials"></a><span data-ttu-id="f2855-103">Schannel 認證</span><span class="sxs-lookup"><span data-stu-id="f2855-103">Schannel Credentials</span></span>

<span data-ttu-id="f2855-104">安全通道通訊協定需要認證，以驗證服務器和用戶端（選擇性）。</span><span class="sxs-lookup"><span data-stu-id="f2855-104">Schannel protocols require credentials to authenticate servers and optionally, clients.</span></span> <span data-ttu-id="f2855-105">[*安全通道安全性通訊協定*](../secgloss/s-gly.md)需要伺服器驗證（伺服器會將其身分識別證明提供給用戶端）。</span><span class="sxs-lookup"><span data-stu-id="f2855-105">Server authentication, where the server provides proof of its identity to the client, is required by the Schannel [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="f2855-106">伺服器可能會在任何時間要求用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="f2855-106">Client authentication may be requested by the server at any time.</span></span>

<span data-ttu-id="f2855-107">Schannel 認證是 [*x.509*](../secgloss/x-gly.md) 憑證。</span><span class="sxs-lookup"><span data-stu-id="f2855-107">Schannel credentials are [*X.509*](../secgloss/x-gly.md) certificates.</span></span> <span data-ttu-id="f2855-108">憑證的 [*公開*](../secgloss/p-gly.md)和 [*私密金鑰*](../secgloss/p-gly.md)資訊可用來驗證服務器和用戶端（選擇性）。</span><span class="sxs-lookup"><span data-stu-id="f2855-108">[*Public*](../secgloss/p-gly.md) and [*private key*](../secgloss/p-gly.md) information from certificates is used to authenticate the server and optionally, the client.</span></span> <span data-ttu-id="f2855-109">當用戶端和伺服器交換產生和交換 [*工作階段金鑰*](../secgloss/s-gly.md)所需的資訊時，也會使用這些金鑰來提供訊息 [*完整性*](../secgloss/i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="f2855-109">These keys are also used to provide message [*integrity*](../secgloss/i-gly.md) while client and server exchange the information required to generate and exchange [*session keys*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="f2855-110">如需程式設計資訊，請參閱 [取得 Schannel 認證](obtaining-schannel-credentials.md)。</span><span class="sxs-lookup"><span data-stu-id="f2855-110">For programming information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
