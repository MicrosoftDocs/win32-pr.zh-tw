---
description: 本主題說明如何在 Microsoft 媒體基礎中建立「ASF 設定檔」。
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: 建立 ASF 設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970746"
---
# <a name="creating-an-asf-profile"></a><span data-ttu-id="30a7c-103">建立 ASF 設定檔</span><span class="sxs-lookup"><span data-stu-id="30a7c-103">Creating an ASF Profile</span></span>

<span data-ttu-id="30a7c-104">本主題說明如何在 Microsoft 媒體基礎中建立「ASF 設定檔」。</span><span class="sxs-lookup"><span data-stu-id="30a7c-104">This topic describes how to create as ASF profile in Microsoft Media Foundation.</span></span>

-   [<span data-ttu-id="30a7c-105">建立新的設定檔</span><span class="sxs-lookup"><span data-stu-id="30a7c-105">Create a New Profile</span></span>](#create-a-new-profile)
-   [<span data-ttu-id="30a7c-106">從 ASF ContentInfo 物件取得設定檔</span><span class="sxs-lookup"><span data-stu-id="30a7c-106">Get the Profile from the ASF ContentInfo Object</span></span>](#get-the-profile-from-the-asf-contentinfo-object)
-   [<span data-ttu-id="30a7c-107">從簡報描述項取得設定檔</span><span class="sxs-lookup"><span data-stu-id="30a7c-107">Get the Profile from a Presentation Descriptor</span></span>](#get-the-profile-from-a-presentation-descriptor)
-   [<span data-ttu-id="30a7c-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="30a7c-108">Related topics</span></span>](#related-topics)

## <a name="create-a-new-profile"></a><span data-ttu-id="30a7c-109">建立新的設定檔</span><span class="sxs-lookup"><span data-stu-id="30a7c-109">Create a New Profile</span></span>

<span data-ttu-id="30a7c-110">若要建立空白的 ASF 設定檔，請呼叫 [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) 函數。</span><span class="sxs-lookup"><span data-stu-id="30a7c-110">To create an empty ASF profile, call the [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) function.</span></span> <span data-ttu-id="30a7c-111">此函數會傳回 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="30a7c-111">This function returns a pointer to the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="30a7c-112">應用程式可以使用此介面將資料流程新增至設定檔，並設定每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="30a7c-112">The application can use this interface to add streams to the profile, and to configure each of the streams.</span></span> <span data-ttu-id="30a7c-113">如需詳細資訊，請參閱 [建立及設定 ASF 資料流程](creating-and-configuring-asf-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="30a7c-113">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>

<span data-ttu-id="30a7c-114">（選擇性）應用程式可以將互斥物件新增至兩個或多個資料流程。</span><span class="sxs-lookup"><span data-stu-id="30a7c-114">Optionally, the application can add mutual-exclusion objects to two or more streams.</span></span> <span data-ttu-id="30a7c-115">請參閱 [使用 ASF 資料流程的相互排除](using-mutual-exclusion-for-asf-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="30a7c-115">See [Using Mutual Exclusion for ASF Streams](using-mutual-exclusion-for-asf-streams.md).</span></span>

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a><span data-ttu-id="30a7c-116">從 ASF ContentInfo 物件取得設定檔</span><span class="sxs-lookup"><span data-stu-id="30a7c-116">Get the Profile from the ASF ContentInfo Object</span></span>

<span data-ttu-id="30a7c-117">應用程式可以從 [Asf ContentInfo 物件](asf-contentinfo-object.md)取得現有 asf 檔案的 asf 設定檔。</span><span class="sxs-lookup"><span data-stu-id="30a7c-117">An application can get the ASF profile of an existing ASF file from the [ASF ContentInfo Object](asf-contentinfo-object.md).</span></span> <span data-ttu-id="30a7c-118">設定檔已設定，而且包含檔案中所有資料流程的設定。</span><span class="sxs-lookup"><span data-stu-id="30a7c-118">The profile is already configured and contains settings for the all of the streams in the file.</span></span>

<span data-ttu-id="30a7c-119">藉由剖析檔案的 ASF 標頭物件來初始化 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="30a7c-119">Initialize the ContentInfo object by parsing the ASF Header Object of the file.</span></span> <span data-ttu-id="30a7c-120">這是透過 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="30a7c-120">This is done through the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="30a7c-121">讀取所有的標頭物件並填入 ASF 程式庫之後，就會產生此檔案的設定檔。</span><span class="sxs-lookup"><span data-stu-id="30a7c-121">After all the Header Objects are read and the ASF library is populated, the profile for this file is generated.</span></span> <span data-ttu-id="30a7c-122">應用程式可以藉由呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)來取得這個已初始化設定檔的指標。</span><span class="sxs-lookup"><span data-stu-id="30a7c-122">The application can get a pointer to this initialized profile by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>

## <a name="get-the-profile-from-a-presentation-descriptor"></a><span data-ttu-id="30a7c-123">從簡報描述項取得設定檔</span><span class="sxs-lookup"><span data-stu-id="30a7c-123">Get the Profile from a Presentation Descriptor</span></span>

<span data-ttu-id="30a7c-124">您可以從檔案的 [呈現描述](presentation-descriptors.md) 項，或從 [ASF ContentInfo](asf-contentinfo-object.md) 物件取得現有 ASF 檔案的設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="30a7c-124">You can get the profile object of an existing ASF file from the [presentation descriptor](presentation-descriptors.md) for the file, or from the [ASF ContentInfo](asf-contentinfo-object.md) object.</span></span> <span data-ttu-id="30a7c-125">在此情況下，已設定設定檔，並包含檔案中所有資料流程的設定。</span><span class="sxs-lookup"><span data-stu-id="30a7c-125">In this case, the profile is already configured and contains settings for all of the streams in the file.</span></span> <span data-ttu-id="30a7c-126">如果您想要修改現有的 ASF 設定檔，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="30a7c-126">This can be useful if you want to modify an existing ASF profile.</span></span> <span data-ttu-id="30a7c-127">例如，您可能想要以較低的位元速率重新編碼 Windows Media 視訊檔案。</span><span class="sxs-lookup"><span data-stu-id="30a7c-127">For example, you might wish to re-encode a Windows Media Video file at a lower bit rate.</span></span>

<span data-ttu-id="30a7c-128">若要從呈現描述項取得設定檔，請呼叫 [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor)。</span><span class="sxs-lookup"><span data-stu-id="30a7c-128">To get the profile from the presentation descriptor, call [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span></span> <span data-ttu-id="30a7c-129">此函式會剖析展示描述項，並在 ASF 設定檔中填入媒體檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="30a7c-129">This function parses the presentation descriptor, and populates an ASF profile with information about the media file.</span></span> <span data-ttu-id="30a7c-130">函數會傳回 IMFASFProfile 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="30a7c-130">The function returns a pointer to the IMFASFProfile interface.</span></span> <span data-ttu-id="30a7c-131">然後，您可以使用此介面來修改設定檔。</span><span class="sxs-lookup"><span data-stu-id="30a7c-131">You can then use this interface to modify the profile.</span></span>

<span data-ttu-id="30a7c-132">若要取得簡報描述項，請呼叫下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="30a7c-132">To get the presentation descriptor, call one of the following methods:</span></span>

-   <span data-ttu-id="30a7c-133">從 ASF 媒體來源，呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)。</span><span class="sxs-lookup"><span data-stu-id="30a7c-133">From the ASF media source, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="30a7c-134">從 [ASF ContentInfo](asf-contentinfo-object.md) 物件中，呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)。</span><span class="sxs-lookup"><span data-stu-id="30a7c-134">From the [ASF ContentInfo](asf-contentinfo-object.md) object, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="30a7c-135">在呼叫這個方法之前，請確定已初始化 ContentInfo 物件進行讀取。</span><span class="sxs-lookup"><span data-stu-id="30a7c-135">Prior to calling this method, make sure that the ContentInfo object is initialized for reading.</span></span> <span data-ttu-id="30a7c-136">如需詳細資訊，請參閱 [讀取現有檔案的 Asf 標頭物件](reading-the-asf-header-object-of-an-existing-file.md)中的「從現有的 ASF 檔案初始化 ContentInfo 物件」。</span><span class="sxs-lookup"><span data-stu-id="30a7c-136">For more information, see "Initializing the ContentInfo Object from an Existing ASF File" in [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span> <span data-ttu-id="30a7c-137">但是，如果您已經有初始化的 ContentInfo 物件，您可以直接從該物件取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="30a7c-137">However, if you already have an initialized ContentInfo object, you can get the profile directly from it.</span></span> <span data-ttu-id="30a7c-138">這會在本主題稍後的「從 ContentInfo 物件取得設定檔」中說明。</span><span class="sxs-lookup"><span data-stu-id="30a7c-138">This is described in "Getting the Profile from the ContentInfo Object " later in this topic.</span></span>

<span data-ttu-id="30a7c-139">下列範例示範如何從展示描述項建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="30a7c-139">The following example shows how to create a profile from a presentation descriptor.</span></span> <span data-ttu-id="30a7c-140">此函式會建立檔案的媒體來源、從媒體來源取得簡報描述項，並建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="30a7c-140">The function creates a media source for the file, gets the presentation descriptor from the media source, and creates a profile.</span></span> <span data-ttu-id="30a7c-141">此範例假設 *>pszfilename* 指定了 ASF 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="30a7c-141">This example assumes that *pszFileName* specifies the URL of an ASF file.</span></span>


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



<span data-ttu-id="30a7c-142">此範例會使用 [SafeRelease](saferelease.md) 來釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="30a7c-142">This example uses [SafeRelease](saferelease.md) to release interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30a7c-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="30a7c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30a7c-144">ASF 設定檔</span><span class="sxs-lookup"><span data-stu-id="30a7c-144">ASF Profile</span></span>](asf-profile.md)
</dt> </dl>

 

 



