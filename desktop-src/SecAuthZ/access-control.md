---
description: 存取控制是指可控制哪些人可以存取作業系統中資源的安全性功能。 應用程式會呼叫存取控制功能，以設定可以存取特定資源的人員，或控制應用程式所提供資源的存取權。
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: " (授權) 的存取控制"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026626"
---
# <a name="access-control-authorization"></a><span data-ttu-id="c4444-104"> (授權) 的存取控制</span><span class="sxs-lookup"><span data-stu-id="c4444-104">Access Control (Authorization)</span></span>

<span data-ttu-id="c4444-105">存取控制是指可控制哪些人可以存取作業系統中資源的安全性功能。</span><span class="sxs-lookup"><span data-stu-id="c4444-105">Access control refers to security features that control who can access resources in the operating system.</span></span> <span data-ttu-id="c4444-106">應用程式會呼叫存取控制功能，以設定可以存取特定資源的人員，或控制應用程式所提供資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="c4444-106">Applications call access control functions to set who can access specific resources or control access to resources provided by the application.</span></span>

<span data-ttu-id="c4444-107">本總覽說明用來控制對 Windows 物件（例如檔案）的存取，以及控制系統管理功能存取權的安全性模型，例如設定系統時間或審核使用者動作。</span><span class="sxs-lookup"><span data-stu-id="c4444-107">This overview describes the security model for controlling access to Windows objects, such as files, and for controlling access to administrative functions, such as setting the system time or auditing user actions.</span></span> <span data-ttu-id="c4444-108">[存取控制模型](access-control-model.md)主題提供存取控制元件的概要說明，以及它們彼此互動的方式。</span><span class="sxs-lookup"><span data-stu-id="c4444-108">The [Access Control Model](access-control-model.md) topic provides a high-level description of the parts of access control and how they interact with each other.</span></span>

<span data-ttu-id="c4444-109">下列主題說明存取控制：</span><span class="sxs-lookup"><span data-stu-id="c4444-109">The following topics describe access control:</span></span>

-   [<span data-ttu-id="c4444-110">C2 層級安全性</span><span class="sxs-lookup"><span data-stu-id="c4444-110">C2-level Security</span></span>](c2-level-security.md)
-   [<span data-ttu-id="c4444-111">存取控制模型</span><span class="sxs-lookup"><span data-stu-id="c4444-111">Access Control Model</span></span>](access-control-model.md)
-   [<span data-ttu-id="c4444-112">安全描述項定義語言</span><span class="sxs-lookup"><span data-stu-id="c4444-112">Security Descriptor Definition Language</span></span>](security-descriptor-definition-language.md)
-   [<span data-ttu-id="c4444-113">特權</span><span class="sxs-lookup"><span data-stu-id="c4444-113">Privileges</span></span>](privileges.md)
-   [<span data-ttu-id="c4444-114">稽核產生</span><span class="sxs-lookup"><span data-stu-id="c4444-114">Audit Generation</span></span>](audit-generation.md)
-   [<span data-ttu-id="c4444-115">安全物件</span><span class="sxs-lookup"><span data-stu-id="c4444-115">Securable Objects</span></span>](securable-objects.md)
-   [<span data-ttu-id="c4444-116">低層級存取控制</span><span class="sxs-lookup"><span data-stu-id="c4444-116">Low-level Access Control</span></span>](low-level-access-control.md)

<span data-ttu-id="c4444-117">以下是常見的存取控制工作：</span><span class="sxs-lookup"><span data-stu-id="c4444-117">The following are common access control tasks:</span></span>

-   [<span data-ttu-id="c4444-118">Dacl 如何控制物件的存取</span><span class="sxs-lookup"><span data-stu-id="c4444-118">How DACLs Control Access to an Object</span></span>](how-dacls-control-access-to-an-object.md)
-   [<span data-ttu-id="c4444-119">控制在 c + + 中建立子物件</span><span class="sxs-lookup"><span data-stu-id="c4444-119">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="c4444-120">用來控制物件屬性存取權的 Ace</span><span class="sxs-lookup"><span data-stu-id="c4444-120">ACEs to Control Access to an Object's Properties</span></span>](aces-to-control-access-to-an-object-s-properties.md)
-   [<span data-ttu-id="c4444-121">要求存取物件的存取權限</span><span class="sxs-lookup"><span data-stu-id="c4444-121">Requesting Access Rights to an Object</span></span>](requesting-access-rights-to-an-object.md)

<span data-ttu-id="c4444-122">下列主題提供存取控制工作的範例程式碼：</span><span class="sxs-lookup"><span data-stu-id="c4444-122">The following topics provide example code for access control tasks:</span></span>

-   [<span data-ttu-id="c4444-123">使用 c + + 修改物件的 Acl</span><span class="sxs-lookup"><span data-stu-id="c4444-123">Modifying the ACLs of an Object in C++</span></span>](modifying-the-acls-of-an-object-in-c--.md)
-   [<span data-ttu-id="c4444-124">在 c + + 中建立新物件的安全描述項</span><span class="sxs-lookup"><span data-stu-id="c4444-124">Creating a Security Descriptor for a New Object in C++</span></span>](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [<span data-ttu-id="c4444-125">控制在 c + + 中建立子物件</span><span class="sxs-lookup"><span data-stu-id="c4444-125">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="c4444-126">在 c + + 中啟用和停用許可權</span><span class="sxs-lookup"><span data-stu-id="c4444-126">Enabling and Disabling Privileges in C++</span></span>](enabling-and-disabling-privileges-in-c--.md)
-   [<span data-ttu-id="c4444-127">在 c + + 中以存取權杖搜尋 SID</span><span class="sxs-lookup"><span data-stu-id="c4444-127">Searching for a SID in an Access Token in C++</span></span>](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [<span data-ttu-id="c4444-128">在 c + + 中尋找檔案物件的擁有者</span><span class="sxs-lookup"><span data-stu-id="c4444-128">Finding the Owner of a File Object in C++</span></span>](finding-the-owner-of-a-file-object-in-c--.md)
-   [<span data-ttu-id="c4444-129">以 c + + 取得物件擁有權</span><span class="sxs-lookup"><span data-stu-id="c4444-129">Taking Object Ownership in C++</span></span>](taking-object-ownership-in-c--.md)
-   [<span data-ttu-id="c4444-130">建立 DACL</span><span class="sxs-lookup"><span data-stu-id="c4444-130">Creating a DACL</span></span>](/windows/desktop/SecBP/creating-a-dacl)

 

 
