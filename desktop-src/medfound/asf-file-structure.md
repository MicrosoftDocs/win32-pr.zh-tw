---
description: 本主題將說明 Advanced 系統格式的結構 (ASF) 檔。
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: ASF 檔案結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510829"
---
# <a name="asf-file-structure"></a><span data-ttu-id="0a1a8-103">ASF 檔案結構</span><span class="sxs-lookup"><span data-stu-id="0a1a8-103">ASF File Structure</span></span>

<span data-ttu-id="0a1a8-104">本主題將說明 Advanced 系統格式的結構 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-104">This topic describes the structure of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="0a1a8-105">如需 ASF 檔案的詳細資訊，請下載 [Asf 規格](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-105">For detailed information about ASF files, download the [ASF Specification](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span> <span data-ttu-id="0a1a8-106">您也可以使用 [Windows MEDIA ASF Viewer 9 系列](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) 工具來查看現有 ASF 檔案的結構。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-106">You can also use the [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) tool to see the structure of an existing ASF file.</span></span>

<span data-ttu-id="0a1a8-107">ASF 檔案的組織基礎單位稱為 *物件*。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-107">The base unit of organization for ASF files is called an *object*.</span></span> <span data-ttu-id="0a1a8-108">ASF 檔案物件包含下列資料。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-108">An ASF file object contains the following data.</span></span>



| <span data-ttu-id="0a1a8-109">資料</span><span class="sxs-lookup"><span data-stu-id="0a1a8-109">Data</span></span>                                                        | <span data-ttu-id="0a1a8-110">大小</span><span class="sxs-lookup"><span data-stu-id="0a1a8-110">Size</span></span>     |
|-------------------------------------------------------------|----------|
| <span data-ttu-id="0a1a8-111">識別物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-111">A GUID that identifies the object.</span></span>                          | <span data-ttu-id="0a1a8-112">128 位元</span><span class="sxs-lookup"><span data-stu-id="0a1a8-112">128 bits</span></span> |
| <span data-ttu-id="0a1a8-113">物件大小。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-113">The size of the object.</span></span>                                     | <span data-ttu-id="0a1a8-114">64-位。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-114">64-bits.</span></span> |
| <span data-ttu-id="0a1a8-115">物件資料。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-115">Object data.</span></span> <span data-ttu-id="0a1a8-116">物件資料可以包含其他 ASF 物件。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-116">The object data can contain other ASF objects.</span></span> | <span data-ttu-id="0a1a8-117">變動。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-117">Varies.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="0a1a8-118">ASF 檔案物件只是一個資料區塊。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-118">An ASF file object is simply a chunk of data.</span></span> <span data-ttu-id="0a1a8-119">它不是電腦程式設計中的物件。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-119">It is not an object in the computer programming sense.</span></span>

 

<span data-ttu-id="0a1a8-120">ASF 檔案包含三種類型的最上層檔案物件。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-120">An ASF file contains three types of top-level file objects.</span></span>



| <span data-ttu-id="0a1a8-121">ASF 檔案物件</span><span class="sxs-lookup"><span data-stu-id="0a1a8-121">ASF File Object</span></span>                                                                                                                      | <span data-ttu-id="0a1a8-122">Description</span><span class="sxs-lookup"><span data-stu-id="0a1a8-122">Description</span></span>                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a1a8-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header 物件</span><span class="sxs-lookup"><span data-stu-id="0a1a8-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header Object</span></span><br/>         | <span data-ttu-id="0a1a8-124">包含 ASF 檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-124">Contains information about the ASF file.</span></span><br/>  |
| <span data-ttu-id="0a1a8-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Data 物件</span><span class="sxs-lookup"><span data-stu-id="0a1a8-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Data Object</span></span><br/>                     | <span data-ttu-id="0a1a8-126">包含媒體資料的封包。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-126">Contains packets of media data.</span></span><br/>           |
| <span data-ttu-id="0a1a8-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> 索引物件 (s) </span><span class="sxs-lookup"><span data-stu-id="0a1a8-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Index Object(s)</span></span><br/> | <span data-ttu-id="0a1a8-128">包含一或多個索引。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-128">Contains one or more indexes.</span></span> <span data-ttu-id="0a1a8-129">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="0a1a8-129">(Optional.)</span></span><br/> |



 

<span data-ttu-id="0a1a8-130">下圖顯示 ASF 檔案結構。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-130">The following diagram shows the ASF file structure.</span></span>

![顯示 asf 檔案結構的圖表，包括標頭、資料和索引內的專案](images/asf-components04.png)

<span data-ttu-id="0a1a8-132">此圖表不會繪製以進行調整;通常，資料物件會包含大部分的檔案。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-132">This diagram is not drawn to scale; typically the Data Object comprises most of the file.</span></span>

### <a name="header-object"></a><span data-ttu-id="0a1a8-133">Header 物件</span><span class="sxs-lookup"><span data-stu-id="0a1a8-133">Header Object</span></span>

<span data-ttu-id="0a1a8-134">標頭物件是必要的，而且會出現在每個 ASF 檔案的開頭。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-134">The Header Object is mandatory and appears at the beginning of every ASF file.</span></span> <span data-ttu-id="0a1a8-135">它包含通用檔案屬性，以及有關 ASF 檔案中資料流程的資訊。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-135">It contains global file attributes and information about the streams in the ASF file.</span></span> <span data-ttu-id="0a1a8-136">這項資訊是用來解讀和播放檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-136">This information is used to interpret and play the data in the file.</span></span>

<span data-ttu-id="0a1a8-137">標頭物件包含數個強制子物件：</span><span class="sxs-lookup"><span data-stu-id="0a1a8-137">The Header Object contains several madatory sub-objects:</span></span>

-   <span data-ttu-id="0a1a8-138">檔案屬性物件會描述檔案的全域屬性，例如檔案大小、播放持續時間、資料封包數、最小和最大封包大小，以及最大位元速率。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-138">The File Properties Object describes global attributes of the file, such as the file size, play duration, number of data packets, minimum and maximum packet size, and maximum bit rate.</span></span>
-   <span data-ttu-id="0a1a8-139">標頭擴充物件可將其他功能新增至 ASF 檔案，同時維持回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-139">The Header Extension Object enables additional functionality to be added to an ASF file while maintaining backward compatibility.</span></span>
-   <span data-ttu-id="0a1a8-140">資料流程屬性物件會描述檔案中的一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-140">The Stream Properties Object describes one stream in the file.</span></span> <span data-ttu-id="0a1a8-141">ASF 檔案必須包含至少一個資料流程，因此至少必須包含一個資料流程屬性物件。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-141">An ASF file must contain at least one stream, and therefore at least one Stream Properties Object.</span></span>

<span data-ttu-id="0a1a8-142">標頭物件可以包含其他選用的資訊，包括與檔案相關的中繼資料 (例如標題和作者) 、用來編碼檔案的編解碼器清單，以及內容保護資訊。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-142">The Header Object can contain additional optional information, including metadata about the file (such as title and author), a list of the codecs used to encode the file, and content protection information.</span></span>

### <a name="data-object"></a><span data-ttu-id="0a1a8-143">資料物件</span><span class="sxs-lookup"><span data-stu-id="0a1a8-143">Data Object</span></span>

<span data-ttu-id="0a1a8-144">ASF 資料物件包含 ASF 檔案的所有媒體資料。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-144">The ASF Data Object contains all of the media data for the ASF file.</span></span> <span data-ttu-id="0a1a8-145">此物件是必要的，而且必須遵循 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-145">This object is mandatory and must follow the ASF Header Object.</span></span>

<span data-ttu-id="0a1a8-146">資料物件會分割成資料封 *包*。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-146">The Data Object is divided into data *packets*.</span></span> <span data-ttu-id="0a1a8-147">每個封包都包含檔案中一個或多個資料流程的資料。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-147">Each packet contains data for one or several streams in the file.</span></span> <span data-ttu-id="0a1a8-148">資料封包包含可提供封包剖析資訊的資料封包標頭，後面接著承載資料的實際數位媒體資料。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-148">A data packet contains a data packet header that provides packet parsing information, followed by the payload data the actual digital media data.</span></span> <span data-ttu-id="0a1a8-149">所有的資料封包都有相關聯的呈現時間，並依照收到的順序排列。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-149">All of the data packets have a presentation time associated with it and are arranged in the order received.</span></span>

<span data-ttu-id="0a1a8-150">資料物件內容的相關資訊（例如封包大小和封包計數）會儲存在標頭物件中。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-150">Information about the contents of the Data Object, such as the packet size and packet count, is stored in the Header Object.</span></span>

### <a name="index-object"></a><span data-ttu-id="0a1a8-151">Index 物件</span><span class="sxs-lookup"><span data-stu-id="0a1a8-151">Index Object</span></span>

<span data-ttu-id="0a1a8-152">索引物件是選擇性的，且是 ASF 檔案中的最後一個物件。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-152">The Index Object is optional and is the last object in the ASF file.</span></span> <span data-ttu-id="0a1a8-153">ASF 檔案可以包含一個以上的索引物件。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-153">An ASF file can contain more than one Index Object.</span></span> <span data-ttu-id="0a1a8-154">Index 物件提供以時間為基礎的隨機存取 ASF 資料物件。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-154">The Index Object provides time-based random access into the ASF Data Object.</span></span>

<span data-ttu-id="0a1a8-155">簡單的索引物件是另一種索引類型。</span><span class="sxs-lookup"><span data-stu-id="0a1a8-155">A Simple Index Object is another type of index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a1a8-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a1a8-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a1a8-157">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="0a1a8-157">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




