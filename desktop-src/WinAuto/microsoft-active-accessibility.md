---
title: Microsoft Active Accessibility
description: Microsoft Active Accessibility 是一種元件物件模型， (以 COM) 為基礎的技術，可改善協助工具輔助使用在 Microsoft Windows 上執行之應用程式的方式。
ms.assetid: f3e31c6f-c49e-4a61-99f1-b695ece2bfc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef277e54c34b64747811c4db40ecfb8fa1fb6bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682725"
---
# <a name="microsoft-active-accessibility"></a><span data-ttu-id="eceab-103">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="eceab-103">Microsoft Active Accessibility</span></span>

## <a name="purpose"></a><span data-ttu-id="eceab-104">目的</span><span class="sxs-lookup"><span data-stu-id="eceab-104">Purpose</span></span>

<span data-ttu-id="eceab-105">Microsoft Active Accessibility 是一種元件物件模型， (以 COM) 為基礎的技術，可改善協助工具輔助使用在 Microsoft Windows 上執行之應用程式的方式。</span><span class="sxs-lookup"><span data-stu-id="eceab-105">Microsoft Active Accessibility is a Component Object Model (COM)-based technology that improves the way accessibility aids work with applications running on Microsoft Windows.</span></span> <span data-ttu-id="eceab-106">它提供合併到作業系統中的動態連結程式庫，以及提供可靠方法來公開 UI 專案相關資訊的 COM 介面和 API 元素。</span><span class="sxs-lookup"><span data-stu-id="eceab-106">It provides dynamic-link libraries that are incorporated into the operating system as well as a COM interface and API elements that provide reliable methods for exposing information about UI elements.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="eceab-107">適用時</span><span class="sxs-lookup"><span data-stu-id="eceab-107">Where applicable</span></span>

<span data-ttu-id="eceab-108">藉由使用 Microsoft Active Accessibility 和遵循可存取的設計實務，開發人員可以讓具有視覺、聽力或動作障礙的許多人更容易存取在 Windows 上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="eceab-108">By using Microsoft Active Accessibility and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="eceab-109">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="eceab-109">Developer audience</span></span>

<span data-ttu-id="eceab-110">Microsoft Active Accessibility 主要是針對 C、c + + 和 Microsoft Visual Basic 開發人員所設計。</span><span class="sxs-lookup"><span data-stu-id="eceab-110">Microsoft Active Accessibility is designed primarily for C, C++, and Microsoft Visual Basic developers.</span></span> <span data-ttu-id="eceab-111">一般情況下，開發人員對於 COM 物件和介面以及 Unicode 都需要有中等程度的瞭解。</span><span class="sxs-lookup"><span data-stu-id="eceab-111">In general, developers need a moderate level of understanding about COM objects and interfaces as well as about Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="eceab-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="eceab-112">Run-time requirements</span></span>

<span data-ttu-id="eceab-113">Windows XP 和 Windows Server 2003 內建 Microsoft Active Accessibility 的完整支援。</span><span class="sxs-lookup"><span data-stu-id="eceab-113">Full support for Microsoft Active Accessibility is built into Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="eceab-114">Windows NT 4.0 （含 Service Pack 6） (SP6) 和更新版本，以及 Windows 98 Microsoft Active Accessibility 也支援。</span><span class="sxs-lookup"><span data-stu-id="eceab-114">Microsoft Active Accessibility is also supported on Windows NT 4.0 with Service Pack 6 (SP6) and later, and Windows 98.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eceab-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="eceab-115">In this section</span></span>



| <span data-ttu-id="eceab-116">主題</span><span class="sxs-lookup"><span data-stu-id="eceab-116">Topic</span></span>                                                             | <span data-ttu-id="eceab-117">描述</span><span class="sxs-lookup"><span data-stu-id="eceab-117">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eceab-118">快速入門</span><span class="sxs-lookup"><span data-stu-id="eceab-118">Getting Started</span></span>](getting-started.md)<br/>                 | <span data-ttu-id="eceab-119">Microsoft Active Accessibility 元件和支援平臺的簡介，以及 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化的簡短比較。</span><span class="sxs-lookup"><span data-stu-id="eceab-119">Introduction to the Microsoft Active Accessibility components and the supported platforms, and a brief comparison of Microsoft Active Accessibility and Microsoft UI Automation.</span></span><br/> |
| [<span data-ttu-id="eceab-120">技術總覽</span><span class="sxs-lookup"><span data-stu-id="eceab-120">Technical Overview</span></span>](technical-overview.md)<br/>           | <span data-ttu-id="eceab-121">Microsoft Active Accessibility 技術的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="eceab-121">General information about Microsoft Active Accessibility technology.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="eceab-122">C/c + + 開發人員指南</span><span class="sxs-lookup"><span data-stu-id="eceab-122">C/C++ Developer's Guide</span></span>](c-c---developer-s-guide.md)<br/> | <span data-ttu-id="eceab-123">從 C 或 c + + 應用程式開發人員的觀點來看 Microsoft Active Accessibility 如何運作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eceab-123">Information about how Microsoft Active Accessibility works from the perspective of a C or C++ application developer.</span></span> <span data-ttu-id="eceab-124">它涵蓋了用戶端和伺服器開發人員的特定問題。</span><span class="sxs-lookup"><span data-stu-id="eceab-124">It covers issues specific to client and server developers.</span></span><br/>  |
| [<span data-ttu-id="eceab-125">C/c + + 參考</span><span class="sxs-lookup"><span data-stu-id="eceab-125">C/C++ Reference</span></span>](c-c---reference.md)<br/>                 | <span data-ttu-id="eceab-126">適用于 C/c + + 開發人員的 Microsoft Active Accessibility API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="eceab-126">Reference documentation about the Microsoft Active Accessibility API for C/C++ developers.</span></span><br/>                                                                                       |
| [<span data-ttu-id="eceab-127">範例</span><span class="sxs-lookup"><span data-stu-id="eceab-127">Samples</span></span>](samples.md)<br/>                                 | <span data-ttu-id="eceab-128">示範如何使用 Microsoft Active Accessibility API 的程式範例。</span><span class="sxs-lookup"><span data-stu-id="eceab-128">Sample programs that demonstrate how to use the Microsoft Active Accessibility API.</span></span><br/>                                                                                              |
| [<span data-ttu-id="eceab-129">附錄</span><span class="sxs-lookup"><span data-stu-id="eceab-129">Appendixes</span></span>](appendixes.md)<br/>                           | <span data-ttu-id="eceab-130">Microsoft Active Accessibility 用戶端、伺服器開發人員和 Visual Basic 開發人員的其他參考資料。</span><span class="sxs-lookup"><span data-stu-id="eceab-130">Additional reference material for Microsoft Active Accessibility client and server developers and Visual Basic developers.</span></span><br/>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="eceab-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="eceab-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eceab-132">Microsoft 協助工具網站</span><span class="sxs-lookup"><span data-stu-id="eceab-132">Microsoft Accessibility website</span></span>](https://www.microsoft.com/enable/)
</dt> <dt>

[<span data-ttu-id="eceab-133">MSDN 上的 Microsoft 協助工具開發人員中心</span><span class="sxs-lookup"><span data-stu-id="eceab-133">Microsoft Accessibility Developer Center on MSDN</span></span>](/windows/apps/accessibility)
</dt> </dl>

 

