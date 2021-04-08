---
description: 筆墨分析程式庫有四個層級： Windows Forms、WPF、COM 和基底層。 本節說明使用每個圖層的時機。
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: 筆墨分析 API 使用方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943259"
---
# <a name="ink-analysis-api-usage"></a><span data-ttu-id="68e94-104">筆墨分析 API 使用方式</span><span class="sxs-lookup"><span data-stu-id="68e94-104">Ink Analysis API Usage</span></span>

<span data-ttu-id="68e94-105">筆墨分析程式庫有四個層級： Windows Forms、WPF、COM 和基底層。</span><span class="sxs-lookup"><span data-stu-id="68e94-105">There are four layers to the Ink Analysis library: Windows Forms, WPF, COM, and the base layer.</span></span> <span data-ttu-id="68e94-106">本節說明使用每個圖層的時機。</span><span class="sxs-lookup"><span data-stu-id="68e94-106">This section describes when to use each layer.</span></span>

## <a name="ink-analysis-api-overview"></a><span data-ttu-id="68e94-107">筆墨分析 API 總覽</span><span class="sxs-lookup"><span data-stu-id="68e94-107">Ink Analysis API Overview</span></span>

<span data-ttu-id="68e94-108">筆墨分析程式庫是設計用來在各種支援的程式設計環境中使用。</span><span class="sxs-lookup"><span data-stu-id="68e94-108">The Ink Analysis libraries are designed to be used in a variety of supported programming environments.</span></span> <span data-ttu-id="68e94-109">有四個基本層可讓您的應用程式使用筆墨分析。</span><span class="sxs-lookup"><span data-stu-id="68e94-109">There are four basic layers through which your application can make use of Ink Analysis.</span></span> <span data-ttu-id="68e94-110">這些層級如下：</span><span class="sxs-lookup"><span data-stu-id="68e94-110">These layers are:</span></span>

-   <span data-ttu-id="68e94-111">Windows Forms 層</span><span class="sxs-lookup"><span data-stu-id="68e94-111">The Windows Forms layer</span></span>
-   <span data-ttu-id="68e94-112">WPF 層</span><span class="sxs-lookup"><span data-stu-id="68e94-112">The WPF layer</span></span>
-   <span data-ttu-id="68e94-113">COM 層</span><span class="sxs-lookup"><span data-stu-id="68e94-113">The COM layer</span></span>
-   <span data-ttu-id="68e94-114">基底層</span><span class="sxs-lookup"><span data-stu-id="68e94-114">The base layer</span></span>

### <a name="windows-forms-applications"></a><span data-ttu-id="68e94-115">Windows Forms 應用程式</span><span class="sxs-lookup"><span data-stu-id="68e94-115">Windows Forms Applications</span></span>

<span data-ttu-id="68e94-116">您可以藉由新增下列程式庫的參考，在您的 managed 專案中使用筆墨分析 API：</span><span class="sxs-lookup"><span data-stu-id="68e94-116">You can use the Ink Analysis API in your managed project by adding a reference to the following libraries:</span></span>

-   <span data-ttu-id="68e94-117"> (Microsoft.Ink.Analysis.dll) 的 Microsoft Ink 分析</span><span class="sxs-lookup"><span data-stu-id="68e94-117">Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)</span></span>
-   <span data-ttu-id="68e94-118">筆墨檔分析庫 (IACore.dll) </span><span class="sxs-lookup"><span data-stu-id="68e94-118">Ink Document Analysis Library (IACore.dll)</span></span>

<span data-ttu-id="68e94-119">在 Windows Forms 應用程式中，您很有可能會使用程式庫搭配在 Microsoft Tablet PC API 1.7 版元件中找到的標準 Tablet PC 平臺物件。</span><span class="sxs-lookup"><span data-stu-id="68e94-119">In Windows Forms applications, you will most likely use the libraries in conjunction with the standard Tablet PC platform objects found in the Microsoft Tablet PC API v1.7 assembly.</span></span> <span data-ttu-id="68e94-120">確定您也有下列參考：</span><span class="sxs-lookup"><span data-stu-id="68e94-120">Be sure you also have a reference to:</span></span>

-   <span data-ttu-id="68e94-121">Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll) </span><span class="sxs-lookup"><span data-stu-id="68e94-121">Microsoft Tablet PC API v1.7.2600.2180 (Microsoft.Ink.dll)</span></span>

### <a name="windows-presentation-framework-applications"></a><span data-ttu-id="68e94-122">Windows Presentation Framework 應用程式</span><span class="sxs-lookup"><span data-stu-id="68e94-122">Windows Presentation Framework Applications</span></span>

<span data-ttu-id="68e94-123">您可以在 WPF 專案中使用筆墨分析 API，方法是將參考新增至 IAWinFX.dll 元件中的 System.object 命名空間中定義的筆墨分析成員。</span><span class="sxs-lookup"><span data-stu-id="68e94-123">You can use the Ink Analysis API in your WPF project by adding a reference to the Ink Analysis members that are defined in the System.Windows.Ink namespace in the IAWinFX.dll assembly.</span></span> <span data-ttu-id="68e94-124">SDK 會安裝此元件。</span><span class="sxs-lookup"><span data-stu-id="68e94-124">This assembly is installed by the SDK.</span></span>

### <a name="com-applications"></a><span data-ttu-id="68e94-125">COM 應用程式</span><span class="sxs-lookup"><span data-stu-id="68e94-125">COM Applications</span></span>

<span data-ttu-id="68e94-126">非自動化 COM 應用程式應該使用筆墨分析 Api 的 COM 層。</span><span class="sxs-lookup"><span data-stu-id="68e94-126">Non-Automation COM applications should use the COM layer of the Ink Analysis APIs.</span></span>

<span data-ttu-id="68e94-127">輸入特定的 [CoNtextNode](/previous-versions/ms551996(v=vs.100)) 物件（例如 [ParagraphNode](/previous-versions/ms580136(v=vs.100))、 [InkWordNode](/previous-versions/ms580133(v=vs.100))和其他物件）不會用於 COM 層。</span><span class="sxs-lookup"><span data-stu-id="68e94-127">Type specific [ContextNode](/previous-versions/ms551996(v=vs.100)) objects-such as [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100)), and others-are not used in the COM layer.</span></span> <span data-ttu-id="68e94-128">相反地，您應該在標準 [**ICoNtextNode**](icontextnode.md)介面上使用 [**ICoNtextNode：： AddPropertyData**](icontextnode-addpropertydata.md) 。</span><span class="sxs-lookup"><span data-stu-id="68e94-128">Rather, you should use the [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) on the standard [**IContextNode**](icontextnode.md) interface.</span></span>

<span data-ttu-id="68e94-129">您必須 \# 包含 "IACom .h"。</span><span class="sxs-lookup"><span data-stu-id="68e94-129">You must \#include "IACom.h".</span></span> <span data-ttu-id="68e94-130">您很可能會使用程式庫搭配使用 Tablet PC 平臺筆墨物件，因此您也應該 \# 包含 "msinkaut"。</span><span class="sxs-lookup"><span data-stu-id="68e94-130">You will most likely use the libraries in conjunction wit the Tablet PC platform Ink object, so you should also \#include "msinkaut.h".</span></span>

### <a name="rts-and-other-applications"></a><span data-ttu-id="68e94-131">RTS 和其他應用程式</span><span class="sxs-lookup"><span data-stu-id="68e94-131">RTS and Other Applications</span></span>

<span data-ttu-id="68e94-132">筆墨分析基底圖層的運作方式不同于其他專案，它會使用點資料進行分析，而不是 [筆劃](/previous-versions/ms552692(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="68e94-132">The Ink Analysis base layer works differently than the others in that it takes point data for analysis rather than [Stroke](/previous-versions/ms552692(v=vs.100)) objects.</span></span> <span data-ttu-id="68e94-133">您可以直接使用基底層而不是使用 Windows forms 或 COM 層的範例，包括不使用第一代 Tablet PC 平臺筆墨物件的應用程式，或是使用 [**RealTimeStylus**](realtimestylus-class.md) api 來管理手寫筆輸入的應用程式，而不是使用 Tablet Pc 平臺 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="68e94-133">Examples of where you would work with the Base layer directly rather than using the Windows forms or COM layers include applications that do not use first generation Tablet PC Platform Ink objects, or applications that use the [**RealTimeStylus**](realtimestylus-class.md) APIs to manage stylus input rather than using the Tablet PC Platform [Ink](/previous-versions/ms583670(v=vs.100)) objects.</span></span>

## <a name="32-bit-support-only"></a><span data-ttu-id="68e94-134">僅限32位支援</span><span class="sxs-lookup"><span data-stu-id="68e94-134">32-bit Support Only</span></span>

<span data-ttu-id="68e94-135">請注意，只有在32位的進程中才支援筆墨分析程式庫。</span><span class="sxs-lookup"><span data-stu-id="68e94-135">Note that the Ink Analysis libraries are only supported in 32-bit processes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68e94-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="68e94-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68e94-137">筆墨分析總覽</span><span class="sxs-lookup"><span data-stu-id="68e94-137">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="68e94-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="68e94-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 
