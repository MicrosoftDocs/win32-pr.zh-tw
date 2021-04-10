---
description: 說明認證管理 API 用來處理的兩種認證。
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: 認證類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944415"
---
# <a name="kinds-of-credentials"></a><span data-ttu-id="aecda-103">認證類型</span><span class="sxs-lookup"><span data-stu-id="aecda-103">Kinds of Credentials</span></span>

<span data-ttu-id="aecda-104">認證管理 API 適用于兩種類型的認證：</span><span class="sxs-lookup"><span data-stu-id="aecda-104">The Credentials Management API works with two kinds of credentials:</span></span>

-   [<span data-ttu-id="aecda-105">網域認證</span><span class="sxs-lookup"><span data-stu-id="aecda-105">Domain Credentials</span></span>](#domain-credentials)
-   [<span data-ttu-id="aecda-106">一般認證</span><span class="sxs-lookup"><span data-stu-id="aecda-106">Generic Credentials</span></span>](#generic-credentials)

## <a name="domain-credentials"></a><span data-ttu-id="aecda-107">網域認證</span><span class="sxs-lookup"><span data-stu-id="aecda-107">Domain Credentials</span></span>

<span data-ttu-id="aecda-108">作業系統會使用網域認證，並由「本地安全機構」 (LSA) 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="aecda-108">Domain credentials are used by the operating system and authenticated by the Local Security Authority (LSA).</span></span> <span data-ttu-id="aecda-109">一般來說，當註冊的安全性套件（例如 Kerberos 通訊協定）驗證使用者所提供的登入資料時，就會建立使用者的網域認證。</span><span class="sxs-lookup"><span data-stu-id="aecda-109">Typically, domain credentials are established for a user when a registered security package, such as the Kerberos protocol, authenticates logon data that is provided by the user.</span></span> <span data-ttu-id="aecda-110">系統會快取登入認證，讓單一登入可讓使用者存取許多不同的資源。</span><span class="sxs-lookup"><span data-stu-id="aecda-110">The logon credentials are cached by the operating system so that a single sign-on gives the user access to many different resources.</span></span> <span data-ttu-id="aecda-111">例如，網路連線可能會以透明的方式進行，而且可以根據使用者的快取網域認證來授與受保護系統物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="aecda-111">For example, network connections can occur transparently, and access to protected system objects can be granted based on the user's cached domain credentials.</span></span>

<span data-ttu-id="aecda-112">認證管理功能提供一種機制，讓應用程式在使用者登入之後提示使用者輸入網域認證，並讓作業系統驗證使用者提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="aecda-112">Credentials Management functions provide a mechanism for applications to prompt a user for domain credentials after the user logs on, and to have the operating system authenticate the information that is provided by the user.</span></span>

<span data-ttu-id="aecda-113">網域認證的秘密部分（密碼）會受到作業系統的保護。</span><span class="sxs-lookup"><span data-stu-id="aecda-113">The secret part of domain credentials, the password, is protected by the operating system.</span></span> <span data-ttu-id="aecda-114">只有使用 LSA 執行同進程的程式碼可以讀取和寫入網域認證。</span><span class="sxs-lookup"><span data-stu-id="aecda-114">Only code running in-process with the LSA can read and write domain credentials.</span></span> <span data-ttu-id="aecda-115">應用程式僅限於寫入網域認證。</span><span class="sxs-lookup"><span data-stu-id="aecda-115">Applications are limited to writing domain credentials.</span></span>

<span data-ttu-id="aecda-116">Windows 支援擴充智慧卡和憑證認證的使用。</span><span class="sxs-lookup"><span data-stu-id="aecda-116">Windows supports expanded use of smart card and certificate credentials.</span></span> <span data-ttu-id="aecda-117">為了協助確保安全性，認證管理 API 永遠不會將智慧卡 PIN 儲存在電腦上。</span><span class="sxs-lookup"><span data-stu-id="aecda-117">To help ensure security, the Credentials Management API never stores the smart card PIN on the computer.</span></span>

## <a name="generic-credentials"></a><span data-ttu-id="aecda-118">一般認證</span><span class="sxs-lookup"><span data-stu-id="aecda-118">Generic Credentials</span></span>

<span data-ttu-id="aecda-119">一般認證是由直接管理授權和安全性的應用程式所定義和驗證，而不是將這些工作委派給作業系統。</span><span class="sxs-lookup"><span data-stu-id="aecda-119">Generic credentials are defined and authenticated by applications that manage authorization and security directly instead of delegating these tasks to the operating system.</span></span> <span data-ttu-id="aecda-120">例如，應用程式可以要求使用者輸入應用程式提供的使用者名稱和密碼，或產生 [*憑證*](../secgloss/c-gly.md) 來存取網站。</span><span class="sxs-lookup"><span data-stu-id="aecda-120">For example, an application can require users to enter a user name and password provided by the application or to produce a [*certificate*](../secgloss/c-gly.md) to access a website.</span></span>

<span data-ttu-id="aecda-121">應用程式會使用認證管理功能來提示使用者提供應用程式定義的一般認證資訊，例如使用者名稱、憑證、智慧卡或密碼。</span><span class="sxs-lookup"><span data-stu-id="aecda-121">Applications use Credentials Management functions to prompt users for application-defined, generic, credential information, such as user name, certificate, smart card, or password.</span></span> <span data-ttu-id="aecda-122">使用者輸入的資訊會傳回給應用程式進行驗證。</span><span class="sxs-lookup"><span data-stu-id="aecda-122">The information entered by the user is returned to the application for authentication.</span></span>

<span data-ttu-id="aecda-123">認證管理提供可自訂的快取管理和一般認證的長期儲存。</span><span class="sxs-lookup"><span data-stu-id="aecda-123">Credentials Management provides customizable cache management and long-term storage for generic credentials.</span></span> <span data-ttu-id="aecda-124">使用者進程可以讀取和寫入一般認證。</span><span class="sxs-lookup"><span data-stu-id="aecda-124">Generic credentials can be read and written by user processes.</span></span>

 

 
