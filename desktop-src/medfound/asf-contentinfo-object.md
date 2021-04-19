---
description: ASF ContentInfo 物件
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: ASF ContentInfo 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966657"
---
# <a name="asf-contentinfo-object"></a><span data-ttu-id="9612e-103">ASF ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="9612e-103">ASF ContentInfo Object</span></span>

<span data-ttu-id="9612e-104">ASF *ContentInfo* 物件會儲存來自檔案之 ASF 標頭物件的資訊。</span><span class="sxs-lookup"><span data-stu-id="9612e-104">The ASF *ContentInfo* object stores information from the ASF Header Object of a file.</span></span> <span data-ttu-id="9612e-105">應用程式可基於下列目的使用 ContentInfo 物件：</span><span class="sxs-lookup"><span data-stu-id="9612e-105">An application can use the ContentInfo object for the following purposes:</span></span>

-   <span data-ttu-id="9612e-106">讀取現有媒體檔案的標頭物件。</span><span class="sxs-lookup"><span data-stu-id="9612e-106">Read the Header Object for an existing media file.</span></span> <span data-ttu-id="9612e-107">在此情況下，ContentInfo 物件會剖析標頭物件，並儲存特性檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9612e-107">In this case, the ContentInfo object parses the Header Object and stores information about the characteristics file.</span></span> <span data-ttu-id="9612e-108">媒體基礎透過屬性和介面公開數個屬性。</span><span class="sxs-lookup"><span data-stu-id="9612e-108">Media Foundation exposes several of these properties through attributes and interfaces.</span></span> <span data-ttu-id="9612e-109">這些會在 [ASF 標頭物件的媒體基礎屬性](media-foundation-attributes-for-asf-header-objects.md)中說明。</span><span class="sxs-lookup"><span data-stu-id="9612e-109">These are described in [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>
-   <span data-ttu-id="9612e-110">寫入標頭資訊，並為新檔案建立標頭物件。</span><span class="sxs-lookup"><span data-stu-id="9612e-110">Write header information and construct a Header Object for a new file.</span></span>
-   <span data-ttu-id="9612e-111">在讀取或寫入媒體檔案時，初始化其他 ASF 物件，例如 [Asf 分隔器](asf-splitter.md)、 [Asf](asf-multiplexer.md)多工器和 asf 索引子。</span><span class="sxs-lookup"><span data-stu-id="9612e-111">Initialize other ASF objects such as the [ASF Splitter](asf-splitter.md), [ASF Multiplexer](asf-multiplexer.md), and the ASF Indexer, while reading or writing a media file.</span></span>

<span data-ttu-id="9612e-112">如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="9612e-112">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="creating-the-contentinfo-object"></a><span data-ttu-id="9612e-113">建立 ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="9612e-113">Creating the ContentInfo Object</span></span>

<span data-ttu-id="9612e-114">若要建立 ContentInfo 物件的新實例，請呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="9612e-114">To create a new instance of the ContentInfo object, call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function.</span></span> <span data-ttu-id="9612e-115">這個方法會傳回空的 ContentInfo 物件的指標，此物件必須初始化以使用特定的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="9612e-115">This method returns a pointer to an empty ContentInfo object that must be initialized to work with a specific ASF file.</span></span> <span data-ttu-id="9612e-116">根據應用程式是要讀取現有的檔案或寫入新的 ASF 檔案，它必須呼叫 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 或 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) 來填入空的物件。</span><span class="sxs-lookup"><span data-stu-id="9612e-116">Depending on whether the application is reading an existing file or writing a new ASF file, it must call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) or [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to populate the empty object.</span></span>

<span data-ttu-id="9612e-117">如需這些方法呼叫的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9612e-117">For more information about these method calls, see the following topics:</span></span>

-   [<span data-ttu-id="9612e-118">讀取現有檔案的 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="9612e-118">Reading the ASF Header Object of an Existing File</span></span>](reading-the-asf-header-object-of-an-existing-file.md)
-   [<span data-ttu-id="9612e-119">從 ASF 標頭物件取得資訊</span><span class="sxs-lookup"><span data-stu-id="9612e-119">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
-   [<span data-ttu-id="9612e-120">為新檔案撰寫 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="9612e-120">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
-   [<span data-ttu-id="9612e-121">適用于 ASF 標頭物件的媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="9612e-121">Media Foundation Attributes for ASF Header Objects</span></span>](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a><span data-ttu-id="9612e-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="9612e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9612e-123">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="9612e-123">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



