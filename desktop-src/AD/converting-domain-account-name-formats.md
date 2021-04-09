---
title: 轉換網域帳戶名稱格式
description: 在主機伺服器上使用服務控制管理員 (SCM) 的 Microsoft Win32 函數使用 \ 0034;網域 \\ 使用者名稱 \ 0034; 服務帳戶的格式。
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681684"
---
# <a name="converting-domain-account-name-formats"></a><span data-ttu-id="81d1c-103">轉換網域帳戶名稱格式</span><span class="sxs-lookup"><span data-stu-id="81d1c-103">Converting Domain Account Name Formats</span></span>

<span data-ttu-id="81d1c-104">在主機伺服器上使用「服務控制管理員」 (SCM) 的 Microsoft Win32 函數會使用「 <domain> \\ <username> 服務帳戶」的格式。</span><span class="sxs-lookup"><span data-stu-id="81d1c-104">The Microsoft Win32 functions for working with the service control manager (SCM) on a host server use the "<domain>\\<username>" format for service accounts.</span></span> <span data-ttu-id="81d1c-105">例如，如果您呼叫 [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) 函式來抓取用來執行服務的使用者帳戶，則此函式會傳回 "Fabrikam \\ jeffsmith" 格式的名稱。</span><span class="sxs-lookup"><span data-stu-id="81d1c-105">For example, if you call the [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) function to retrieve the user account under which your service runs, the function returns the name in "Fabrikam\\jeffsmith" format.</span></span> <span data-ttu-id="81d1c-106">若要系結至目錄中的使用者帳戶（例如變更帳戶密碼），需要帳戶的辨別名稱，其格式為 "CN = Jeff Smith，CN = Users，DC = Fabrikam，DC = COM"。</span><span class="sxs-lookup"><span data-stu-id="81d1c-106">To bind to the user account in the directory, for example to change the account password, the distinguished name of the account is required, which has the format "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM".</span></span>

<span data-ttu-id="81d1c-107">若要在各種名稱格式之間進行轉換，請使用 [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) 函式，此函式可以將名稱轉換為其他格式，例如 (UPN) 的使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="81d1c-107">To convert between the various name formats, use the [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) function, which can convert a name to other formats, such as a user principal name (UPN).</span></span>

 

 