---
title: 從編解碼器取得串流設定資訊
description: 從編解碼器取得串流設定資訊
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- 串流，來自編解碼器的設定
- 編解碼器，取得串流設定
- 資料流程、編解碼器格式
- 編解碼器，格式
- 資料流程，IWMCodecInfo 介面
- IWMCodecInfo，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104374769"
---
# <a name="getting-stream-configuration-information-from-codecs"></a><span data-ttu-id="0f252-109">從編解碼器取得串流設定資訊</span><span class="sxs-lookup"><span data-stu-id="0f252-109">Getting Stream Configuration Information from Codecs</span></span>

<span data-ttu-id="0f252-110">針對使用 Windows Media 音訊和影片編解碼器的音訊和影片串流，您應該從您想要使用的編解碼器取得串流設定結構的值。</span><span class="sxs-lookup"><span data-stu-id="0f252-110">For audio and video streams that use the Windows Media Audio and Video codecs, you should get the values for the stream configuration structures from the codec you want to use.</span></span> <span data-ttu-id="0f252-111">雖然您可以自行設定這些值，但使用編解碼器可確保這些值是正確的。</span><span class="sxs-lookup"><span data-stu-id="0f252-111">While it is possible to set these values yourself, using the codecs ensures that the values are accurate.</span></span> <span data-ttu-id="0f252-112">除非檔特別建議特定的變更，否則您不應該改變這些結構中的值。</span><span class="sxs-lookup"><span data-stu-id="0f252-112">You should not alter the values in these structures unless the documentation specifically recommends a particular change.</span></span>

<span data-ttu-id="0f252-113">編解碼器的資訊採用編解碼器格式的形式。</span><span class="sxs-lookup"><span data-stu-id="0f252-113">Information from the codecs comes in the form of codec formats.</span></span> <span data-ttu-id="0f252-114">每個編解碼器格式都是編解碼器支援的單一資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="0f252-114">Each codec format is a single stream format supported by the codec.</span></span> <span data-ttu-id="0f252-115">如需資料流程格式的詳細資訊，請參閱 [格式](formats.md)。</span><span class="sxs-lookup"><span data-stu-id="0f252-115">For more information about stream formats, see [Formats](formats.md).</span></span>

<span data-ttu-id="0f252-116">您可以使用配置檔案管理員物件的 [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)、 [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)和 [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) 介面，從 Windows Media 編解碼器要求資訊。</span><span class="sxs-lookup"><span data-stu-id="0f252-116">You can request information from the Windows Media codecs using the [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2), and [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interfaces of the profile manager object.</span></span> <span data-ttu-id="0f252-117">若要取得配置檔案管理員物件的 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面，請呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數。</span><span class="sxs-lookup"><span data-stu-id="0f252-117">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="0f252-118">在 **IWMProfileManager** 上呼叫 **QueryInterface** 以取得 **IWMCodecInfo3**。</span><span class="sxs-lookup"><span data-stu-id="0f252-118">Call **QueryInterface** on **IWMProfileManager** to get **IWMCodecInfo3**.</span></span>

<span data-ttu-id="0f252-119">下列各節將說明如何取得您需要的資訊。</span><span class="sxs-lookup"><span data-stu-id="0f252-119">The following sections describe how to get the information you need.</span></span>



| <span data-ttu-id="0f252-120">區段</span><span class="sxs-lookup"><span data-stu-id="0f252-120">Section</span></span>                                                                                                | <span data-ttu-id="0f252-121">描述</span><span class="sxs-lookup"><span data-stu-id="0f252-121">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f252-122">列舉所有已安裝的 Windows Media 編解碼器</span><span class="sxs-lookup"><span data-stu-id="0f252-122">To Enumerate All Installed Windows Media Codecs</span></span>](to-enumerate-all-installed-windows-media-codecs.md) | <span data-ttu-id="0f252-123">說明如何使用 **IWMCodecInfo** 和 **IWMCodecInfo2** 介面的方法，以抓取每個已安裝 Windows Media 編解碼器的名稱和編解碼器索引。</span><span class="sxs-lookup"><span data-stu-id="0f252-123">Describes how to use the methods of the **IWMCodecInfo** and **IWMCodecInfo2** interfaces to retrieve the name and codec index of each Windows Media codec installed.</span></span> |
| [<span data-ttu-id="0f252-124">列舉編解碼器格式</span><span class="sxs-lookup"><span data-stu-id="0f252-124">To Enumerate Codec Formats</span></span>](to-enumerate-codec-formats.md)                                           | <span data-ttu-id="0f252-125">說明如何從編解碼器取得串流設定物件，以便在您的設定檔中使用。</span><span class="sxs-lookup"><span data-stu-id="0f252-125">Describes how to get stream configuration objects from codecs for use in your profiles.</span></span>                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0f252-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f252-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f252-127">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="0f252-127">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




