---
description: 有一些格式可供儲存筆墨資料，包括：
ms.assetid: b08fba71-46cb-4419-9da5-a33a5b9a5ec0
title: 筆墨資料格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ccd0ab298e183867a9c4f8018727f22e51e7bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318104"
---
# <a name="ink-data-formats"></a><span data-ttu-id="45197-103">筆墨資料格式</span><span class="sxs-lookup"><span data-stu-id="45197-103">Ink Data Formats</span></span>

<span data-ttu-id="45197-104">有一些格式可供儲存筆墨資料，包括：</span><span class="sxs-lookup"><span data-stu-id="45197-104">There are a number of formats in which ink data can be stored, including:</span></span>

-   <span data-ttu-id="45197-105"> (ISF 的筆墨序列化格式) </span><span class="sxs-lookup"><span data-stu-id="45197-105">Ink serialized format (ISF)</span></span>
-   <span data-ttu-id="45197-106">HTML</span><span class="sxs-lookup"><span data-stu-id="45197-106">HTML</span></span>
-   <span data-ttu-id="45197-107">RTF 格式 (RTF)</span><span class="sxs-lookup"><span data-stu-id="45197-107">Rich Text Format (RTF)</span></span>
-   <span data-ttu-id="45197-108">二進位格式</span><span class="sxs-lookup"><span data-stu-id="45197-108">Binary format</span></span>
-   <span data-ttu-id="45197-109">可延伸標記語言 (XML)  (以 XML) 為基礎的格式</span><span class="sxs-lookup"><span data-stu-id="45197-109">Extensible Markup Language (XML) based formats</span></span>

<span data-ttu-id="45197-110">不同的格式適用于不同的情況。</span><span class="sxs-lookup"><span data-stu-id="45197-110">Different formats are applicable under different circumstances.</span></span> <span data-ttu-id="45197-111">為了成功與剪貼簿互動，應用程式應該能夠辨識和產生最多不同的格式。</span><span class="sxs-lookup"><span data-stu-id="45197-111">To interact most successfully with the Clipboard, applications should be able to recognize and generate as many different formats as possible.</span></span>

<span data-ttu-id="45197-112">可以用來儲存筆跡的最重要和基本格式是筆跡序列化格式 (ISF) 。</span><span class="sxs-lookup"><span data-stu-id="45197-112">The most important and basic format that can be used to store ink is Ink Serialized Format (ISF).</span></span> <span data-ttu-id="45197-113">ISF 提供精簡但完整的單一 [**筆墨**](inkdisp-class.md) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="45197-113">ISF provides a compact but complete representation of a single [**Ink**](inkdisp-class.md) object.</span></span>

<span data-ttu-id="45197-114">同樣重要的格式是 HTML。</span><span class="sxs-lookup"><span data-stu-id="45197-114">An equally important format is HTML.</span></span> <span data-ttu-id="45197-115">筆墨資料可以用 HTML 表示，因為無法辨識筆墨的應用程式可將其視為影像。</span><span class="sxs-lookup"><span data-stu-id="45197-115">Ink data can be represented in HTML in such a way that it can be viewed as an image by applications that do not recognize ink.</span></span> <span data-ttu-id="45197-116">此外，還會維護筆墨的完整精確度。</span><span class="sxs-lookup"><span data-stu-id="45197-116">In addition, the full fidelity of the ink is maintained.</span></span> <span data-ttu-id="45197-117">基於這些理由，而且因為它是一種常用的格式，可讓您呈現許多不同類型的內容，Microsoft 建議使用 HTML 作為共用筆墨的格式。</span><span class="sxs-lookup"><span data-stu-id="45197-117">For these reasons, and because it is a commonly understood format that allows for the representation of many different types of content, Microsoft recommends HTML as the format for sharing ink.</span></span>

<span data-ttu-id="45197-118">也可以儲存其他格式的筆跡。</span><span class="sxs-lookup"><span data-stu-id="45197-118">It is possible to store ink in other formats, as well.</span></span> <span data-ttu-id="45197-119">使用 RTF 格式時，您可以將筆跡貼到無法辨識筆墨的應用程式，例如 Microsoft Word 2002。</span><span class="sxs-lookup"><span data-stu-id="45197-119">By using RTF as the format, you can paste ink into applications that do not recognize ink, such as Microsoft Word 2002.</span></span> <span data-ttu-id="45197-120">這是藉由在 RTF 內內嵌包含筆墨的 OLE 物件來完成。</span><span class="sxs-lookup"><span data-stu-id="45197-120">This is done by embedding OLE objects that contain ink within the RTF.</span></span> <span data-ttu-id="45197-121">您仍可使用其他格式，例如二進位或以 XML 為基礎的格式。</span><span class="sxs-lookup"><span data-stu-id="45197-121">Still other formats, such as binary or XML-based formats, can be used.</span></span>

<span data-ttu-id="45197-122">您針對特定應用程式所選擇要複製、貼上或序列化筆墨的格式，應以應用程式特定的需求和資源為基礎。</span><span class="sxs-lookup"><span data-stu-id="45197-122">The formats you choose for a particular application to copy, paste, or serialize ink should be based on that applications specific needs and resources.</span></span> <span data-ttu-id="45197-123">應用程式至少應該能夠複製和貼上 ISF，以允許最低層級的筆墨互通性。</span><span class="sxs-lookup"><span data-stu-id="45197-123">At a minimum, an application should be able to copy and paste ISF, which allows for the lowest level of ink interoperability.</span></span> <span data-ttu-id="45197-124">ISF 和複製和貼上 ISF 的能力都內建于 Tablet PC 平臺中。</span><span class="sxs-lookup"><span data-stu-id="45197-124">Both ISF and the ability to copy and paste ISF are built into the Tablet PC platform.</span></span> <span data-ttu-id="45197-125">不過，許多應用程式需要表示更複雜的內容，例如包含多個筆墨物件或格式化文字的選取專案。</span><span class="sxs-lookup"><span data-stu-id="45197-125">However, many applications need to represent more complex content, such as a selection containing multiple ink objects or formatted text.</span></span> <span data-ttu-id="45197-126">在這種情況下，應用程式可以複製並貼上 HTML。</span><span class="sxs-lookup"><span data-stu-id="45197-126">In such a case, an application can copy and paste HTML.</span></span> <span data-ttu-id="45197-127">這可提供最大的彈性。</span><span class="sxs-lookup"><span data-stu-id="45197-127">This allows for a maximum amount of flexibility.</span></span> <span data-ttu-id="45197-128">HTML 已廣泛地理解且容易產生。</span><span class="sxs-lookup"><span data-stu-id="45197-128">HTML is widely understood and easy to generate.</span></span> <span data-ttu-id="45197-129">最後，已經產生 RTF 或強式與繼承應用程式通訊的應用程式，也應該產生 RTF 格式。</span><span class="sxs-lookup"><span data-stu-id="45197-129">Finally, applications that already produce RTF or have a strong need to communicate with older applications should produce an RTF format as well.</span></span>

> [!Note]  
> <span data-ttu-id="45197-130">在討論筆墨互通性、點陣圖、ISF 和 GIF 的過程中，都是影像格式。</span><span class="sxs-lookup"><span data-stu-id="45197-130">Throughout the discussion of ink interoperability, bitmap, ISF, and GIF are image formats.</span></span> <span data-ttu-id="45197-131">文字筆墨物件 (tInk) 和草圖筆墨物件 (接收) 是 OLE 物件。</span><span class="sxs-lookup"><span data-stu-id="45197-131">The text ink object (tInk) and sketch ink object (sInk) are OLE objects.</span></span> <span data-ttu-id="45197-132">二進位、HTML、XML 和 RTF 是使用影像的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="45197-132">Binary, HTML, XML, and RTF are document formats in which the images are consumed.</span></span>

 

<span data-ttu-id="45197-133">Tablet PC 平臺提供的 Api 可協助您產生及解讀這些格式。</span><span class="sxs-lookup"><span data-stu-id="45197-133">The Tablet PC platform provides APIs to help you generate and interpret these formats.</span></span> <span data-ttu-id="45197-134">有許多選項都應該符合任何應用程式的互通性和持續性需求。</span><span class="sxs-lookup"><span data-stu-id="45197-134">There are many options that together should fit the interoperability and persistence needs of any application.</span></span> <span data-ttu-id="45197-135">如需筆墨格式的詳細資訊，請參閱 [持續性格式](persistence-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="45197-135">For more information about ink formats, see [Persistence Formats](persistence-formats.md).</span></span>

 

 



