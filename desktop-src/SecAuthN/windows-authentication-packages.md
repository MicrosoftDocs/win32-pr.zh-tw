---
description: Windows 驗證套件會為 LSA 提供的 LsaLogonUser 和 LsaCallAuthenticationPackage 函數實作為封裝專屬的功能，藉此提供驗證服務。
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows 驗證套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511224"
---
# <a name="windows-authentication-packages"></a><span data-ttu-id="f5984-103">Windows 驗證套件</span><span class="sxs-lookup"><span data-stu-id="f5984-103">Windows Authentication Packages</span></span>

<span data-ttu-id="f5984-104">Windows 驗證套件會為 LSA 提供的 [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) 和 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) 函數實作為封裝專屬的功能，藉此提供驗證服務。</span><span class="sxs-lookup"><span data-stu-id="f5984-104">Windows authentication packages provide authentication services by implementing package-specific functionality for the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) and [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) functions provided by the LSA.</span></span>

<span data-ttu-id="f5984-105">MSV1 \_ 0 是 Windows [*驗證套件*](../secgloss/a-gly.md)的範例。</span><span class="sxs-lookup"><span data-stu-id="f5984-105">MSV1\_0 is an example of a Windows [*authentication package*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="f5984-106">MSV1 \_ 0 封裝可接受使用者名稱和 [*雜湊*](../secgloss/h-gly.md) 密碼，這會在 [*安全性帳戶管理員*](../secgloss/s-gly.md) (SAM) 資料庫中查閱。</span><span class="sxs-lookup"><span data-stu-id="f5984-106">The MSV1\_0 package accepts a user name and a [*hashed*](../secgloss/h-gly.md) password, which it looks up in the [*Security Accounts Manager*](../secgloss/s-gly.md) (SAM) database.</span></span> <span data-ttu-id="f5984-107">MSV1 0 authentication 套件會根據查閱結果來 \_ 接受或拒絕驗證嘗試。</span><span class="sxs-lookup"><span data-stu-id="f5984-107">Depending on the results of the lookup, the MSV1\_0 authentication package accepts or rejects the authentication attempt.</span></span>

<span data-ttu-id="f5984-108">如需 LSA 提供的支援函式清單，讓 Windows 驗證需要系統服務的封裝使用，請參閱 [驗證封裝所呼叫的 Lsa 函數](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="f5984-108">For a list of the support functions the LSA provides for use by Windows authentication packages that require system services, see [LSA Functions Called by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="f5984-109">Windows 驗證套件必須執行一組 LSA 所呼叫的函數。</span><span class="sxs-lookup"><span data-stu-id="f5984-109">Windows authentication packages must implement a set of functions that are called by the LSA.</span></span> <span data-ttu-id="f5984-110">如需函式的完整清單，請參閱 [驗證封裝所執行](authentication-functions.md)的函式。</span><span class="sxs-lookup"><span data-stu-id="f5984-110">For the complete list of functions, see [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

 

 
