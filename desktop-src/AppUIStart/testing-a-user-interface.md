---
title: 測試消費者介面
description: 本節詳細說明一些與測試 Windows 應用程式的 UI 相關聯的工作。
ms.assetid: d628e530-7a0b-4a8d-9a9f-253aec275fa9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e86282c03502642541c0ea1318b8ccaf6d16b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933529"
---
# <a name="testing-a-user-interface"></a><span data-ttu-id="5de9a-103">測試消費者介面</span><span class="sxs-lookup"><span data-stu-id="5de9a-103">Testing a User Interface</span></span>

<span data-ttu-id="5de9a-104">本節詳細說明一些與測試 Windows 應用程式的 UI 相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="5de9a-104">This section describes in detail some of the tasks associated with testing a UI for a Windows application.</span></span>

-   [<span data-ttu-id="5de9a-105">簡介</span><span class="sxs-lookup"><span data-stu-id="5de9a-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="5de9a-106">可用性測試</span><span class="sxs-lookup"><span data-stu-id="5de9a-106">Usability Testing</span></span>](#usability-testing)
-   [<span data-ttu-id="5de9a-107">輔助功能測試</span><span class="sxs-lookup"><span data-stu-id="5de9a-107">Accessibility Testing</span></span>](#accessibility-testing)

## <a name="introduction"></a><span data-ttu-id="5de9a-108">簡介</span><span class="sxs-lookup"><span data-stu-id="5de9a-108">Introduction</span></span>

<span data-ttu-id="5de9a-109">若要完整判斷應用程式 UI 的有效性和整體可用性，必須進行測試。</span><span class="sxs-lookup"><span data-stu-id="5de9a-109">To fully determine the effectiveness and overall usability of an application UI, it must be tested.</span></span> <span data-ttu-id="5de9a-110">測試會公開 UI 在最廣泛的可能物件上使用的簡單或困難之處。</span><span class="sxs-lookup"><span data-stu-id="5de9a-110">Testing exposes how easy or difficult the UI is to use for the broadest possible audience.</span></span> <span data-ttu-id="5de9a-111">測試應用程式所需的時間很值得。</span><span class="sxs-lookup"><span data-stu-id="5de9a-111">The time that it takes to test an application is well worth it.</span></span>

<span data-ttu-id="5de9a-112">本主題著重于三個主要的測試案例：一般可用性、協助工具和自動化。</span><span class="sxs-lookup"><span data-stu-id="5de9a-112">This topic focuses on three primary testing scenarios: general usability, accessibility, and automation.</span></span>

## <a name="usability-testing"></a><span data-ttu-id="5de9a-113">可用性測試</span><span class="sxs-lookup"><span data-stu-id="5de9a-113">Usability Testing</span></span>

<span data-ttu-id="5de9a-114">可用性測試可讓您藉由研究真實使用者實際使用產品的方式，來評估產品。</span><span class="sxs-lookup"><span data-stu-id="5de9a-114">Usability testing provides the opportunity to evaluate a product by studying how real users actually use the product.</span></span> <span data-ttu-id="5de9a-115">這項分析可確保 (或面對實際資料的) ，支援預期的使用者和介面設計相關的重要假設。</span><span class="sxs-lookup"><span data-stu-id="5de9a-115">This analysis ensures that key assumptions about intended users and interface designs are supported (or challenged) with real data.</span></span> <span data-ttu-id="5de9a-116">只有藉由收集這項經驗資料，您才能找出產品的 UI 符合您使用者的需求和期望的程度。</span><span class="sxs-lookup"><span data-stu-id="5de9a-116">Only by gathering this empirical data can you find out how well the UI for a product fits your users' needs and expectations.</span></span>

<span data-ttu-id="5de9a-117">藉由觀察使用者與產品的互動並聆聽使用者意見反應，將會識別出可能難以尋找和使用的重要功能。</span><span class="sxs-lookup"><span data-stu-id="5de9a-117">By observing user interaction with the product and listening to user feedback, important features that may be difficult to find and use are identified.</span></span> <span data-ttu-id="5de9a-118">根據這些結果，您可以視需要對 UI 進行調整。</span><span class="sxs-lookup"><span data-stu-id="5de9a-118">Based on these results, adjustments can be made to the UI as required.</span></span> <span data-ttu-id="5de9a-119">您幾乎無法在沒有一些可用性測試的情況下建立有用的產品，因為結果會提供對產品做出更佳決策的基礎，並提升整體使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="5de9a-119">It is almost impossible to build a useful product without some level of usability testing as the results provide the basis for making better decisions about the product and improving the overall user experience.</span></span>

<span data-ttu-id="5de9a-120">可用性測試只在整合至整個專案生命週期時，才提供大幅的投資。</span><span class="sxs-lookup"><span data-stu-id="5de9a-120">Usability testing provides significant payback only when it is well integrated into the entire project lifecycle.</span></span> <span data-ttu-id="5de9a-121">單一可用性研究可以找出問題，但如果沒有後續的測試，就很難判斷解決方案是否已解決這些問題或引進新的問題。</span><span class="sxs-lookup"><span data-stu-id="5de9a-121">A single usability study can identify issues, but without follow-up tests it is difficult to determine if the solutions have solved those problems or introduced new ones.</span></span>

<span data-ttu-id="5de9a-122">可用性測試的主要案例包括：</span><span class="sxs-lookup"><span data-stu-id="5de9a-122">The primary scenarios for usability testing are:</span></span>

-   <span data-ttu-id="5de9a-123">如果您是軟體產品廠商，測試產品的真實使用者表示您正在評估設計。</span><span class="sxs-lookup"><span data-stu-id="5de9a-123">If you are a software product vendor, testing real users of your product means you are evaluating the design.</span></span> <span data-ttu-id="5de9a-124">根據您設計應用程式的方式，使用者可以完成他們需要執行的工作嗎？</span><span class="sxs-lookup"><span data-stu-id="5de9a-124">Based on how you have designed the application, can users complete the tasks they need to do?</span></span> <span data-ttu-id="5de9a-125">測試實際執行工作的使用者，也可以指出您所關注的 UI 指導方針是否正在您的產品內容中運作，以及一致性是否有助於或阻礙使用者執行其工作的能力。</span><span class="sxs-lookup"><span data-stu-id="5de9a-125">Testing real users doing real tasks can also point out if the UI guidelines you are following are working within the context of your product, and when consistency helps or hinders the ability of a user to do their work.</span></span>
-   <span data-ttu-id="5de9a-126">如果您是軟體產品採購商，您可以進行「可用性測試」以評估要購買的產品。</span><span class="sxs-lookup"><span data-stu-id="5de9a-126">If you are a software product purchaser, you can do usability testing to evaluate a product for purchase.</span></span> <span data-ttu-id="5de9a-127">例如，您的公司可能會考慮為其20000員工購買產品。</span><span class="sxs-lookup"><span data-stu-id="5de9a-127">For example, your company might consider buying a product for their twenty thousand employees.</span></span> <span data-ttu-id="5de9a-128">在公司花費錢之前，它想要確定有問題的產品真的可協助員工更妥善地執行工作。</span><span class="sxs-lookup"><span data-stu-id="5de9a-128">Before the company spends its money, it wants to make sure that the product in question will really help employees do their jobs better.</span></span> <span data-ttu-id="5de9a-129">可用性測試也有助於查看建議的應用程式是否遵循發佈的 UI 樣式指導方針 (內部或外部) 。</span><span class="sxs-lookup"><span data-stu-id="5de9a-129">Usability testing can also be useful to see if the proposed application follows published UI style guidelines (internal or external).</span></span> <span data-ttu-id="5de9a-130">最好使用 UI 指導方針作為輔助，而不是主要的資訊來源，以進行購買決策。</span><span class="sxs-lookup"><span data-stu-id="5de9a-130">It's best to use UI guidelines as an auxiliary, rather than primary, source of information for making purchase decisions.</span></span>

<span data-ttu-id="5de9a-131">如需詳細資訊，請參閱 [可用性實務：可用性測試](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing)。</span><span class="sxs-lookup"><span data-stu-id="5de9a-131">For more information, see [Usability in Practice: Usability Testing](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing).</span></span>

## <a name="accessibility-testing"></a><span data-ttu-id="5de9a-132">輔助功能測試</span><span class="sxs-lookup"><span data-stu-id="5de9a-132">Accessibility Testing</span></span>

<span data-ttu-id="5de9a-133">輔助功能測試包含兩個 UI 設計區域：支援殘障使用者，以及自動化測試架構的程式設計存取。</span><span class="sxs-lookup"><span data-stu-id="5de9a-133">Accessibility testing encompasses two areas of a UI design: support for users with disabilities and programmatic access by automated test frameworks.</span></span>

<span data-ttu-id="5de9a-134">確保應用程式可供殘障使用者存取，牽涉到測試：</span><span class="sxs-lookup"><span data-stu-id="5de9a-134">Ensuring that an application is accessible to users with disabilities involves testing for:</span></span>

-   <span data-ttu-id="5de9a-135">合規性-應用程式是否符合有關協助工具的各種法律需求？</span><span class="sxs-lookup"><span data-stu-id="5de9a-135">Compliance - Does the application comply with various legal requirements regarding accessibility?</span></span>
-   <span data-ttu-id="5de9a-136">效能-殘障使用者是否可以使用應用程式？</span><span class="sxs-lookup"><span data-stu-id="5de9a-136">Effectiveness - Can users with disabilities use the application?</span></span>
-   <span data-ttu-id="5de9a-137">實用性-應用程式是否會針對殘障使用者公開適當的功能？</span><span class="sxs-lookup"><span data-stu-id="5de9a-137">Usefulness - Does the application expose adequate functionality for users with disabilities?</span></span>
-   <span data-ttu-id="5de9a-138">滿意度-使用者如何察覺應用程式？</span><span class="sxs-lookup"><span data-stu-id="5de9a-138">Satisfaction - How is the application perceived by users with disabilities?</span></span>

<span data-ttu-id="5de9a-139">測試應用程式的這些層面可透過存取範圍審核來完成，這牽涉到協助工具專家手動審核應用程式，以及已停用使用者和輔助技術裝置的專注可用性研究。</span><span class="sxs-lookup"><span data-stu-id="5de9a-139">Testing for these aspects of an application can be accomplished through an accessibility audit, which involves a manual review of the application by an accessibility expert, and a focused usability study of disabled users and assistive technology devices.</span></span>

<span data-ttu-id="5de9a-140">雖然看似不相關，但是自動化測試架構的程式設計存取需求與輔助技術裝置的程式設計存取需求之間有密切的關聯性。</span><span class="sxs-lookup"><span data-stu-id="5de9a-140">Although seemingly unrelated, there is a close correlation between the programmatic access requirements of automated test frameworks and those of assistive technology devices.</span></span> <span data-ttu-id="5de9a-141">支援另一種是啟用另一項的額外優點。</span><span class="sxs-lookup"><span data-stu-id="5de9a-141">Supporting one has the added benefit of enabling the other.</span></span> <span data-ttu-id="5de9a-142">如需有關 Windows 應用程式中的協助工具和測試自動化的詳細資訊，請參閱 [協助工具](/windows/desktop/accessibility)、 [測試控管](/windows/desktop/WinAuto/testing-tools)和 [windows 自動化 API](/windows/desktop/WinAuto/windows-automation-api-portal)。</span><span class="sxs-lookup"><span data-stu-id="5de9a-142">For more information on accessibility and test automation in Windows applications, see [Accessibility](/windows/desktop/accessibility), [Testing Tools](/windows/desktop/WinAuto/testing-tools), and the [Windows Automation API](/windows/desktop/WinAuto/windows-automation-api-portal).</span></span>

 

 