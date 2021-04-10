---
title: 今天的目錄服務
description: 通常會在單一組織內找到多個系統管理目錄。
ms.assetid: e6f05beb-d88d-46d5-85c7-3477a6af03c9
ms.tgt_platform: multiple
keywords:
- 目錄服務 ADSI
- 目錄服務 ADSI、目錄服務背景
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e6a6e5dfd1e0f8fc3f87d407bbbce28caa0696
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182992"
---
# <a name="directory-services-today"></a><span data-ttu-id="8266c-105">今天的目錄服務</span><span class="sxs-lookup"><span data-stu-id="8266c-105">Directory Services Today</span></span>

<span data-ttu-id="8266c-106">通常會在單一組織內找到多個系統管理目錄。</span><span class="sxs-lookup"><span data-stu-id="8266c-106">It is common to find multiple administrative directories deployed within a single organization.</span></span> <span data-ttu-id="8266c-107">這些目錄包含網路資源目錄，例如以 LDAP 為基礎的目錄，例如 Microsoft Active Directory directory 服務、Windows 作業系統目錄服務，以及應用程式特定目錄，例如 Microsoft Exchange。</span><span class="sxs-lookup"><span data-stu-id="8266c-107">These directories include network resource directories, such as LDAP-based directories like Microsoft Active Directory directory service, Windows operating system directory service, as well as application-specific directories, such as Microsoft Exchange.</span></span>

![部署多個目錄](images/ds2chal.png)

## <a name="the-directory-challenge"></a><span data-ttu-id="8266c-109">目錄挑戰</span><span class="sxs-lookup"><span data-stu-id="8266c-109">The Directory Challenge</span></span>

<span data-ttu-id="8266c-110">組織中的多個目錄對使用者、系統管理員和開發人員而言，會造成複雜的挑戰。</span><span class="sxs-lookup"><span data-stu-id="8266c-110">Multiple directories in the organization pose complex challenges to users, administrators, and developers.</span></span> <span data-ttu-id="8266c-111">這些問題具有有限的全目錄部署。</span><span class="sxs-lookup"><span data-stu-id="8266c-111">These problems have limited wide-directory deployment.</span></span> <span data-ttu-id="8266c-112">使用者會在多個目錄之間，面對多個登入和各種介面的資訊。</span><span class="sxs-lookup"><span data-stu-id="8266c-112">Users face multiple logons and a variety of interfaces to information across multiple directories.</span></span> <span data-ttu-id="8266c-113">系統管理員面臨管理多個目錄的複雜性。</span><span class="sxs-lookup"><span data-stu-id="8266c-113">Administrators face the complexity of managing multiple directories.</span></span> <span data-ttu-id="8266c-114">終端使用者和系統管理員想要讓應用程式開發人員使用現有的系統管理目錄，但開發人員會面臨有關要使用哪一個的困境。</span><span class="sxs-lookup"><span data-stu-id="8266c-114">End users and administrators want application developers to use an existing administrative directory, but developers face a dilemma about which one to use.</span></span> <span data-ttu-id="8266c-115">每個目錄都提供獨特的應用程式介面。</span><span class="sxs-lookup"><span data-stu-id="8266c-115">Each directory offers unique application interfaces.</span></span> <span data-ttu-id="8266c-116">開發人員必須選擇特定的目錄執行，或支援其應用程式的多個版本。</span><span class="sxs-lookup"><span data-stu-id="8266c-116">A developer must choose a specific directory implementation, or support multiple versions of their application.</span></span> <span data-ttu-id="8266c-117">因此，開發人員很少會使用現有的目錄服務。</span><span class="sxs-lookup"><span data-stu-id="8266c-117">As a result, developers rarely use existing directory services.</span></span>

 

 




