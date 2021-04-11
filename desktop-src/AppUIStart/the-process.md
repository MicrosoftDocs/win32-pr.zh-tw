---
title: UI 開發總覽
description: 本節將概述使用者介面設計的三個階段，並介紹通常與每個階段相關聯的工作。
ms.assetid: ab544cb9-eed3-4575-a8dd-2f5d7b5c575f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b531fb07a1805c14441c81777bbdddad0739e7cb
ms.sourcegitcommit: e5c43274e96cb8fd1b60fc187ef16723e9258367
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/17/2020
ms.locfileid: "104022957"
---
# <a name="overview-of-the-user-interface-development-process"></a><span data-ttu-id="83dda-103">消費者介面開發流程的總覽</span><span class="sxs-lookup"><span data-stu-id="83dda-103">Overview of the User Interface Development Process</span></span>

<span data-ttu-id="83dda-104">本節將概述使用者介面設計的三個階段，並介紹通常與每個階段相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="83dda-104">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span>

## <a name="the-application-user-interface-and-the-user-experience"></a><span data-ttu-id="83dda-105">應用程式消費者介面和使用者體驗</span><span class="sxs-lookup"><span data-stu-id="83dda-105">The Application User Interface and the User Experience</span></span>

<span data-ttu-id="83dda-106">首先，「使用者介面」和「使用者經驗」等詞彙都必須明確闡明。</span><span class="sxs-lookup"><span data-stu-id="83dda-106">To begin, the terms "user interface" and "user experience" must be clarified.</span></span>

<span data-ttu-id="83dda-107">應用程式的使用者介面通常牽涉到使用者在螢幕上直接看到並與之互動的物件。</span><span class="sxs-lookup"><span data-stu-id="83dda-107">The user interface of an application typically involves those objects that a user sees and interacts with directly on their screen.</span></span> <span data-ttu-id="83dda-108">例如，這類物件包含檔空間、功能表、對話方塊、圖示、影像和動畫。</span><span class="sxs-lookup"><span data-stu-id="83dda-108">For example, such objects include the document space, menus, dialog boxes, icons, images, and animations.</span></span>

<span data-ttu-id="83dda-109">但是，應用程式的使用者介面只是整體使用者體驗的一種層面。</span><span class="sxs-lookup"><span data-stu-id="83dda-109">However, the user interface of an application is only one aspect of the overall user experience.</span></span> <span data-ttu-id="83dda-110">使用者體驗的其他方面，使用者看不到，但對於應用程式而言是不可或缺的，且對其可用性而言是不可或缺的，包括啟動時間、延遲、錯誤處理，以及在不需要直接使用者互動的情況下完成自動化工作。</span><span class="sxs-lookup"><span data-stu-id="83dda-110">Other aspects of the user experience that are not visible to the user, but are integral to an application and critical to its usability, include start up time, latency, error handling, and automated tasks that are completed without direct user interaction.</span></span>

<span data-ttu-id="83dda-111">一般情況下，使用者介面需要使用者採取動作來完成工作，而不需要使用者介面即可達到絕佳的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="83dda-111">In general, a user interface requires action by a user to accomplish a task, while a great user experience can be achieved with no user interface at all.</span></span>

## <a name="user-interface-development"></a><span data-ttu-id="83dda-112">消費者介面開發</span><span class="sxs-lookup"><span data-stu-id="83dda-112">User Interface Development</span></span>

<span data-ttu-id="83dda-113">在整個開發生命週期中，提供成功的使用者體驗需要平衡的方法。</span><span class="sxs-lookup"><span data-stu-id="83dda-113">Providing a successful user experience requires a balanced approach throughout the development life cycle.</span></span> <span data-ttu-id="83dda-114">為了確保這種平衡，您不僅必須專注于執行完成工作所需的功能，還必須瞭解如何透過使用者介面來公開工作。</span><span class="sxs-lookup"><span data-stu-id="83dda-114">To ensure this balance, you must not only focus on implementing the functionality required to complete a task but also on how the task is exposed through the user interface.</span></span> <span data-ttu-id="83dda-115">請記住，使用者介面不僅必須正常運作，也必須可供使用。</span><span class="sxs-lookup"><span data-stu-id="83dda-115">Remember, the user interface must not only be functional, it must also be usable.</span></span>

<span data-ttu-id="83dda-116">以下列出使用者介面 dvelopment 流程的一般階段：</span><span class="sxs-lookup"><span data-stu-id="83dda-116">The following outlines the typical phases of the user interface dvelopment process:</span></span>

### <a name="designing"></a><span data-ttu-id="83dda-117">設計</span><span class="sxs-lookup"><span data-stu-id="83dda-117">Designing</span></span>

-   <span data-ttu-id="83dda-118">功能性需求–決定應用程式的初始需求和目標。</span><span class="sxs-lookup"><span data-stu-id="83dda-118">Functional requirements – Determine the initial requirements and goals for the application.</span></span>
-   <span data-ttu-id="83dda-119">使用者分析–識別使用者案例，並瞭解每個案例的使用者需求和期望。</span><span class="sxs-lookup"><span data-stu-id="83dda-119">User analysis – Identify the user scenarios and understand the needs and expectations of users for each scenario.</span></span>
-   <span data-ttu-id="83dda-120">概念設計-建立應用程式必須支援的基礎商務模型。</span><span class="sxs-lookup"><span data-stu-id="83dda-120">Conceptual design – Model the underlying business that the application must support.</span></span>
-   <span data-ttu-id="83dda-121">邏輯設計-設計應用程式的流程和資訊流程。</span><span class="sxs-lookup"><span data-stu-id="83dda-121">Logical design – Design the process and information flow of the application.</span></span>
-   <span data-ttu-id="83dda-122">實體設計-決定在特定實體平臺上如何實行邏輯設計。</span><span class="sxs-lookup"><span data-stu-id="83dda-122">Physical design – Decide how the logical design will be implemented on specific physical platforms.</span></span>

### <a name="implementing"></a><span data-ttu-id="83dda-123">實作</span><span class="sxs-lookup"><span data-stu-id="83dda-123">Implementing</span></span>

-   <span data-ttu-id="83dda-124">原型-開發著重在介面上的紙張或互動式螢幕原型，而不包含對視覺設計項目的干擾。</span><span class="sxs-lookup"><span data-stu-id="83dda-124">Prototype – Develop paper or interactive screen mockups that focus on the interface and don't include distracting visual design elements.</span></span>
-   <span data-ttu-id="83dda-125">結構-建立應用程式並準備設計變更要求。</span><span class="sxs-lookup"><span data-stu-id="83dda-125">Construct – Build the application and prepare for design change requests.</span></span>

### <a name="testing"></a><span data-ttu-id="83dda-126">測試</span><span class="sxs-lookup"><span data-stu-id="83dda-126">Testing</span></span>

-   <span data-ttu-id="83dda-127">可用性測試–使用各種使用者和案例來測試應用程式。</span><span class="sxs-lookup"><span data-stu-id="83dda-127">Usability testing – Test the application with various users and scenarios.</span></span>
-   <span data-ttu-id="83dda-128">輔助功能測試–使用可存取的技術和自動化測試控管來測試應用程式。</span><span class="sxs-lookup"><span data-stu-id="83dda-128">Accessibility testing – Test the application with accessible technologies and automated test tools.</span></span>

 

 




