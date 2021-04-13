---
description: 開發 COM + 應用程式時，主要工作包括設計 COM 元件來封裝應用程式邏輯，並將這些元件整合至 COM + 應用程式中、建立 COM + 應用程式，以及透過部署和維護來管理應用程式。
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: 開發 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510472"
---
# <a name="developing-com-applications"></a><span data-ttu-id="9959c-103">開發 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="9959c-103">Developing COM+ Applications</span></span>

<span data-ttu-id="9959c-104">開發 COM + 應用程式時，主要工作包括設計 COM 元件來封裝應用程式邏輯，並將這些元件整合至 COM + 應用程式中、建立 COM + 應用程式，以及透過部署和維護來管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="9959c-104">When developing COM+ applications, the principal tasks include designing COM components to encapsulate application logic and integrating these components into a COM+ application, creating the COM+ application, and administering the application through deployment and maintenance.</span></span>

## <a name="designing-com-components"></a><span data-ttu-id="9959c-105">設計 COM 元件</span><span class="sxs-lookup"><span data-stu-id="9959c-105">Designing COM Components</span></span>

<span data-ttu-id="9959c-106">下列步驟描述良好元件設計的一般程式：</span><span class="sxs-lookup"><span data-stu-id="9959c-106">The following steps describe a general procedure for good component design:</span></span>

1.  <span data-ttu-id="9959c-107">定義 COM 類別和實類別。</span><span class="sxs-lookup"><span data-stu-id="9959c-107">Define the COM classes and implementation classes.</span></span>
2.  <span data-ttu-id="9959c-108">將類別群組為元件。</span><span class="sxs-lookup"><span data-stu-id="9959c-108">Group the classes into components.</span></span>
3.  <span data-ttu-id="9959c-109">針對您的元件選取 COM + 服務集合，即使您未在開發元件時指定所有服務。</span><span class="sxs-lookup"><span data-stu-id="9959c-109">Select the set of COM+ services for your component, even if you do not specify all of them when developing the component.</span></span> <span data-ttu-id="9959c-110">您稍後可以使用 [元件服務] 系統管理工具或 COM + 系統管理物件模型來指定這些服務 (如需 COM + 系統管理物件模型的詳細資訊，請參閱 [自動化 COM + 管理](automating-com--administration.md) 。 ) </span><span class="sxs-lookup"><span data-stu-id="9959c-110">These services can later be specified using the Component Services administrative tool or the COM+ administration object model (See [Automating COM+ Administration](automating-com--administration.md) for more information about the COM+ administration object model.)</span></span>

## <a name="creating-the-com-application"></a><span data-ttu-id="9959c-111">建立 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="9959c-111">Creating the COM+ Application</span></span>

<span data-ttu-id="9959c-112">設計 COM 元件之後，開發人員會將元件整合至 COM + 應用程式，並設定應用程式。</span><span class="sxs-lookup"><span data-stu-id="9959c-112">After designing the COM components, the developer integrates the components into a COM+ application and configures the application.</span></span> <span data-ttu-id="9959c-113">下列步驟說明此程序：</span><span class="sxs-lookup"><span data-stu-id="9959c-113">The following steps describe the process:</span></span>

1.  <span data-ttu-id="9959c-114">將元件整合至 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9959c-114">Integrate the components into a COM+ application.</span></span> <span data-ttu-id="9959c-115">您可以將元件整合至現有的 COM + 應用程式，或為元件建立新的 (空白) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9959c-115">You can integrate the components into an existing COM+ application or create a new (empty) application for the components.</span></span> <span data-ttu-id="9959c-116"> (參閱 [建立 COM + 應用程式](creating-com--applications.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="9959c-116">(See [Creating COM+ Applications](creating-com--applications.md).)</span></span>
2.  <span data-ttu-id="9959c-117">針對每個類別 (指定一組正確的屬性（如果有的話），如果未在開發工具) 中指定，則為。</span><span class="sxs-lookup"><span data-stu-id="9959c-117">Specify the correct set of attributes for each of the classes (if any, and if not specified in the development tool).</span></span> <span data-ttu-id="9959c-118">這些屬性 (會表達任何 COM + 服務的元件相依性，例如，交易、佇列元件、安全性、物件共用和及時啟用) 。</span><span class="sxs-lookup"><span data-stu-id="9959c-118">These attributes express the components dependencies on any COM+ services its implementation might rely on (for example, transactions, Queued Components, Security, Object Pooling, and Just-in-Time Activation).</span></span>
3.  <span data-ttu-id="9959c-119">將安全性架構 (角色和角色指派指派給) 的類別、介面和方法。</span><span class="sxs-lookup"><span data-stu-id="9959c-119">Set up the security framework (roles and assignment of roles to classes, interfaces, and methods).</span></span>
4.  <span data-ttu-id="9959c-120">在類別和應用程式上設定環境特定屬性 (預設物件集區大小，例如) 。</span><span class="sxs-lookup"><span data-stu-id="9959c-120">Configure environment-specific attributes on classes and applications (the default object pool size, for example).</span></span> <span data-ttu-id="9959c-121">這些環境特定屬性之後可以 (或修改) 由系統管理員設定。</span><span class="sxs-lookup"><span data-stu-id="9959c-121">These environment-specific attributes can later be set (or modified) by the system administrator.</span></span>
5.  <span data-ttu-id="9959c-122">匯出應用程式以轉散發和部署。</span><span class="sxs-lookup"><span data-stu-id="9959c-122">Export the application for redistribution and deployment.</span></span>

<span data-ttu-id="9959c-123">如需設計分散式應用程式之步驟的詳細資訊，請參閱 [設計 COM + 應用程式](designing-com--applications.md)。</span><span class="sxs-lookup"><span data-stu-id="9959c-123">For more detailed information on the steps in designing distributed applications, see [Designing COM+ Applications](designing-com--applications.md).</span></span>

## <a name="administering-com-applications"></a><span data-ttu-id="9959c-124">管理 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="9959c-124">Administering COM+ Applications</span></span>

<span data-ttu-id="9959c-125">一般來說，開發人員會將部分設定的 COM + 應用程式提供給系統管理員。</span><span class="sxs-lookup"><span data-stu-id="9959c-125">Typically, a developer delivers a partially configured COM+ application to the system administrator.</span></span> <span data-ttu-id="9959c-126">然後系統管理員可以自訂一個或多個特定環境的應用程式 (例如，將使用者帳戶新增至應用程式叢集中的角色和伺服器名稱) 。</span><span class="sxs-lookup"><span data-stu-id="9959c-126">The administrator can then customize the application for one or more specific environments (for example, by adding user accounts in roles and server names in an application cluster).</span></span> <span data-ttu-id="9959c-127">系統管理員的工作包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="9959c-127">The administrator's tasks include the following:</span></span>

-   <span data-ttu-id="9959c-128">在系統管理電腦上安裝部分設定的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9959c-128">Installing the partially configured COM+ application on an administrative computer.</span></span>
-   <span data-ttu-id="9959c-129">提供環境特定的屬性，例如角色成員和物件集區大小。</span><span class="sxs-lookup"><span data-stu-id="9959c-129">Providing environment-specific attributes, such as role members and object pool size.</span></span>
-   <span data-ttu-id="9959c-130">重新匯出完整設定的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9959c-130">Re-exporting the fully configured COM+ application.</span></span>
-   <span data-ttu-id="9959c-131">建立應用程式 proxy (如果要從遠端存取應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="9959c-131">Creating an application proxy (if the application is to be accessed remotely).</span></span>

<span data-ttu-id="9959c-132">針對特定環境完整設定應用程式之後，系統管理員就可以將它部署在測試或實際執行機器上。</span><span class="sxs-lookup"><span data-stu-id="9959c-132">After an application is fully configured for a specific environment, the administrator can then deploy it on test or production machines.</span></span> <span data-ttu-id="9959c-133">這牽涉到在一或多部電腦上安裝完整設定的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9959c-133">This involves installing the fully configured COM+ application on one or more computers.</span></span>

<span data-ttu-id="9959c-134">如需 COM + 系統管理程式的詳細資訊，請參閱「元件服務」系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="9959c-134">For detailed information on COM+ administration procedures, see the Component Services administrative tool.</span></span>

 

 



