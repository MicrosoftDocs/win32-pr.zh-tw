---
description: Windows 作業系統支援使用安全性封裝（以安全性支援提供者和驗證套件的形式）來進行驗證。
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: 安全性支援提供者/驗證套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974659"
---
# <a name="security-support-providerauthentication-packages"></a><span data-ttu-id="150aa-103">安全性支援提供者/驗證套件</span><span class="sxs-lookup"><span data-stu-id="150aa-103">Security Support Provider/Authentication Packages</span></span>

<span data-ttu-id="150aa-104">Windows 作業系統支援使用 [*安全性封裝*](../secgloss/s-gly.md) （以 [*安全性支援提供者*](../secgloss/s-gly.md) 和 [*驗證套件*](../secgloss/a-gly.md)的形式）來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="150aa-104">The Windows operating system supports authentication using [*security packages*](../secgloss/s-gly.md) that function as both [*security support providers*](../secgloss/s-gly.md) and as [*authentication packages*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="150aa-105">安全性套件提供 Windows 驗證套件的登入程式支援服務，也會藉由執行一組對應至 [安全性支援提供者介面](sspi.md) 的函式（ (SSPI) ），為應用程式提供驗證服務。</span><span class="sxs-lookup"><span data-stu-id="150aa-105">Security packages provide the logon process support services of a Windows authentication package and also provide authentication services to applications by implementing a set of functions that are mapped to the [Security Support Provider Interface](sspi.md) (SSPI).</span></span>

<span data-ttu-id="150aa-106">作為驗證套件並執行 [*SSPI*](../secgloss/s-gly.md) 所需功能的安全性封裝，稱為安全性支援提供者/驗證套件 (SSP/AP) 。</span><span class="sxs-lookup"><span data-stu-id="150aa-106">A security package that functions as an authentication package and implements the functionality required by [*SSPI*](../secgloss/s-gly.md) is called a security support provider/authentication package (SSP/AP).</span></span>

<span data-ttu-id="150aa-107">如需安全性封裝的詳細資訊，請參閱 [Microsoft 提供的 SSP 套件](ssp-packages-provided-by-microsoft.md)。</span><span class="sxs-lookup"><span data-stu-id="150aa-107">For more information about security packages, see [SSP Packages Provided by Microsoft](ssp-packages-provided-by-microsoft.md).</span></span> <span data-ttu-id="150aa-108">如需有關開發自訂 SSP/Ap 的詳細資訊，請參閱 [自訂安全性封裝](custom-security-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="150aa-108">For information about developing custom SSP/APs, see [Custom Security Packages](custom-security-packages.md).</span></span>

 

 
