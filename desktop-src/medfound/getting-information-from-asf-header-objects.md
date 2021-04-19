---
description: ASF 標頭資訊儲存在媒體檔案的 ASF 標頭物件中。
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: 從 ASF 標頭物件取得資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998219"
---
# <a name="getting-information-from-asf-header-objects"></a><span data-ttu-id="57b50-103">從 ASF 標頭物件取得資訊</span><span class="sxs-lookup"><span data-stu-id="57b50-103">Getting Information from ASF Header Objects</span></span>

<span data-ttu-id="57b50-104">ASF 標頭資訊儲存在媒體檔案的 ASF 標頭物件中。</span><span class="sxs-lookup"><span data-stu-id="57b50-104">ASF header information is stored in the ASF Header Objects of a media file.</span></span> <span data-ttu-id="57b50-105">媒體基礎提供 [ASF ContentInfo 物件](asf-contentinfo-object.md) 來使用標頭物件。</span><span class="sxs-lookup"><span data-stu-id="57b50-105">Media Foundation provides the [ASF ContentInfo Object](asf-contentinfo-object.md) to work with the Header Object.</span></span> <span data-ttu-id="57b50-106">需要填入的 ContentInfo 物件，應用程式才能讀取現有檔案的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="57b50-106">A populated ContentInfo object is required in order for the application to read header information of an existing file.</span></span> <span data-ttu-id="57b50-107">這可以藉由呼叫 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)來達成。</span><span class="sxs-lookup"><span data-stu-id="57b50-107">This is achieved by calling [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span> <span data-ttu-id="57b50-108">如果剖析成功完成，檔案的 ASF 程式庫（由媒體基礎在內部維護）會填入來自各種標頭物件的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="57b50-108">If parsing completes successfully, the ASF library for the file, which is maintained internally by Media Foundation, is populated with header information from various Header Objects.</span></span> <span data-ttu-id="57b50-109">其中有些屬性會公開給應用程式，它可以透過展示描述元、資料流程描述元、設定檔和中繼資料屬性上的屬性來取得。</span><span class="sxs-lookup"><span data-stu-id="57b50-109">Some of these properties are exposed to the application, which it can retrieve through attributes on the presentation descriptor, stream descriptor, the profile, and metadata properties.</span></span>

<span data-ttu-id="57b50-110">如需屬性的完整清單，請參閱 [適用于 ASF 標頭物件的媒體基礎屬性](media-foundation-attributes-for-asf-header-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="57b50-110">For the complete list of attributes, see [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a><span data-ttu-id="57b50-111">從簡報描述元中取出標頭資訊</span><span class="sxs-lookup"><span data-stu-id="57b50-111">Retrieving Header Information from a Presentation Descriptor</span></span>

<span data-ttu-id="57b50-112">簡報描述元物件包含特定媒體來源的說明，在此案例中為 ASF 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="57b50-112">A presentation descriptor object contains the description of a particular media source, in this case the ASF media source.</span></span> <span data-ttu-id="57b50-113">如果 **ParseHeader** 呼叫順利完成，就會將標頭物件中的檔案層級資訊儲存為表示描述項的屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-113">If the **ParseHeader** call completes successfully, file-level information from the Header Object is stored as attributes on the presentation descriptor.</span></span> <span data-ttu-id="57b50-114">若要建立展示描述項，請呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)。</span><span class="sxs-lookup"><span data-stu-id="57b50-114">To create the presentation descriptor, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="57b50-115">這個方法會傳回填入的表示描述元物件的指標，其中包含與 ContentInfo 物件相關聯之 ASF 檔案的這些屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-115">This method returns a pointer to a populated presentation descriptor object that contains these attributes for the ASF file associated with the ContentInfo object.</span></span> <span data-ttu-id="57b50-116">若要取得特定屬性的值，請在展示描述項上呼叫 **IMFAttributes：： Getxxx** 方法，並指定 **MF \_ PD \_ ASF \_ xxx** 屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-116">To get values for specific attributes, call **IMFAttributes::Getxxx** methods on the presentation descriptor and specify the **MF\_PD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="57b50-117">下列範例程式碼會抓取 ContentInfo 物件所指定之 ASF 檔案的播放持續時間。</span><span class="sxs-lookup"><span data-stu-id="57b50-117">The following example code retrieves the play duration of an ASF file, specified by a ContentInfo object.</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



<span data-ttu-id="57b50-118">如需一般展示描述項的詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。</span><span class="sxs-lookup"><span data-stu-id="57b50-118">For more information about presentation descriptors in general, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="57b50-119">如需完整的簡報描述元屬性集，請參閱 [展示描述項屬性](presentation-descriptor-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="57b50-119">For the complete set of presentation descriptor attributes, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-a-stream-descriptor"></a><span data-ttu-id="57b50-120">從資料流程描述元中取出標頭資訊</span><span class="sxs-lookup"><span data-stu-id="57b50-120">Retrieving Header Information from a Stream Descriptor</span></span>

<span data-ttu-id="57b50-121">資料流程描述元物件會公開 [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) 介面，並描述檔案中資料流程的特性。</span><span class="sxs-lookup"><span data-stu-id="57b50-121">A stream descriptor object exposes the [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface and describes the characteristics of the streams in the file.</span></span> <span data-ttu-id="57b50-122">ASF 內容的表示描述項包含一或多個代表標頭物件中所列之資料流程的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="57b50-122">The presentation descriptor for the ASF content contains one or more stream descriptors that represent the streams listed in the Header Object.</span></span> <span data-ttu-id="57b50-123">在 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) 的呼叫順利完成之後，基礎資料流程描述元會從不同的標頭物件填入資料流程層級資訊。</span><span class="sxs-lookup"><span data-stu-id="57b50-123">After the call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) completes successfully, the underlying stream descriptors are populated with stream-level information from the various Header Objects.</span></span> <span data-ttu-id="57b50-124">若要取得 ASF 資料流程的資料流程描述元，請在從 ContentInfo 物件產生的表示描述項上呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) 。</span><span class="sxs-lookup"><span data-stu-id="57b50-124">To get a stream descriptor for an ASF stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) on the presentation descriptor that is generated from the ContentInfo object.</span></span>

<span data-ttu-id="57b50-125">部分資料流程屬性會設定為數據流描述項的屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-125">Some of the stream properties are set as attributes on stream descriptors.</span></span> <span data-ttu-id="57b50-126">在資料流程描述項上呼叫 **IMFAttributes：： Getxxx** 方法，並 **指定 \_ MF \_ SD ASF \_ xxx** 屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-126">Call **IMFAttributes::Getxxx** methods on a stream descriptor and specify the **MF\_SD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="57b50-127">如需完整的資料流程描述元屬性集，請參閱 [資料流程描述項屬性](stream-descriptor-attributes.md)中所列的「ASF 特定的資料流程描述元」屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-127">For the complete set of stream descriptor attributes, see "ASF-Specific Stream Descriptor" attributes listed in [Stream Descriptor Attributes](stream-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-the-profile-object"></a><span data-ttu-id="57b50-128">從設定檔物件中取出標頭資訊</span><span class="sxs-lookup"><span data-stu-id="57b50-128">Retrieving Header Information from the Profile Object</span></span>

<span data-ttu-id="57b50-129">除了資料流程描述元之外，ASF 設定檔物件也會描述資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-129">In addition to stream descriptors, the ASF profile object also describes the stream properties.</span></span> <span data-ttu-id="57b50-130">若要取得現有 ASF 檔案的設定檔，請呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)。</span><span class="sxs-lookup"><span data-stu-id="57b50-130">To get the profile of an existing ASF file, call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="57b50-131">這個方法所傳回的 ASF 設定檔物件不包含任何 **MF \_ PD \_ ASF \_ xxx** 屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-131">The ASF profile object returned by this method does not include any of the **MF\_PD\_ASF\_xxx** attributes.</span></span> <span data-ttu-id="57b50-132">這些屬性只會在呼叫 [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) 從展示描述項產生設定檔物件之後，才可供應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="57b50-132">These attributes are available to the application only after it calls [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) to generate the profile object from a presentation descriptor.</span></span> <span data-ttu-id="57b50-133">您可以使用設定檔來取得相互排除的指標，以及串流處理優先權的物件。</span><span class="sxs-lookup"><span data-stu-id="57b50-133">You can use the profile to get pointers to the mutual exclusion and stream prioritization objects.</span></span>

<span data-ttu-id="57b50-134">如需設定檔物件的詳細資訊，請參閱 [ASF 設定檔](asf-profile.md) 。</span><span class="sxs-lookup"><span data-stu-id="57b50-134">For information about the profile object, see [ASF Profile](asf-profile.md) .</span></span>

## <a name="retrieving-metadata-from-header-objects"></a><span data-ttu-id="57b50-135">從標頭物件中取出中繼資料</span><span class="sxs-lookup"><span data-stu-id="57b50-135">Retrieving Metadata from Header Objects</span></span>

<span data-ttu-id="57b50-136">ASF 檔案可以包含數個在檔案編碼期間設定的中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-136">An ASF file can contain several metadata properties that are set during file encoding.</span></span> <span data-ttu-id="57b50-137">應用程式可以使用 ContentInfo 物件來列舉這些屬性。</span><span class="sxs-lookup"><span data-stu-id="57b50-137">An application can enumerate these properties with the ContentInfo object.</span></span> <span data-ttu-id="57b50-138">其中有些屬性（例如變數位元速率 (VBR) 資訊）可透過展示描述元、串流描述項的屬性，以及媒體檔案的媒體類型，提供給應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="57b50-138">Some of these properties, such as variable bit rate (VBR) information, are available to the application through attributes on presentation descriptor, stream descriptors, and media types for the media file.</span></span> <span data-ttu-id="57b50-139">這些屬性是在透過 [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 呼叫初始化期間，于 ContentInfo 物件上設定的。</span><span class="sxs-lookup"><span data-stu-id="57b50-139">These attributes are set on the ContentInfo object during initialization through the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57b50-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="57b50-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57b50-141">ASF ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="57b50-141">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> </dl>

 

 



