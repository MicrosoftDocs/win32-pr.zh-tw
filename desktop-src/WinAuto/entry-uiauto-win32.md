---
title: UI 自動化
description: Microsoft 消費者介面自動化是一種協助工具架構，可讓 Windows 應用程式提供使用者介面的程式設計相關資訊， (Ui) 。
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842540"
---
# <a name="ui-automation"></a><span data-ttu-id="5dc7c-103">UI 自動化</span><span class="sxs-lookup"><span data-stu-id="5dc7c-103">UI Automation</span></span>

<span data-ttu-id="5dc7c-104">Microsoft 消費者介面自動化是一種協助工具架構，可讓 Windows 應用程式提供使用者介面的程式設計相關資訊， (Ui) 。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-104">Microsoft UI Automation is an accessibility framework that enables Windows applications to provide and consume programmatic information about user interfaces (UIs).</span></span> <span data-ttu-id="5dc7c-105">它可讓您以程式設計方式存取桌面上大部分的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-105">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="5dc7c-106">它可讓輔助技術產品（例如螢幕讀取器）提供使用者介面的相關資訊給使用者，以及透過標準輸入以外的方式操作 UI。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-106">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="5dc7c-107">消費者介面自動化也可讓自動化測試腳本與 UI 互動。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-107">UI Automation also allows automated test scripts to interact with the UI.</span></span>

-   [<span data-ttu-id="5dc7c-108">適用時</span><span class="sxs-lookup"><span data-stu-id="5dc7c-108">Where Applicable</span></span>](#where-applicable)
-   [<span data-ttu-id="5dc7c-109">開發人員物件</span><span class="sxs-lookup"><span data-stu-id="5dc7c-109">Developer Audience</span></span>](#developer-audience)
-   [<span data-ttu-id="5dc7c-110">執行時間需求</span><span class="sxs-lookup"><span data-stu-id="5dc7c-110">Run-Time Requirements</span></span>](#run-time-requirements)
-   [<span data-ttu-id="5dc7c-111">舊版作業系統的支援</span><span class="sxs-lookup"><span data-stu-id="5dc7c-111">Support for Down-level Operating Systems</span></span>](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a><span data-ttu-id="5dc7c-112">適用情況</span><span class="sxs-lookup"><span data-stu-id="5dc7c-112">Where Applicable</span></span>

<span data-ttu-id="5dc7c-113">藉由使用消費者介面自動化和遵循可存取的設計實務，開發人員可以讓具有視覺、聽力或動作障礙的許多人更容易存取在 Windows 上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-113">By using UI Automation and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span> <span data-ttu-id="5dc7c-114">此外，消費者介面自動化是特別設計來提供適用于自動化測試案例的強大功能。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-114">Also, UI Automation is specifically designed to provide robust functionality for automated testing scenarios.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5dc7c-115">開發人員讀者</span><span class="sxs-lookup"><span data-stu-id="5dc7c-115">Developer Audience</span></span>

<span data-ttu-id="5dc7c-116">消費者介面自動化是專為有經驗的 C/c + + 開發人員所設計。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-116">UI Automation is designed for experienced C/C++ developers.</span></span> <span data-ttu-id="5dc7c-117">一般來說，開發人員需要對元件物件模型進行中等程度的瞭解， (COM) 物件和介面、Unicode 和 Windows API 程式設計。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-117">In general, developers need a moderate level of understanding about Component Object Model (COM) objects and interfaces, Unicode, and Windows API programming.</span></span>

<span data-ttu-id="5dc7c-118">如需受控碼消費者介面自動化的詳細資訊，請參閱 MSDN 上 .NET Framework 開發人員指南》一節中的 [協助工具](/dotnet/framework/ui-automation/) 。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-118">For information about UI Automation for managed code, please see [Accessibility](/dotnet/framework/ui-automation/) in the .NET Framework Developer's Guide section of MSDN.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5dc7c-119">執行階段需求</span><span class="sxs-lookup"><span data-stu-id="5dc7c-119">Run-Time Requirements</span></span>

<span data-ttu-id="5dc7c-120">下列作業系統支援消費者介面自動化： Windows XP、Windows Server 2003、Windows Server 2003 R2、Windows Vista、Windows 7、Windows 10、Windows Server 2008、Windows Server 2008 R2、Windows Server 2012、Windows Server 2012 R2、Windows Server 2016 以及 Windows Server 2019。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-120">UI Automation is supported on the following operating systems: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, and Windows Server 2019.</span></span>

> [!Note]  
> <span data-ttu-id="5dc7c-121">Windows XP 和 Windows Server 2003 也需要 Microsoft .NET Framework 3.0。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-121">Windows XP and Windows Server 2003 also require Microsoft .NET Framework 3.0.</span></span>

 

## <a name="support-for-down-level-operating-systems"></a><span data-ttu-id="5dc7c-122">舊版作業系統的支援</span><span class="sxs-lookup"><span data-stu-id="5dc7c-122">Support for Down-level Operating Systems</span></span>

<span data-ttu-id="5dc7c-123">Windows Vista 的平臺更新是一組執行時間程式庫，可讓開發人員將應用程式的目標設為 Windows 7 和下層作業系統。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-123">The Platform Update for Windows Vista is a set of run-time libraries that enables developers to target applications to both Windows 7 and down-level operating systems.</span></span> <span data-ttu-id="5dc7c-124">Windows Server 2008 的平臺更新是一組執行時間程式庫，可讓開發人員將應用程式的目標設定為 Windows Server 2008 R2 和舊版的 Windows Server。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-124">The Platform Update for Windows Server 2008 is a set of run-time libraries that enables developers to target applications to both Windows Server 2008 R2 and previous versions of Windows Server.</span></span> <span data-ttu-id="5dc7c-125">所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update，取得 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-125">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="5dc7c-126">需要適用于 Windows Vista 或 Windows Server 2008 平臺更新的協力廠商應用程式，可以 Windows Update 偵測是否已安裝;如果不是，Windows Update 會在背景中下載並安裝它。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-126">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether it is installed; if it is not, Windows Update will download and install it in the background.</span></span>

<span data-ttu-id="5dc7c-127">適用于 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新都支援下列作業系統上的整個 Windows Automation API 3.0 功能集。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-127">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 both support the entire Windows Automation API 3.0 feature set on the following operating systems.</span></span>

-   <span data-ttu-id="5dc7c-128">Windows XP (英文) </span><span class="sxs-lookup"><span data-stu-id="5dc7c-128">Windows XP (English)</span></span> <dl> <span data-ttu-id="5dc7c-129">Windows XP Home SP3 x86</span><span class="sxs-lookup"><span data-stu-id="5dc7c-129">Windows XP Home SP3 x86</span></span>  
    <span data-ttu-id="5dc7c-130">Windows XP Professional SP3 x86</span><span class="sxs-lookup"><span data-stu-id="5dc7c-130">Windows XP Professional SP3 x86</span></span>  
    </dl>
-   Windows Server 2003 (English) <dl> <span data-ttu-id="5dc7c-131">Windows Server 2003 SP2 (x86 和 x64) </span><span class="sxs-lookup"><span data-stu-id="5dc7c-131">Windows Server 2003 SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="5dc7c-132">Windows Vista (英文) </span><span class="sxs-lookup"><span data-stu-id="5dc7c-132">Windows Vista (English)</span></span> <dl> <span data-ttu-id="5dc7c-133">Starter SP2 (x86 和 x64) </span><span class="sxs-lookup"><span data-stu-id="5dc7c-133">Starter SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="5dc7c-134">Home Premium SP2 (x86 和 x64) </span><span class="sxs-lookup"><span data-stu-id="5dc7c-134">Home Premium SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="5dc7c-135">Business SP2 (x86 和 x64) </span><span class="sxs-lookup"><span data-stu-id="5dc7c-135">Business SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="5dc7c-136">Enterprise SP2 (x86 和 x64) </span><span class="sxs-lookup"><span data-stu-id="5dc7c-136">Enterprise SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="5dc7c-137">終極 SP2 (x86 和 x64) </span><span class="sxs-lookup"><span data-stu-id="5dc7c-137">Ultimate SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="5dc7c-138">Windows Server 2008 (英文) </span><span class="sxs-lookup"><span data-stu-id="5dc7c-138">Windows Server 2008 (English)</span></span> <dl> <span data-ttu-id="5dc7c-139">Windows Server 2008 SP2 (x86 和 x64)</span><span class="sxs-lookup"><span data-stu-id="5dc7c-139">Windows Server 2008 SP2 (x86 and x64)</span></span>  
    </dl>

<span data-ttu-id="5dc7c-140">如需這兩項更新的詳細資訊，請參閱 [Windows Vista 的平臺更新](../win7ip/platform-update-for-windows-vista-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="5dc7c-140">For more information about both updates, see [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5dc7c-141">本節內容</span><span class="sxs-lookup"><span data-stu-id="5dc7c-141">In this section</span></span>

-   [<span data-ttu-id="5dc7c-142">UI 自動化基礎</span><span class="sxs-lookup"><span data-stu-id="5dc7c-142">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
-   [<span data-ttu-id="5dc7c-143">消費者介面自動化提供者程式設計人員指南</span><span class="sxs-lookup"><span data-stu-id="5dc7c-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
-   [<span data-ttu-id="5dc7c-144">消費者介面自動化用戶端程式設計人員指南</span><span class="sxs-lookup"><span data-stu-id="5dc7c-144">UI Automation Client Programmer's Guide</span></span>](uiauto-clientportal.md)
-   [<span data-ttu-id="5dc7c-145">參考</span><span class="sxs-lookup"><span data-stu-id="5dc7c-145">Reference</span></span>](entry-uiautocore-ref.md)
-   [<span data-ttu-id="5dc7c-146">範例</span><span class="sxs-lookup"><span data-stu-id="5dc7c-146">Samples</span></span>](samples-entry.md)
-   [<span data-ttu-id="5dc7c-147">附錄</span><span class="sxs-lookup"><span data-stu-id="5dc7c-147">Appendixes</span></span>](appendix-entry.md)

 

 