---
description: 如果您的 COM + 應用程式使用以角色為基礎的安全性，則需要完成幾項工作。
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: 設定 Role-Based 安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317832"
---
# <a name="configuring-role-based-security"></a><span data-ttu-id="cbb0c-103">設定 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="cbb0c-103">Configuring Role-Based Security</span></span>

<span data-ttu-id="cbb0c-104">如果您的 COM + 應用程式使用以角色為基礎的安全性，則需要完成幾項工作。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-104">If your COM+ application uses role-based security, there are several tasks that need to be completed.</span></span> <span data-ttu-id="cbb0c-105">在您的應用程式中設計元件時，您會定義協助保護這些元件存取權所需的角色。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-105">When designing the components in your application, you define the roles that are necessary to help protect access to those components.</span></span> <span data-ttu-id="cbb0c-106">您也可以決定要將哪些角色指派給應用程式的元件、介面和方法。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-106">You also decide which roles to assign to the application's components, interfaces, and methods.</span></span> <span data-ttu-id="cbb0c-107">在應用程式整合期間，您可以使用 [元件服務] 系統管理工具，將定義的角色加入至應用程式，並將每個角色指派給適當的元件、介面和方法。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-107">During application integration, you use the Component Services administrative tool to add the defined roles to the application and assign each role to the appropriate components, interfaces, and methods.</span></span>

<span data-ttu-id="cbb0c-108">在設定以角色為基礎的安全性時，您會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="cbb0c-108">In configuring role-based security, you perform the following steps:</span></span>

1.  <span data-ttu-id="cbb0c-109">在應用層級啟用存取檢查。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-109">Enable access checks at the application level.</span></span> <span data-ttu-id="cbb0c-110">開啟應用程式的安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-110">To turn on security checking for an application.</span></span> <span data-ttu-id="cbb0c-111">如需如何執行此步驟的詳細資訊，請參閱 [啟用應用程式的存取檢查](enabling-access-checks-for-an-application.md) 。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-111">See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md) for details on how to perform this step.</span></span>
2.  <span data-ttu-id="cbb0c-112">設定存取檢查的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-112">Set security level for access checks.</span></span> <span data-ttu-id="cbb0c-113">在進程或進程和元件層級設定安全性。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-113">To set security either at process or at process and component level.</span></span> <span data-ttu-id="cbb0c-114">如需如何執行此步驟的詳細資訊，請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md) 。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md) for details on how to perform this step.</span></span>
3.  <span data-ttu-id="cbb0c-115">在元件層級啟用存取檢查。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-115">Enable access checks at the component level.</span></span> <span data-ttu-id="cbb0c-116">開啟元件、介面和方法層級的安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-116">To turn on security checking at the component, interface, and method levels.</span></span> <span data-ttu-id="cbb0c-117">如需如何執行此步驟的詳細資訊，請參閱在 [元件層級啟用存取檢查](enabling-access-checks-at-the-component-level.md) 。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-117">See [Enabling Access Checks at the Component Level](enabling-access-checks-at-the-component-level.md) for details on how to perform this step.</span></span>
4.  <span data-ttu-id="cbb0c-118">定義應用程式的角色。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-118">Define roles for an application.</span></span> <span data-ttu-id="cbb0c-119">建立應用程式的角色。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-119">To create roles for an application.</span></span> <span data-ttu-id="cbb0c-120">如需如何執行此步驟的詳細資訊，請參閱 [定義應用程式的角色](defining-roles-for-an-application.md) 。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-120">See [Defining Roles for an Application](defining-roles-for-an-application.md) for details on how to perform this step.</span></span>
5.  <span data-ttu-id="cbb0c-121">將角色指派給元件、介面或方法。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-121">Assign roles to components, interfaces, or methods.</span></span> <span data-ttu-id="cbb0c-122">將角色指派給應用程式內的特定資源。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-122">To assign roles to specific resources within an application.</span></span> <span data-ttu-id="cbb0c-123">如需如何執行此步驟的詳細資訊，請參閱 [將角色指派給元件、介面或方法](assigning-roles-to-components--interfaces--or-methods.md) 。</span><span class="sxs-lookup"><span data-stu-id="cbb0c-123">See [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md) for details on how to perform this step.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbb0c-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbb0c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbb0c-125">設定軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="cbb0c-125">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="cbb0c-126">設定模擬等級</span><span class="sxs-lookup"><span data-stu-id="cbb0c-126">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



