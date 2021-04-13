---
title: 工作註冊資訊
description: 註冊資訊可讓您以數種不同的方式來識別工作。 例如，作者可以識別工作、撰寫工作的方式 (稱為工作來源) 和註冊日期。
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- 註冊資訊工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300032"
---
# <a name="task-registration-information"></a><span data-ttu-id="43b4a-105">工作註冊資訊</span><span class="sxs-lookup"><span data-stu-id="43b4a-105">Task Registration Information</span></span>

<span data-ttu-id="43b4a-106">註冊資訊可讓您以數種不同的方式來識別工作。</span><span class="sxs-lookup"><span data-stu-id="43b4a-106">Registration information provides a way to identify a task in several different ways.</span></span> <span data-ttu-id="43b4a-107">例如，作者可以識別工作、撰寫工作的方式 (稱為工作來源) 和註冊日期。</span><span class="sxs-lookup"><span data-stu-id="43b4a-107">For example, a task can be identified by the author, how it was authored (referred to as the task source), and date of registration.</span></span>

## <a name="using-registration-information"></a><span data-ttu-id="43b4a-108">使用註冊資訊</span><span class="sxs-lookup"><span data-stu-id="43b4a-108">Using Registration Information</span></span>

<span data-ttu-id="43b4a-109">註冊資訊通常會在工作建立時指定，然後以下列方式使用：</span><span class="sxs-lookup"><span data-stu-id="43b4a-109">Registration information is typically specified when the task is created and then used in the following ways:</span></span>

-   <span data-ttu-id="43b4a-110">由工作排程器使用者介面顯示。</span><span class="sxs-lookup"><span data-stu-id="43b4a-110">Displayed by the Task Scheduler user interface.</span></span>
-   <span data-ttu-id="43b4a-111">取得或設定 c + + 應用程式或腳本。</span><span class="sxs-lookup"><span data-stu-id="43b4a-111">Get or set by C++ applications or scripts.</span></span>
-   <span data-ttu-id="43b4a-112">在企業環境中，當列舉所有已註冊的工作時，用來做為搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="43b4a-112">In an enterprise environment, used as a search criteria when enumerating over all registered tasks.</span></span>

## <a name="types-of-registration-information"></a><span data-ttu-id="43b4a-113">註冊資訊的類型</span><span class="sxs-lookup"><span data-stu-id="43b4a-113">Types of Registration Information</span></span>

<span data-ttu-id="43b4a-114">工作註冊資訊是由 [**RegistrationInfo**](registrationinfo.md) 物件的屬性所定義，用於腳本應用程式、c + + 應用程式的 [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) 介面屬性，以及 [**RegistrationInfo (taskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) 專案的子項目，以讀取或寫入 XML。</span><span class="sxs-lookup"><span data-stu-id="43b4a-114">Task registration information is defined by the properties of the [**RegistrationInfo**](registrationinfo.md) object for scripting applications, the properties of the [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) interface for C++ applications, and the child elements of the [**RegistrationInfo (taskType) element**](taskschedulerschema-registrationinfo-tasktype-element.md) for reading or writing XML.</span></span>

<span data-ttu-id="43b4a-115">這些屬性可讓您存取下列類型的註冊資訊：</span><span class="sxs-lookup"><span data-stu-id="43b4a-115">These properties allow access to the following types of registration information:</span></span>

-   <span data-ttu-id="43b4a-116">工作作者</span><span class="sxs-lookup"><span data-stu-id="43b4a-116">Task Author</span></span>

    <span data-ttu-id="43b4a-117">工作排程器設定工作建立時的作者。</span><span class="sxs-lookup"><span data-stu-id="43b4a-117">Task Scheduler sets the author of the task when it is created.</span></span>

-   <span data-ttu-id="43b4a-118">工作註冊日期</span><span class="sxs-lookup"><span data-stu-id="43b4a-118">Task Registration Date</span></span>

    <span data-ttu-id="43b4a-119">工作排程器在工作註冊時設定此日期。</span><span class="sxs-lookup"><span data-stu-id="43b4a-119">Task Scheduler sets this date when the task is registered.</span></span>

-   <span data-ttu-id="43b4a-120">工作描述</span><span class="sxs-lookup"><span data-stu-id="43b4a-120">Task Description</span></span>

    <span data-ttu-id="43b4a-121">使用者定義的描述，其中可能包含用來啟動工作的觸發程式，或工作執行的動作。</span><span class="sxs-lookup"><span data-stu-id="43b4a-121">A user-defined description that may include what triggers are used to start the task or what actions the task performs.</span></span>

-   <span data-ttu-id="43b4a-122">工作檔</span><span class="sxs-lookup"><span data-stu-id="43b4a-122">Task Documentation</span></span>

    <span data-ttu-id="43b4a-123">工作所需的使用者提供檔。</span><span class="sxs-lookup"><span data-stu-id="43b4a-123">User-supplied documentation that is needed by the task.</span></span>

-   <span data-ttu-id="43b4a-124">工作安全描述項</span><span class="sxs-lookup"><span data-stu-id="43b4a-124">Task Security Descriptor</span></span>

    <span data-ttu-id="43b4a-125">使用者提供的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="43b4a-125">A user-supplied security descriptor.</span></span>

-   <span data-ttu-id="43b4a-126">工作來源</span><span class="sxs-lookup"><span data-stu-id="43b4a-126">Task Source</span></span>

    <span data-ttu-id="43b4a-127">描述工作來源的使用者提供資訊。</span><span class="sxs-lookup"><span data-stu-id="43b4a-127">User-supplied information that describes where the task originated from.</span></span> <span data-ttu-id="43b4a-128">例如，工作可能源自元件、服務、應用程式或使用者。</span><span class="sxs-lookup"><span data-stu-id="43b4a-128">For example, a task may originate from a component, service, application, or user.</span></span>

-   <span data-ttu-id="43b4a-129">工作 URI</span><span class="sxs-lookup"><span data-stu-id="43b4a-129">Task URI</span></span>

    <span data-ttu-id="43b4a-130">工作 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="43b4a-130">A uniform resource identifier (URI) for the task.</span></span>

-   <span data-ttu-id="43b4a-131">工作版本</span><span class="sxs-lookup"><span data-stu-id="43b4a-131">Task Version</span></span>

    <span data-ttu-id="43b4a-132">當有多個工作版本存在時所使用的使用者提供資訊。</span><span class="sxs-lookup"><span data-stu-id="43b4a-132">User-supplied information that is used when multiple versions of a task exist.</span></span>

-   <span data-ttu-id="43b4a-133">XML 文字</span><span class="sxs-lookup"><span data-stu-id="43b4a-133">XML Text</span></span>

    <span data-ttu-id="43b4a-134">XML 格式的註冊資訊版本。</span><span class="sxs-lookup"><span data-stu-id="43b4a-134">An XML-formatted version of the registration information.</span></span> <span data-ttu-id="43b4a-135">請注意，您可以直接透過這個 XML 來設定或修改註冊資訊，適當的物件和介面屬性也會隨之更新。</span><span class="sxs-lookup"><span data-stu-id="43b4a-135">Note that you can set or modify the registration information directly through this XML and the appropriate object and interface properties will be updated accordingly.</span></span>

## <a name="registering-tasks"></a><span data-ttu-id="43b4a-136">註冊工作</span><span class="sxs-lookup"><span data-stu-id="43b4a-136">Registering Tasks</span></span>

<span data-ttu-id="43b4a-137">工作可以在建立工作定義之後註冊，而且註冊資訊和設定值是由使用者提供。</span><span class="sxs-lookup"><span data-stu-id="43b4a-137">A task can be registered after the task definitions are created and registration information and setting values are supplied by the user.</span></span> <span data-ttu-id="43b4a-138">使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法來註冊工作，以編寫應用程式的腳本，或使用 [**ITaskFolder：： RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) 方法來進行 c + + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="43b4a-138">A task is registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method for scripting applications or the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method for C++ applications.</span></span> <span data-ttu-id="43b4a-139">如果您想要使用 XML 來定義工作，請使用 [**TaskFolder. RegisterTask**](taskfolder-registertask.md) 方法來編寫應用程式的腳本，並使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 方法來進行 c + + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="43b4a-139">If you want to register a task using XML to define the task, you use the [**TaskFolder.RegisterTask**](taskfolder-registertask.md) method for scripting applications and the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method for C++ applications.</span></span>

<span data-ttu-id="43b4a-140">在上面所述的方法中，您可以指定要執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="43b4a-140">In the methods mentioned above, you can specify the security context to run the task.</span></span> <span data-ttu-id="43b4a-141">您必須是系統管理員，才能將工作排程在非您自己的內容下執行。</span><span class="sxs-lookup"><span data-stu-id="43b4a-141">You have to be an administrator on the system to schedule jobs to run under contexts other than your own.</span></span> <span data-ttu-id="43b4a-142">如需有關執行工作之安全性內容的詳細資訊，請參閱執行工作的 [安全性](security-contexts-for-running-tasks.md)內容。</span><span class="sxs-lookup"><span data-stu-id="43b4a-142">For more information on the security contexts to run tasks, see [Security Contexts for Running Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43b4a-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="43b4a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43b4a-144">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="43b4a-144">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="43b4a-145">工作排程器</span><span class="sxs-lookup"><span data-stu-id="43b4a-145">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




