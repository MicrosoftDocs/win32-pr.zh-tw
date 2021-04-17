---
title: 使用 Kerberos 進行相互驗證的限制
description: 用戶端的帳戶和服務的帳戶必須在 Windows 2000 原生或混合模式網域中，因為在舊版網域中無法使用 Kerberos 服務。
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462016"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a><span data-ttu-id="798ab-103">使用 Kerberos 進行相互驗證的限制</span><span class="sxs-lookup"><span data-stu-id="798ab-103">Limitations of Mutual Authentication with Kerberos</span></span>

<span data-ttu-id="798ab-104">用戶端的帳戶和服務的帳戶必須在 Windows 2000 原生或混合模式網域中，因為在舊版網域中無法使用 Kerberos 服務。</span><span class="sxs-lookup"><span data-stu-id="798ab-104">Both the client's account and the service's account must be in Windows 2000 native or mixed-mode domains because Kerberos services are not available in downlevel domains.</span></span> <span data-ttu-id="798ab-105">此外，用戶端和服務帳戶都必須位於相同的樹系中，因為用戶端的 KDC 會使用通用類別目錄來搜尋服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="798ab-105">In addition, both client and service accounts must be in the same forest because the client's KDC uses the global catalog to search for the service principal name.</span></span>

<span data-ttu-id="798ab-106">服務和用戶端都必須在 Windows 2000 上執行，否則 Kerberos 的相互驗證將會失敗，因為舊版 Windows 不支援 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="798ab-106">Both service and client must be running on Windows 2000, otherwise mutual authentication with Kerberos will fail because earlier versions of Windows do not support Kerberos.</span></span>

<span data-ttu-id="798ab-107">服務主體名稱必須包含執行服務之主機伺服器的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="798ab-107">Service principal names must include the DNS name of the host server on which the service is running.</span></span> <span data-ttu-id="798ab-108">您必須使用 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="798ab-108">You must use the DNS name.</span></span>

 

 




