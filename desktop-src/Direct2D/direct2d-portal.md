---
title: Direct2D
description: .
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2eae62ba2d6ff44920d6b6d4890a8c48bc3c0f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023761"
---
# <a name="direct2d"></a><span data-ttu-id="9412d-103">Direct2D</span><span class="sxs-lookup"><span data-stu-id="9412d-103">Direct2D</span></span>

## <a name="purpose"></a><span data-ttu-id="9412d-104">目的</span><span class="sxs-lookup"><span data-stu-id="9412d-104">Purpose</span></span>

<span data-ttu-id="9412d-105">Direct2D 是一種硬體加速的即時模式 2D 圖形 API，能夠以高效能和高品質來呈現 2D 幾何、點陣圖和文字。</span><span class="sxs-lookup"><span data-stu-id="9412d-105">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="9412d-106">Direct2D API 的設計目的是要與 GDI、GDI + 和 Direct3D 順利互通。</span><span class="sxs-lookup"><span data-stu-id="9412d-106">The Direct2D API is designed to interoperate well with GDI, GDI+, and Direct3D.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9412d-107">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="9412d-107">Developer audience</span></span>

<span data-ttu-id="9412d-108">Direct2D 主要是設計來供下列開發人員類別使用：</span><span class="sxs-lookup"><span data-stu-id="9412d-108">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="9412d-109">大型企業規模原生應用程式的開發人員。</span><span class="sxs-lookup"><span data-stu-id="9412d-109">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="9412d-110">建立可供下游開發人員取用的控制項工具組和程式庫的開發人員。</span><span class="sxs-lookup"><span data-stu-id="9412d-110">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="9412d-111">需要伺服器端呈現2D 圖形的開發人員。</span><span class="sxs-lookup"><span data-stu-id="9412d-111">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="9412d-112">使用 Direct3D 圖形並需要簡單、高效能的2D 和文字轉譯（用於功能表、使用者介面 (UI) 專案），以及顯示 (HUDs) 的開發人員。</span><span class="sxs-lookup"><span data-stu-id="9412d-112">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user-interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9412d-113">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="9412d-113">Run-time requirements</span></span>

-   <span data-ttu-id="9412d-114">Windows 7 或 Windows Vista Service Pack 2 (SP2) 和 Windows Vista 和更新版本的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="9412d-114">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista and later.</span></span>
-   <span data-ttu-id="9412d-115">Windows Server 2008 R2 或 Windows Server 2008 Service Pack 2 (SP2) 和 Windows Server 2008 和更新版本的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="9412d-115">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008 and later.</span></span>

> [!Note]
>
> <span data-ttu-id="9412d-116">Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新是一組執行時間程式庫，可讓開發人員將應用程式的目標設為 Windows 7、Windows Vista、Windows Server 2008 R2 和 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="9412d-116">The Platform Update for Windows Vista and Platform Update for Windows Server 2008 are a set of run-time libraries that enables developers to target applications to Windows 7, Windows Vista, Windows Server 2008 R2, and Windows Server 2008.</span></span> <span data-ttu-id="9412d-117">所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update 取得這些更新。</span><span class="sxs-lookup"><span data-stu-id="9412d-117">These updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="9412d-118">需要適用于 Windows Vista 或 Windows Server 2008 平臺更新的協力廠商應用程式，可以 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。</span><span class="sxs-lookup"><span data-stu-id="9412d-118">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span> <span data-ttu-id="9412d-119">如需這兩項更新的詳細資訊，請參閱 [Windows Vista 的平臺更新](https://support.microsoft.com/kb/971644)。</span><span class="sxs-lookup"><span data-stu-id="9412d-119">For more information about both updates, see [Platform Update for Windows Vista](https://support.microsoft.com/kb/971644).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="9412d-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="9412d-120">In this section</span></span>



| <span data-ttu-id="9412d-121">主題</span><span class="sxs-lookup"><span data-stu-id="9412d-121">Topic</span></span>                                                                                          | <span data-ttu-id="9412d-122">描述</span><span class="sxs-lookup"><span data-stu-id="9412d-122">Description</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9412d-123">Direct2D 的新功能</span><span class="sxs-lookup"><span data-stu-id="9412d-123">What's new in Direct2D</span></span>](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="9412d-124">以下是一些 Direct2D 新增專案。</span><span class="sxs-lookup"><span data-stu-id="9412d-124">Here are some of the new additions to Direct2D.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="9412d-125">關於 Direct2D</span><span class="sxs-lookup"><span data-stu-id="9412d-125">About Direct2D</span></span>](direct2d-overview.md)<br/>                                             | <span data-ttu-id="9412d-126">介紹 Direct2D，這是一個 API，可讓 Win32 開發人員能夠執行具有優異效能和視覺品質的2D 圖形轉譯工作。</span><span class="sxs-lookup"><span data-stu-id="9412d-126">Introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span> <br/> |
| [<span data-ttu-id="9412d-127">Windows 8 的 Direct2D 快速入門</span><span class="sxs-lookup"><span data-stu-id="9412d-127">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)<br/>    | <span data-ttu-id="9412d-128">摘要說明使用 Direct2D 進行繪製所需的步驟，並提供範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="9412d-128">Summarizes the steps required to draw with Direct2D and provides example code.</span></span><br/>                                                                                     |
| [<span data-ttu-id="9412d-129">使用 Direct2D 開始使用</span><span class="sxs-lookup"><span data-stu-id="9412d-129">Getting Started with Direct2D</span></span>](getting-started-with-direct2d-nav.md)<br/>              | <span data-ttu-id="9412d-130">說明如何開始建立 Direct2D 應用程式，並提供範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="9412d-130">Describes how to get started creating Direct2D applications and provides example code.</span></span><br/>                                                                             |
| [<span data-ttu-id="9412d-131">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="9412d-131">Programming Guide</span></span>](programming-guide.md)<br/>                                          | <span data-ttu-id="9412d-132">本節包含描述如何使用 Direct2D API 的概念程式設計主題。</span><span class="sxs-lookup"><span data-stu-id="9412d-132">This section contains conceptual programming topics that describe how to use the Direct2D API.</span></span> <br/>                                                                    |
| [<span data-ttu-id="9412d-133">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="9412d-133">Direct2D reference</span></span>](reference.md)<br/>                                                      | <span data-ttu-id="9412d-134">詳細說明 Direct2D API。</span><span class="sxs-lookup"><span data-stu-id="9412d-134">Describes the Direct2D API in detail.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="9412d-135">工具和公用程式</span><span class="sxs-lookup"><span data-stu-id="9412d-135">Tools and Utilities</span></span>](tools-and-utilities.md)<br/>                                      | <span data-ttu-id="9412d-136">為 Direct2D 提供的工具和公用程式。</span><span class="sxs-lookup"><span data-stu-id="9412d-136">Tools and utilities provided for Direct2D.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="9412d-137">範例</span><span class="sxs-lookup"><span data-stu-id="9412d-137">Samples</span></span>](d2d-samples.md)<br/>                                                          | <span data-ttu-id="9412d-138">示範 Direct2D API 的範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="9412d-138">Sample applications that demonstrate the Direct2D API.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="9412d-139">Direct2D 詞彙</span><span class="sxs-lookup"><span data-stu-id="9412d-139">Direct2D Glossary</span></span>](direct2d-glossary.md)<br/>                                          | <span data-ttu-id="9412d-140">描述 Direct2D 檔一般使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="9412d-140">Describes terms commonly used by the Direct2D documentation.</span></span> <br/>                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="9412d-141">其他資源</span><span class="sxs-lookup"><span data-stu-id="9412d-141">Additional resources</span></span>

-   [<span data-ttu-id="9412d-142">**DirectX 圖形與遊戲**</span><span class="sxs-lookup"><span data-stu-id="9412d-142">**DirectX Graphics and Gaming**</span></span>](/windows/desktop/directx)
-   [<span data-ttu-id="9412d-143">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="9412d-143">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)

 

