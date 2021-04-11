---
description: Windows Imaging Component
ms.assetid: b872baf9-9fcb-4604-a518-26e109eda792
title: Windows Imaging Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00bb18e2e432abbe3cfb3b72d28ceb4182e63ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193710"
---
# <a name="windows-imaging-component"></a><span data-ttu-id="187b4-103">Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="187b4-103">Windows Imaging Component</span></span>

## <a name="purpose"></a><span data-ttu-id="187b4-104">目的</span><span class="sxs-lookup"><span data-stu-id="187b4-104">Purpose</span></span>

<span data-ttu-id="187b4-105">Windows 影像處理元件 (WIC) 是可延伸的平臺，可為數字影像提供低層級的 API。</span><span class="sxs-lookup"><span data-stu-id="187b4-105">The Windows Imaging Component (WIC) is an extensible platform that provides low-level API for digital images.</span></span>  <span data-ttu-id="187b4-106">WIC 支援標準 web 映射格式、高動態範圍影像和原始相機資料。</span><span class="sxs-lookup"><span data-stu-id="187b4-106">WIC supports the standard web image formats, high dynamic range images, and raw camera data.</span></span>  <span data-ttu-id="187b4-107">WIC 也支援其他功能，例如：</span><span class="sxs-lookup"><span data-stu-id="187b4-107">WIC also supports additional features such as:</span></span>

-   <span data-ttu-id="187b4-108">標準元資料格式的內建支援</span><span class="sxs-lookup"><span data-stu-id="187b4-108">Built-in support for standard metadata formats</span></span>
-   <span data-ttu-id="187b4-109">映射編解碼器、像素格式和元資料格式的可擴充架構。</span><span class="sxs-lookup"><span data-stu-id="187b4-109">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>
-   <span data-ttu-id="187b4-110">範圍廣泛的像素格式支援。</span><span class="sxs-lookup"><span data-stu-id="187b4-110">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="187b4-111">高彩支援;包含30位的延伸範圍、30位高精確度，以及48位高精確度和寬範圍像素格式。</span><span class="sxs-lookup"><span data-stu-id="187b4-111">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="187b4-112">漸進式影像解碼。</span><span class="sxs-lookup"><span data-stu-id="187b4-112">Progressive image decoding.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="187b4-113">開發人員讀者</span><span class="sxs-lookup"><span data-stu-id="187b4-113">Developer Audience</span></span>

<span data-ttu-id="187b4-114">WIC 的設計是為了符合下列開發人員類別的需求：</span><span class="sxs-lookup"><span data-stu-id="187b4-114">WIC is designed to meet the needs of the following classes of developers:</span></span>

-   <span data-ttu-id="187b4-115">在應用程式中讀取和寫入影像資料的開發人員。</span><span class="sxs-lookup"><span data-stu-id="187b4-115">Developers who read and write image data in an application.</span></span>
-   <span data-ttu-id="187b4-116">在應用程式中讀取和寫入影像中繼資料的開發人員。</span><span class="sxs-lookup"><span data-stu-id="187b4-116">Developers who read and write image metadata in an application.</span></span>
-   <span data-ttu-id="187b4-117">需要針對新設計或實作為映射編解碼器進行執行時間編解碼器探索的開發人員。</span><span class="sxs-lookup"><span data-stu-id="187b4-117">Developers who want run-time codec discovery for newly designed or implemented image codecs.</span></span>
-   <span data-ttu-id="187b4-118">開發人員設計或執行新的映射編解碼器和元資料格式。</span><span class="sxs-lookup"><span data-stu-id="187b4-118">Developers designing or implementing new image codecs and metadata formats.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="187b4-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="187b4-119">In this section</span></span>



| <span data-ttu-id="187b4-120">主題</span><span class="sxs-lookup"><span data-stu-id="187b4-120">Topic</span></span>                                                                 | <span data-ttu-id="187b4-121">描述</span><span class="sxs-lookup"><span data-stu-id="187b4-121">Description</span></span>                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="187b4-122">WIC 的新功能</span><span class="sxs-lookup"><span data-stu-id="187b4-122">What's New in WIC</span></span>](what-s-new-in-wic-for-windows-8-1.md)<br/> |                                                     |
| [<span data-ttu-id="187b4-123">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="187b4-123">Programming Guide</span></span>](-wic-programming-guide.md)<br/>            | <span data-ttu-id="187b4-124">說明如何使用 WIC Api。</span><span class="sxs-lookup"><span data-stu-id="187b4-124">Describes how to use the WIC APIs.</span></span><br/>       |
| [<span data-ttu-id="187b4-125">參考</span><span class="sxs-lookup"><span data-stu-id="187b4-125">Reference</span></span>](-wic-codec-reference.md)<br/>                      | <span data-ttu-id="187b4-126">包含 WIC Api 的參考。</span><span class="sxs-lookup"><span data-stu-id="187b4-126">Contains the reference for the WIC APIs.</span></span><br/> |
| [<span data-ttu-id="187b4-127">WIC 範例</span><span class="sxs-lookup"><span data-stu-id="187b4-127">WIC Samples</span></span>](-wic-samples.md)<br/>                            | <span data-ttu-id="187b4-128">提供 WIC 的範例。</span><span class="sxs-lookup"><span data-stu-id="187b4-128">Provides samples for WIC.</span></span><br/>                |
| [<span data-ttu-id="187b4-129">詞彙</span><span class="sxs-lookup"><span data-stu-id="187b4-129">Glossary</span></span>](-wic-glossary.md)<br/>                              | <span data-ttu-id="187b4-130">定義 WIC 中使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="187b4-130">Defines terms that are used in WIC.</span></span><br/>      |



 

 

 




