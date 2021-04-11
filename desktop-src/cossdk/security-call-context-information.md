---
description: 安全性呼叫內容資訊
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: 安全性呼叫內容資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191025"
---
# <a name="security-call-context-information"></a><span data-ttu-id="ae3eb-103">安全性呼叫內容資訊</span><span class="sxs-lookup"><span data-stu-id="ae3eb-103">Security Call Context Information</span></span>

<span data-ttu-id="ae3eb-104">以角色為基礎的安全性建基於一般機制，可讓您在對您的元件發出呼叫的鏈中，取得有關所有上游呼叫端的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-104">Role-based security is built on a general mechanism that enables you to retrieve security information regarding all upstream callers in the chain of calls to your component.</span></span> <span data-ttu-id="ae3eb-105">只有當您啟用元件層級角色檢查時，才能使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-105">This information is available only when you have component-level role checking enabled.</span></span> <span data-ttu-id="ae3eb-106">如需有關如何設定元件層級安全性的詳細資訊，請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md)。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-106">For details about how to set component-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="ae3eb-107">您可以使用 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) 介面，以程式設計方式存取安全性呼叫內容資訊。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-107">You can use the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface to access security call context information programmatically.</span></span> <span data-ttu-id="ae3eb-108">如需描述，請參閱程式 [設計元件安全性](programmatic-component-security.md)。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-108">For a description, see [Programmatic Component Security](programmatic-component-security.md).</span></span>

<span data-ttu-id="ae3eb-109">每次超過安全性界限時，都會傳遞安全性呼叫內容。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-109">Security call context is passed along every time a security boundary is crossed.</span></span> <span data-ttu-id="ae3eb-110">針對位於相同安全性界限內的應用程式中元件之間的呼叫，不會傳遞任何呼叫內容資訊。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-110">For calls between components within an application, which reside within the same security boundary, no call context information is passed.</span></span> <span data-ttu-id="ae3eb-111">對於進程之間或進程內的應用程式之間的呼叫，呼叫內容資訊流程。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-111">For calls between processes or between applications within a process, call context information flows along.</span></span>

<span data-ttu-id="ae3eb-112">如果您想要進行詳細的審核和記錄，這項功能特別有用。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-112">This facility is particularly useful if you wish to do detailed auditing and logging.</span></span> <span data-ttu-id="ae3eb-113">您可以取得並記錄每個上游呼叫端的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="ae3eb-113">You can retrieve and record security information for every upstream caller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae3eb-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="ae3eb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae3eb-115">有效設計角色</span><span class="sxs-lookup"><span data-stu-id="ae3eb-115">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="ae3eb-116">安全性界限</span><span class="sxs-lookup"><span data-stu-id="ae3eb-116">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="ae3eb-117">資訊安全內容屬性</span><span class="sxs-lookup"><span data-stu-id="ae3eb-117">Security Context Property</span></span>](security-context-property.md)
</dt> <dt>

[<span data-ttu-id="ae3eb-118">使用角色進行用戶端授權</span><span class="sxs-lookup"><span data-stu-id="ae3eb-118">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



