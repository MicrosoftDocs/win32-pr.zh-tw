---
description: 為新檔案撰寫 ASF 標頭物件
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: 為新檔案撰寫 ASF 標頭物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988391"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a><span data-ttu-id="3039e-103">為新檔案撰寫 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="3039e-103">Writing an ASF Header Object for a New File</span></span>

<span data-ttu-id="3039e-104">ASF ContentInfo 物件會儲存檔案的 ASF 標頭物件資訊。</span><span class="sxs-lookup"><span data-stu-id="3039e-104">The ASF ContentInfo object stores ASF Header Object information for a file.</span></span> <span data-ttu-id="3039e-105">建立或修改 ASF 檔案時，必須產生標頭物件。</span><span class="sxs-lookup"><span data-stu-id="3039e-105">When an ASF file is created or modified, the Header Object must be generated.</span></span> <span data-ttu-id="3039e-106">若要這樣做，應用程式必須將內容的編碼設定檔提供給 ContentInfo 物件，讓它知道要建立之媒體檔案的特性。</span><span class="sxs-lookup"><span data-stu-id="3039e-106">To do this, the application must provide the encoding profile of the content to the ContentInfo object so that it knows the characteristics of the media file to be created.</span></span>

<span data-ttu-id="3039e-107">若要撰寫新的檔案，您可以使用 ContentInfo 物件來：</span><span class="sxs-lookup"><span data-stu-id="3039e-107">For writing a new file, you can use the ContentInfo object to:</span></span>

-   <span data-ttu-id="3039e-108">從要建立之檔案的設定檔物件收集標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="3039e-108">Collect header information from the profile object of the file to be created,</span></span>
-   <span data-ttu-id="3039e-109">在媒體基礎的內部維護 ASF 程式庫中的各種標頭物件。</span><span class="sxs-lookup"><span data-stu-id="3039e-109">Populate various Header Objects in the ASF library maintained internally by Media Foundation,</span></span>
-   <span data-ttu-id="3039e-110">初始化 asf 資料封包產生的 [asf](asf-multiplexer.md) 多工器，以及</span><span class="sxs-lookup"><span data-stu-id="3039e-110">Initialize the [ASF Multiplexer](asf-multiplexer.md) for ASF data packet generation, and</span></span>
-   <span data-ttu-id="3039e-111">以可寫入檔案的二進位格式來建立最上層的標頭物件。</span><span class="sxs-lookup"><span data-stu-id="3039e-111">Construct the top-level Header Object in binary format that can be written to a file.</span></span>

<span data-ttu-id="3039e-112">如需設定檔的詳細資訊，請參閱 [ASF 設定檔](asf-profile.md)。</span><span class="sxs-lookup"><span data-stu-id="3039e-112">For information about profiles, see [ASF Profile](asf-profile.md).</span></span>

<span data-ttu-id="3039e-113">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="3039e-113">This section contains the following topics:</span></span>



| <span data-ttu-id="3039e-114">主題</span><span class="sxs-lookup"><span data-stu-id="3039e-114">Topic</span></span>                                                                                                              | <span data-ttu-id="3039e-115">描述</span><span class="sxs-lookup"><span data-stu-id="3039e-115">Description</span></span>                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3039e-116">初始化新 ASF 檔案的 ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="3039e-116">Initializing the ContentInfo Object of a New ASF File</span></span>](initializing-the-contentinfo-object-of-a-new-asf-file.md) | <span data-ttu-id="3039e-117">描述 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) 方法，該方法會使用儲存在設定檔物件中的標頭資訊來初始化 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="3039e-117">Describes the [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) method that initializes the ContentInfo object with header information stored in a profile object.</span></span> |
| [<span data-ttu-id="3039e-118">在 ContentInfo 物件中設定屬性</span><span class="sxs-lookup"><span data-stu-id="3039e-118">Setting Properties in the ContentInfo Object</span></span>](setting-properties-in-the-contentinfo-object.md)                   | <span data-ttu-id="3039e-119">必須在 ContentInfo 物件上設定之各種設定屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3039e-119">Information about various configuration properties that must be set on the ContentInfo object.</span></span>                                                                                         |
| [<span data-ttu-id="3039e-120">產生新的 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="3039e-120">Generating a New ASF Header Object</span></span>](generating-a-new-asf-header-object.md)                                       | <span data-ttu-id="3039e-121">如何從 ContentInfo 物件產生媒體緩衝區，其中包含新檔案的實際 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="3039e-121">How to generate a media buffer, which contains the actual ASF Header Object of the new file, from the ContentInfo object.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="3039e-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="3039e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3039e-123">ASF ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="3039e-123">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="3039e-124">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="3039e-124">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="3039e-125">ASF 檔案結構</span><span class="sxs-lookup"><span data-stu-id="3039e-125">ASF File Structure</span></span>
</dt> </dl>

 

 



