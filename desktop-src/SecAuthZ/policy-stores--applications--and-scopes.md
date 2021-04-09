---
description: 授權原則存放區、應用程式和範圍代表授權管理員原則的不同層級。
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: 原則存放區、應用程式和範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848245"
---
# <a name="policy-stores-applications-and-scopes"></a><span data-ttu-id="6fecb-103">原則存放區、應用程式和範圍</span><span class="sxs-lookup"><span data-stu-id="6fecb-103">Policy Stores, Applications, and Scopes</span></span>

<span data-ttu-id="6fecb-104">授權原則存放區、應用程式和範圍代表授權管理員原則的不同層級。</span><span class="sxs-lookup"><span data-stu-id="6fecb-104">Authorization policy stores, applications, and scopes represent different levels of organization of Authorization Manager policy.</span></span> <span data-ttu-id="6fecb-105">原則存放區可包含一或多個應用程式，且應用程式可以包含一或多個範圍。</span><span class="sxs-lookup"><span data-stu-id="6fecb-105">A policy store can contain one or more applications, and an application can contain one or more scopes.</span></span>

-   [<span data-ttu-id="6fecb-106">授權原則存放區</span><span class="sxs-lookup"><span data-stu-id="6fecb-106">Authorization Policy Stores</span></span>](#authorization-policy-stores)
-   [<span data-ttu-id="6fecb-107">應用程式</span><span class="sxs-lookup"><span data-stu-id="6fecb-107">Applications</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="6fecb-108">範圍</span><span class="sxs-lookup"><span data-stu-id="6fecb-108">Scopes</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="6fecb-109">委派</span><span class="sxs-lookup"><span data-stu-id="6fecb-109">Delegation</span></span>](#delegation)
-   [<span data-ttu-id="6fecb-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="6fecb-110">Related topics</span></span>](#related-topics)

## <a name="authorization-policy-stores"></a><span data-ttu-id="6fecb-111">授權原則存放區</span><span class="sxs-lookup"><span data-stu-id="6fecb-111">Authorization Policy Stores</span></span>

<span data-ttu-id="6fecb-112">在授權管理員 API 中，授權原則存放區會以 [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="6fecb-112">In the Authorization Manager API, an authorization policy store is represented by an [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="6fecb-113">授權原則存放區包含應用程式、範圍、作業、工作、角色和使用者群組的定義和指派。</span><span class="sxs-lookup"><span data-stu-id="6fecb-113">The authorization policy store contains definitions and assignments of applications, scopes, operations, tasks, roles, and user groups.</span></span>

<span data-ttu-id="6fecb-114">授權原則存放區可以儲存為 XML 檔案，或儲存在 Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="6fecb-114">An authorization policy store can be stored either as an XML file or in Active Directory.</span></span>

<span data-ttu-id="6fecb-115">應用程式必須先初始化授權原則存放區，才能變更存放區中的資訊，或使用存放區原則來檢查用戶端對資源的存取。</span><span class="sxs-lookup"><span data-stu-id="6fecb-115">An application must initialize an authorization policy store before changing information in the store or using the store policy to check client access to resources.</span></span>

<span data-ttu-id="6fecb-116">授權原則存放區可以包含一或多個 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件，每個物件都代表特定應用程式的授權原則。</span><span class="sxs-lookup"><span data-stu-id="6fecb-116">An authorization policy store can contain one or more [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) objects that each represent authorization policy for a specific application.</span></span>

## <a name="applications"></a><span data-ttu-id="6fecb-117">應用程式</span><span class="sxs-lookup"><span data-stu-id="6fecb-117">Applications</span></span>

<span data-ttu-id="6fecb-118">在授權管理員 API 中，應用程式是以 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="6fecb-118">In the Authorization Manager API, an application is represented by an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object.</span></span> <span data-ttu-id="6fecb-119">授權原則存放區可包含許多應用程式的授權原則資訊。</span><span class="sxs-lookup"><span data-stu-id="6fecb-119">An authorization policy store can contain authorization policy information for many applications.</span></span> <span data-ttu-id="6fecb-120">使用 **IAzApplication** 物件可讓您將不同應用程式的不同授權原則儲存在單一原則存放區中。</span><span class="sxs-lookup"><span data-stu-id="6fecb-120">Using **IAzApplication** objects allows you to store different authorization policy for different applications in a single policy store.</span></span>

<span data-ttu-id="6fecb-121">一個授權原則存放至少必須包含一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="6fecb-121">An authorization policy store must contain at least one application.</span></span>

## <a name="scopes"></a><span data-ttu-id="6fecb-122">範圍</span><span class="sxs-lookup"><span data-stu-id="6fecb-122">Scopes</span></span>

<span data-ttu-id="6fecb-123">在授權管理員 API 中，範圍是由 [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="6fecb-123">In the Authorization Manager API, a scope is represented by an [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span> <span data-ttu-id="6fecb-124">範圍為授權原則提供額外的選擇性組織層級。</span><span class="sxs-lookup"><span data-stu-id="6fecb-124">Scopes provide an additional, optional level of organization for an authorization policy.</span></span> <span data-ttu-id="6fecb-125">應用程式可包含一或多個範圍，但不需要包含任何 (授權管理員提供預設的全應用程式範圍) 。</span><span class="sxs-lookup"><span data-stu-id="6fecb-125">An application can contain one or more scopes, but need not contain any (Authorization Manager provides a default, application-wide scope).</span></span>

<span data-ttu-id="6fecb-126">範圍是應用程式內的細分，可將資源與該應用程式所使用的其他資源分隔開來。</span><span class="sxs-lookup"><span data-stu-id="6fecb-126">A scope is a subdivision within an application that separates resources from other resources that are used by that application.</span></span> <span data-ttu-id="6fecb-127">若有不想將其套用於整個應用程式的授權管理員群組、角色指派、角色定義或工作定義，請將它們建立為領域層級。</span><span class="sxs-lookup"><span data-stu-id="6fecb-127">If you have Authorization Manager groups, role assignments, role definitions, or task definitions that you do not want to apply to an entire application, you can create them at the scope level.</span></span>

## <a name="delegation"></a><span data-ttu-id="6fecb-128">委派</span><span class="sxs-lookup"><span data-stu-id="6fecb-128">Delegation</span></span>

<span data-ttu-id="6fecb-129">儲存在 Active Directory 支援管理委派的授權原則存放區。</span><span class="sxs-lookup"><span data-stu-id="6fecb-129">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="6fecb-130">系統管理可以委派給存放區、應用程式或範圍層級的使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="6fecb-130">Administration can be delegated to users and groups at the store, application, or scope level.</span></span> <span data-ttu-id="6fecb-131">每個層級都會定義該層級之原則的系統管理角色。</span><span class="sxs-lookup"><span data-stu-id="6fecb-131">Each level defines administrative roles for the policy at that level.</span></span> <span data-ttu-id="6fecb-132">若要將控制項委派給使用者或群組，請將控制權指派給系統管理員角色。若要允許使用者或群組讀取原則，請將其指派給 [讀者] 角色。</span><span class="sxs-lookup"><span data-stu-id="6fecb-132">To delegate control to a user or group, assign them to the administrator role; to allow a user or group to read the policy, assign them to the reader role.</span></span>

<span data-ttu-id="6fecb-133">存放區、應用程式或範圍的系統管理員可以讀取和修改委派層級的原則存放區。</span><span class="sxs-lookup"><span data-stu-id="6fecb-133">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="6fecb-134">讀取器可以讀取委派層級的原則存放區，但無法修改存放區。</span><span class="sxs-lookup"><span data-stu-id="6fecb-134">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fecb-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="6fecb-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fecb-136">在 c + + 中建立授權原則存放區物件</span><span class="sxs-lookup"><span data-stu-id="6fecb-136">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="6fecb-137">在 c + + 中建立應用程式物件</span><span class="sxs-lookup"><span data-stu-id="6fecb-137">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="6fecb-138">委派 c + + 中的許可權定義</span><span class="sxs-lookup"><span data-stu-id="6fecb-138">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



