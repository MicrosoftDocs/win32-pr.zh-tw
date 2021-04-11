---
description: COM + 磁碟分割是一種邏輯容器，可讓應用程式獨立于這些應用程式的其他設定以外執行。
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: 什麼是 COM + 磁碟分割？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104116009"
---
# <a name="what-are-com-partitions"></a><span data-ttu-id="33c9c-103">什麼是 COM + 磁碟分割？</span><span class="sxs-lookup"><span data-stu-id="33c9c-103">What Are COM+ Partitions?</span></span>

<span data-ttu-id="33c9c-104">COM + 磁碟分割是一種邏輯容器，可讓應用程式獨立于這些應用程式的其他設定以外執行。</span><span class="sxs-lookup"><span data-stu-id="33c9c-104">A COM+ partition is a logical container that allows applications to run independently of other configurations of those applications.</span></span> <span data-ttu-id="33c9c-105">應用程式的每個設定都會安裝到個別的磁碟分割，而且可以根據其使用者的特定需求來個別管理。</span><span class="sxs-lookup"><span data-stu-id="33c9c-105">Each configuration of an application is installed into a separate partition and can be separately managed, according to the specific needs of its users.</span></span>

<span data-ttu-id="33c9c-106">在 COM + 元件啟用期間，資料分割服務會根據要求元件啟用的使用者身分識別，判斷要啟用的元件設定。</span><span class="sxs-lookup"><span data-stu-id="33c9c-106">During activation of a COM+ component, the partitions service determines which configuration of the component to activate, based on the identity of the user requesting the component activation.</span></span> <span data-ttu-id="33c9c-107">例如，有兩個不同群組、生產和定型的單一組織可以實作為 COM + 分割，以允許這兩個群組在同一部電腦上使用不同的 COM + 應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="33c9c-107">For example, a single organization that has two separate groups, Production and Training, could implement COM+ partitions as a way to allow the two groups to use different configurations of a COM+ application on the same computer.</span></span>

<span data-ttu-id="33c9c-108">**WINDOWS XP：** 無法使用建立、設定或委派 COM + 分割的能力。</span><span class="sxs-lookup"><span data-stu-id="33c9c-108">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="33c9c-109">全域分割區是唯一可用的 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="33c9c-109">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="33c9c-110">**Windows 2000：** COM + 分割服務無法在 Windows 2000 中使用。</span><span class="sxs-lookup"><span data-stu-id="33c9c-110">**Windows 2000:** The COM+ partitions service is not available in Windows 2000.</span></span>

## <a name="benefits-of-using-com-partitions"></a><span data-ttu-id="33c9c-111">使用 COM + 磁碟分割的優點</span><span class="sxs-lookup"><span data-stu-id="33c9c-111">Benefits of Using COM+ Partitions</span></span>

<span data-ttu-id="33c9c-112">使用 COM + 分割可提供數個優點，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="33c9c-112">The use of COM+ partitions offers several advantages, including the following:</span></span>

-   <span data-ttu-id="33c9c-113">組織可以使用較少的實體應用程式伺服器來支援需要多個應用程式設定的使用者，以降低其擁有權總成本 (TCO) 。</span><span class="sxs-lookup"><span data-stu-id="33c9c-113">Organizations can lower their total cost of ownership (TCO) by using fewer physical application servers to support users who need multiple application configurations.</span></span>
-   <span data-ttu-id="33c9c-114">系統管理額外負荷會降低。</span><span class="sxs-lookup"><span data-stu-id="33c9c-114">Administrative overhead is reduced.</span></span> <span data-ttu-id="33c9c-115">系統管理員不需要設定及管理多部電腦，而只需要在同一部電腦上設定和管理多個磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="33c9c-115">Instead of having to configure and manage multiple computers, administrators need only configure and manage multiple partitions on the same computer.</span></span> <span data-ttu-id="33c9c-116">此外，您也可以透過加入新的 COM + 程式設計介面，以程式設計方式管理分割區。</span><span class="sxs-lookup"><span data-stu-id="33c9c-116">Furthermore, partitions can be managed programmatically through the addition of a new COM+ programming interface.</span></span>
-   <span data-ttu-id="33c9c-117">您可以針對本機使用者、網域使用者和組織單位，以分割區為基礎來執行和管理安全性， (Ou) 。</span><span class="sxs-lookup"><span data-stu-id="33c9c-117">Security can be implemented and managed on a partition-by-partition basis for local users, domain users, and organizational units (OUs).</span></span>
-   <span data-ttu-id="33c9c-118">程式設計人員和系統管理員可以使用 Microsoft 的開發和系統管理工具（例如 Windows SDK、Active Directory 消費者和電腦和元件服務系統管理工具）來管理 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="33c9c-118">Programmers and administrators can use Microsoft's development and administrative tools—such as the Windows SDK, Active Directory Users and Computers, and Component Services administrative tool—to manage COM+ partitions.</span></span> <span data-ttu-id="33c9c-119">分割區功能完全整合到這些工具中。</span><span class="sxs-lookup"><span data-stu-id="33c9c-119">The partitions feature is fully integrated into these tools.</span></span>

## <a name="primary-usage-scenario"></a><span data-ttu-id="33c9c-120">主要使用案例</span><span class="sxs-lookup"><span data-stu-id="33c9c-120">Primary Usage Scenario</span></span>

<span data-ttu-id="33c9c-121">客戶部署 COM + 分割功能的主要原因是裝載 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="33c9c-121">A primary reason for customers to deploy the COM+ partitions feature is to host Web-based applications.</span></span> <span data-ttu-id="33c9c-122">例如，假設小型軟體公司開發了一個可供醫院人員使用的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="33c9c-122">For example, suppose a small software company develops a COM+ application for use by hospital personnel.</span></span> <span data-ttu-id="33c9c-123">此應用程式是一種分散式 Web 應用程式，可讓醫院使用 SQL Server 資料庫來儲存及取出患者醫療記錄。</span><span class="sxs-lookup"><span data-stu-id="33c9c-123">The application, which is a distributed Web-based application, provides a way for hospitals to store and retrieve patient medical records using a SQL Server database.</span></span>

<span data-ttu-id="33c9c-124">假設軟體公司有三個客戶：醫院 A、醫院 B 和醫院 C。雖然每個客戶都會在其桌上型電腦上本機執行 COM + 應用程式的用戶端，但 COM + 應用程式的伺服器端是位於軟體公司的內部網頁伺服器上，並由其客戶透過 Web 來存取。</span><span class="sxs-lookup"><span data-stu-id="33c9c-124">Suppose the software company has three customers: Hospital A, Hospital B, and Hospital C. While each customer runs the client side of the COM+ application locally on its desktop computers, the server side of the COM+ application resides on the software company's in-house web server and is accessed by its customers via the Web.</span></span>

<span data-ttu-id="33c9c-125">由於每個醫院都有自己的一組儲存和抓取需求，以及自己的自訂患者資料集，因此軟體公司必須提供一種方式，讓應用程式的多個伺服器部分設定在 web 伺服器上同時執行。</span><span class="sxs-lookup"><span data-stu-id="33c9c-125">Because each hospital has its own set of storage and retrieval requirements and its own set of customized patient data, the software company must provide a way for multiple configurations of the server part of the application to be executed simultaneously on the web server.</span></span> <span data-ttu-id="33c9c-126">COM + 分割可提供此問題的解決方案。</span><span class="sxs-lookup"><span data-stu-id="33c9c-126">COM+ partitions provide a solution to this problem.</span></span>

<span data-ttu-id="33c9c-127">下圖顯示軟體公司的 COM + 應用程式的磁碟分割案例。</span><span class="sxs-lookup"><span data-stu-id="33c9c-127">The following illustration shows the partitions scenario for the software company's COM+ application.</span></span>

![顯示 COM + 應用程式之資料分割案例的圖表，其中包含用戶端應用程式至 SQL server 資料庫的伺服器應用程式。](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a><span data-ttu-id="33c9c-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="33c9c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33c9c-130">應用程式設計限制</span><span class="sxs-lookup"><span data-stu-id="33c9c-130">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="33c9c-131">COM + 佇列元件和分割區</span><span class="sxs-lookup"><span data-stu-id="33c9c-131">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="33c9c-132">分割區執行</span><span class="sxs-lookup"><span data-stu-id="33c9c-132">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="33c9c-133">在分割區中註冊和啟用元件</span><span class="sxs-lookup"><span data-stu-id="33c9c-133">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



