---
description: 當您安裝編解碼器時，必須在登錄中進行註冊。 如果電腦上已經有任何格式的影像，您也必須確定縮圖快取已更新。
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: 編解碼器安裝和註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989459"
---
# <a name="codec-installation-and-registration"></a><span data-ttu-id="e193a-104">編解碼器安裝和註冊</span><span class="sxs-lookup"><span data-stu-id="e193a-104">Codec Installation and Registration</span></span>

<span data-ttu-id="e193a-105">當您安裝編解碼器時，必須在登錄中進行註冊。</span><span class="sxs-lookup"><span data-stu-id="e193a-105">When you install a codec, you must register it in the registry.</span></span> <span data-ttu-id="e193a-106">如果電腦上已經有任何格式的影像，您也必須確定縮圖快取已更新。</span><span class="sxs-lookup"><span data-stu-id="e193a-106">You must also make sure the thumbnail cache gets updated in case any images in your format already exist on the computer.</span></span>

<span data-ttu-id="e193a-107">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="e193a-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="e193a-108">註冊編解碼器</span><span class="sxs-lookup"><span data-stu-id="e193a-108">Registering a Codec</span></span>](#registering-a-codec)
-   [<span data-ttu-id="e193a-109">安裝編解碼器時，更新縮圖快取</span><span class="sxs-lookup"><span data-stu-id="e193a-109">Updating the Thumbnail Cache When Installing Your Codec</span></span>](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [<span data-ttu-id="e193a-110">讓使用者使用您的 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="e193a-110">Making Your WIC-Enabled Codec Available To Users</span></span>](#making-your-wic-enabled-codec-available-to-users)
-   [<span data-ttu-id="e193a-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e193a-111">Related topics</span></span>](#related-topics)

## <a name="registering-a-codec"></a><span data-ttu-id="e193a-112">註冊編解碼器</span><span class="sxs-lookup"><span data-stu-id="e193a-112">Registering a Codec</span></span>

<span data-ttu-id="e193a-113">當您註冊編解碼器時，實際上是註冊兩個元件：編碼器和解碼器。</span><span class="sxs-lookup"><span data-stu-id="e193a-113">When you register a codec, you are actually registering two components: the encoder and the decoder.</span></span> <span data-ttu-id="e193a-114">您也需要建立登錄專案，以針對影像格式所支援的元資料格式，使用元資料處理程式來註冊您的容器格式。</span><span class="sxs-lookup"><span data-stu-id="e193a-114">You also need to make registry entries to register your container format with the metadata handlers for the metadata formats that your image format supports.</span></span>

<span data-ttu-id="e193a-115">下列主題描述您註冊編解碼器所需的登錄專案：</span><span class="sxs-lookup"><span data-stu-id="e193a-115">The following topics describe the registry entries you need to register your codec:</span></span>

[<span data-ttu-id="e193a-116">一般登錄專案</span><span class="sxs-lookup"><span data-stu-id="e193a-116">General Registry Entries</span></span>](-wic-generalregentries.md)

[<span data-ttu-id="e193a-117">編碼器特定的登錄專案</span><span class="sxs-lookup"><span data-stu-id="e193a-117">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)

[<span data-ttu-id="e193a-118">特定解碼器的登錄專案</span><span class="sxs-lookup"><span data-stu-id="e193a-118">Decoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)

[<span data-ttu-id="e193a-119">與 Windows 影像中心和 Windows 檔案總管整合</span><span class="sxs-lookup"><span data-stu-id="e193a-119">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a><span data-ttu-id="e193a-120">安裝編解碼器時，更新縮圖快取</span><span class="sxs-lookup"><span data-stu-id="e193a-120">Updating the Thumbnail Cache When Installing Your Codec</span></span>

<span data-ttu-id="e193a-121">安裝編解碼器之後，安裝程式必須在寫入其登錄專案之後呼叫下列函式。</span><span class="sxs-lookup"><span data-stu-id="e193a-121">When a codec is installed, the installer needs to call the following function after writing its registry entries.</span></span>


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



<span data-ttu-id="e193a-122">此呼叫會通知 Windows 有新的檔案關聯資訊可供使用。</span><span class="sxs-lookup"><span data-stu-id="e193a-122">This call notifies Windows that new file association information is available.</span></span> <span data-ttu-id="e193a-123">如果影像格式中的影像已經存在於電腦上，縮圖快取將包含它們的預設縮圖，因為在第一次取得映射時，沒有可用的解碼器可將縮圖解壓縮。</span><span class="sxs-lookup"><span data-stu-id="e193a-123">If images in your image format already exist on the computer, the thumbnail cache will contain default thumbnails for them because no decoder was available to extract the thumbnails when the images were first acquired.</span></span> <span data-ttu-id="e193a-124">當您通知 Windows 有新的檔案關聯可用時，縮圖快取會捨棄任何空白的縮圖，並從現在可解碼的檔案中解壓縮實際的縮圖。</span><span class="sxs-lookup"><span data-stu-id="e193a-124">When you notify Windows that a new file association is available, the thumbnail cache discards any empty thumbnails and extracts the actual thumbnails from the files that can now be decoded.</span></span>

## <a name="making-your-wic-enabled-codec-available-to-users"></a><span data-ttu-id="e193a-125">讓使用者使用您的 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="e193a-125">Making Your WIC-Enabled Codec Available To Users</span></span>

<span data-ttu-id="e193a-126">如果您是一家攝影機製造商，可以將您的原始編解碼器連同攝影機一起寄送。</span><span class="sxs-lookup"><span data-stu-id="e193a-126">If you are a camera manufacturer, you can ship your raw codecs in the box with your cameras.</span></span> <span data-ttu-id="e193a-127">您也可以在網站的下載頁面上張貼編解碼器。</span><span class="sxs-lookup"><span data-stu-id="e193a-127">You can also post your codecs on the Download page of your Web site.</span></span> <span data-ttu-id="e193a-128">不過，如果使用者從其他來源（例如朋友、商務夥伴或其他網站）取得格式的影像檔案，他們可能不知道要使用哪個編解碼器來將它解碼。</span><span class="sxs-lookup"><span data-stu-id="e193a-128">However, if a user acquires an image file in your format from some other source, such as a friend, business associate, or some other Web site, they may not know where to get the codec to decode it with.</span></span>

<span data-ttu-id="e193a-129">基於這個問題，Windows 提供更簡單的方式讓影像格式的使用者找到您的編解碼器，並將其下載到電腦上，從 Windows Vista 開始。</span><span class="sxs-lookup"><span data-stu-id="e193a-129">Because of this issue, Windows offers an easier way for users of your image format to find your codec and download it onto their computer, starting with Windows Vista.</span></span> <span data-ttu-id="e193a-130">如果 Windows 影像中心將副檔名辨識為影像格式，且未安裝該格式的編解碼器，對話方塊會告知使用者無法顯示相片，並詢問使用者是否要下載顯示該相片所需的軟體。</span><span class="sxs-lookup"><span data-stu-id="e193a-130">If the Windows Photo Gallery recognizes a file name extension as an image format, and the codec for that format is not installed, a dialog box tells the user that the photo can’t be displayed, and asks whether the user wants to download the software required to display it.</span></span> <span data-ttu-id="e193a-131">當使用者接受時，會出現 Microsoft 裝載的網站，其中包含編解碼器製造商下載網站的連結。</span><span class="sxs-lookup"><span data-stu-id="e193a-131">When the user accepts, a Microsoft-hosted Web site appears with a link to the codec manufacturer’s download site.</span></span> <span data-ttu-id="e193a-132"> (選擇性地，您可以要求使用者直接前往您的下載網站。 ) </span><span class="sxs-lookup"><span data-stu-id="e193a-132">(Optionally, you can request that users be taken directly to your download site.)</span></span>

<span data-ttu-id="e193a-133">如果您想要讓 Windows 影像中心辨識影像格式的副檔名，讓使用者可以導向至您的下載網站，您必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e193a-133">If you want your image format’s file name extensions to be recognized by the Windows Photo Gallery so that users can be directed to your download site, you must do the following:</span></span>

1.  <span data-ttu-id="e193a-134">提供編解碼器的下載網站。</span><span class="sxs-lookup"><span data-stu-id="e193a-134">Provide a download site for your codec.</span></span> <span data-ttu-id="e193a-135"> (您所提供的每個編解碼器都可以有個別的頁面，或針對所有編解碼器提供下載的單一頁面。 ) </span><span class="sxs-lookup"><span data-stu-id="e193a-135">(You can have a separate page for each codec you provide, or one page that provides downloads for all your codecs.)</span></span>

    <span data-ttu-id="e193a-136">下載網站應經過當地語系化，而且可由相機型號輕鬆搜尋。</span><span class="sxs-lookup"><span data-stu-id="e193a-136">The download site should be localized and easily searchable by camera model.</span></span>

2.  <span data-ttu-id="e193a-137">為 Microsoft 提供您影像格式的延伸模組清單，以及下載網站的 Url。</span><span class="sxs-lookup"><span data-stu-id="e193a-137">Provide Microsoft with a list of extensions for your image formats, and the URLs for your download sites.</span></span>

<span data-ttu-id="e193a-138">您必須通知 Microsoft 這些延伸模組適用于您未來開發的任何新編解碼器，以及下載網站 Url 的任何變更，以便將新的資訊新增至 Windows 影像中心。</span><span class="sxs-lookup"><span data-stu-id="e193a-138">You must inform Microsoft of the extensions for any new codecs you develop in the future, and of any changes to the URLs of your download sites, so that the new information can be added to the Windows Photo Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e193a-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="e193a-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e193a-140">**概念**</span><span class="sxs-lookup"><span data-stu-id="e193a-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e193a-141">執行 IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="e193a-141">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="e193a-142">結論 (如何撰寫 WIC-Enabled 編解碼器) </span><span class="sxs-lookup"><span data-stu-id="e193a-142">Conclusion (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[<span data-ttu-id="e193a-143">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="e193a-143">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="e193a-144">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="e193a-144">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



