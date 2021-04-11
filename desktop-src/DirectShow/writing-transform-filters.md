---
description: 寫入轉換篩選
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: 寫入轉換篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944433"
---
# <a name="writing-transform-filters"></a><span data-ttu-id="4cab3-103">寫入轉換篩選</span><span class="sxs-lookup"><span data-stu-id="4cab3-103">Writing Transform Filters</span></span>

<span data-ttu-id="4cab3-104">本節說明如何撰寫轉換篩選，定義為只有一個輸入 pin 和一個輸出 pin 的篩選。</span><span class="sxs-lookup"><span data-stu-id="4cab3-104">This section describes how to write a transform filter, defined as a filter that has exactly one input pin and one output pin.</span></span> <span data-ttu-id="4cab3-105">為了說明這些步驟，本節描述的假設轉換篩選會輸出執行長度 (RLE) 影片的編碼。</span><span class="sxs-lookup"><span data-stu-id="4cab3-105">To illustrate the steps, this section describes a hypothetical transform filter that outputs run-length encoded (RLE) video.</span></span> <span data-ttu-id="4cab3-106">它不會描述 RLE 編碼演算法本身，只描述 DirectShow 特定的工作。</span><span class="sxs-lookup"><span data-stu-id="4cab3-106">It does not describe the RLE-encoding algorithm itself, only the tasks that are specific to DirectShow.</span></span> <span data-ttu-id="4cab3-107"> (DirectShow 已經透過 [AVI 壓縮](avi-compressor-filter.md) 程式篩選器提供了 RLE 編解碼器。 ) </span><span class="sxs-lookup"><span data-stu-id="4cab3-107">(DirectShow already provides an RLE codec through the [AVI Compressor](avi-compressor-filter.md) filter.)</span></span>

<span data-ttu-id="4cab3-108">本節假設您將使用 DirectShow 基礎類別庫來建立篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4cab3-108">This section assumes that you will use the DirectShow base class library to create filters.</span></span> <span data-ttu-id="4cab3-109">雖然您可以寫入篩選器，但強烈建議使用基底類別庫。</span><span class="sxs-lookup"><span data-stu-id="4cab3-109">Although you can write a filter without it, the base class library is strongly recommended.</span></span>

> [!Note]  
> <span data-ttu-id="4cab3-110">寫入轉換篩選器之前，請考慮 DirectX 媒體物件 (]) 是否符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="4cab3-110">Before writing a transform filter, consider whether a DirectX Media Object (DMO) would fulfill your requirements.</span></span> <span data-ttu-id="4cab3-111">DMOs 可以進行許多與篩選相同的動作，而 DMOs 的程式設計模型比較簡單。</span><span class="sxs-lookup"><span data-stu-id="4cab3-111">DMOs can do many of the same things as filters, and the programming model for DMOs is simpler.</span></span> <span data-ttu-id="4cab3-112">DMOs 是透過包裝在 DirectShow [包裝](dmo-wrapper-filter.md) 函式篩選器中，但也可以在 directshow 之外使用。</span><span class="sxs-lookup"><span data-stu-id="4cab3-112">DMOs are hosted in DirectShow through the [DMO Wrapper](dmo-wrapper-filter.md) filter, but can also be used outside of DirectShow.</span></span> <span data-ttu-id="4cab3-113">DMOs 現在是適用于編碼器和解碼器的建議解決方案。</span><span class="sxs-lookup"><span data-stu-id="4cab3-113">DMOs are now the recommended solution for encoders and decoders.</span></span>

 

<span data-ttu-id="4cab3-114">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="4cab3-114">This section includes the following topics:</span></span>

-   [<span data-ttu-id="4cab3-115">步驟1。選擇基類</span><span class="sxs-lookup"><span data-stu-id="4cab3-115">Step 1. Choose a Base Class</span></span>](step-1--choose-a-base-class.md)
-   [<span data-ttu-id="4cab3-116">步驟2。宣告篩選類別</span><span class="sxs-lookup"><span data-stu-id="4cab3-116">Step 2. Declare the Filter Class</span></span>](step-2--declare-the-filter-class.md)
-   [<span data-ttu-id="4cab3-117">步驟3。支援媒體類型的協商</span><span class="sxs-lookup"><span data-stu-id="4cab3-117">Step 3. Support Media Type Negotiation</span></span>](step-3--support-media-type-negotiation.md)
-   [<span data-ttu-id="4cab3-118">步驟4：設定配置器屬性</span><span class="sxs-lookup"><span data-stu-id="4cab3-118">Step 4. Set Allocator Properties</span></span>](step-4--set-allocator-properties.md)
-   [<span data-ttu-id="4cab3-119">步驟5。轉換映射</span><span class="sxs-lookup"><span data-stu-id="4cab3-119">Step 5. Transform the Image</span></span>](step-5--transform-the-image.md)
-   [<span data-ttu-id="4cab3-120">步驟6：新增對 COM 的支援</span><span class="sxs-lookup"><span data-stu-id="4cab3-120">Step 6. Add Support for COM</span></span>](step-6--add-support-for-com.md)

## <a name="related-topics"></a><span data-ttu-id="4cab3-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="4cab3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cab3-122">建立 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="4cab3-122">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="4cab3-123">DirectShow 基類</span><span class="sxs-lookup"><span data-stu-id="4cab3-123">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="4cab3-124">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="4cab3-124">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



