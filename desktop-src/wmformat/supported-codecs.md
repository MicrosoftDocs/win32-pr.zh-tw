---
title: 支援的編解碼器
description: 支援的編解碼器
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- Windows Media Format SDK，支援編解碼器
- Windows Media Format SDK，IWMCodecInfo3 介面
- 編解碼器，支援
- IWMCodecInfo3，關於
- 編解碼器，IWMCodecInfo3 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac06ad3d58d066254fa666f96283dca9b8b6ae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681431"
---
# <a name="supported-codecs"></a><span data-ttu-id="fbec1-108">支援的編解碼器</span><span class="sxs-lookup"><span data-stu-id="fbec1-108">Supported Codecs</span></span>

<span data-ttu-id="fbec1-109">Windows Media Format SDK 提供下列編解碼器的支援，這些編解碼器會在您安裝 SDK 時包含。</span><span class="sxs-lookup"><span data-stu-id="fbec1-109">The Windows Media Format SDK provides support for the following codecs which are included when you install the SDK.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fbec1-110">轉碼器</span><span class="sxs-lookup"><span data-stu-id="fbec1-110">Codec</span></span></th>
<th><span data-ttu-id="fbec1-111">Description</span><span class="sxs-lookup"><span data-stu-id="fbec1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fbec1-112">Windows Media 音訊</span><span class="sxs-lookup"><span data-stu-id="fbec1-112">Windows Media Audio</span></span></td>
<td><span data-ttu-id="fbec1-113">音訊編解碼器，適用于編碼複雜音訊的一般用途，像是音樂。此編解碼器的最新版本是 Windows Media 音訊9編解碼器和 Windows Media 音訊9.1 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="fbec1-113">Audio codec for general use in encoding complex audio, like music.The most recent versions of this codec are the Windows Media Audio 9 codec and the Windows Media Audio 9.1 codec.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbec1-114">Windows Media 音訊專業人員</span><span class="sxs-lookup"><span data-stu-id="fbec1-114">Windows Media Audio Professional</span></span></td>
<td><span data-ttu-id="fbec1-115">複雜音訊的音訊編解碼器，像是音樂。</span><span class="sxs-lookup"><span data-stu-id="fbec1-115">Audio codec for complex audio, like music.</span></span> <span data-ttu-id="fbec1-116">支援多重通道和24位編碼。此編解碼器有兩種版本：</span><span class="sxs-lookup"><span data-stu-id="fbec1-116">Supports multichannel and 24-bit encoding.There are two versions of this codec:</span></span><br/>
<ul>
<li><span data-ttu-id="fbec1-117">Windows Media 音訊9專業版</span><span class="sxs-lookup"><span data-stu-id="fbec1-117">Windows Media Audio 9 Professional</span></span></li>
<li><span data-ttu-id="fbec1-118">Windows Media 音訊9.1 專業版</span><span class="sxs-lookup"><span data-stu-id="fbec1-118">Windows Media Audio 9.1 Professional</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbec1-119">Windows Media 音訊無損</span><span class="sxs-lookup"><span data-stu-id="fbec1-119">Windows Media Audio Lossless</span></span></td>
<td><span data-ttu-id="fbec1-120">無失真編碼的音訊編解碼器。此編解碼器有兩種版本：</span><span class="sxs-lookup"><span data-stu-id="fbec1-120">Audio codec for lossless encoding.There are two versions of this codec:</span></span><br/>
<ul>
<li><span data-ttu-id="fbec1-121">Windows Media 音訊9無損</span><span class="sxs-lookup"><span data-stu-id="fbec1-121">Windows Media Audio 9 Lossless</span></span></li>
<li><span data-ttu-id="fbec1-122">Windows Media 音訊9.1 無損</span><span class="sxs-lookup"><span data-stu-id="fbec1-122">Windows Media Audio 9.1 Lossless</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbec1-123">Windows Media 音訊9語音</span><span class="sxs-lookup"><span data-stu-id="fbec1-123">Windows Media Audio 9 Voice</span></span></td>
<td><span data-ttu-id="fbec1-124">針對以高壓縮率編碼人類聲音而優化的音訊編解碼器。</span><span class="sxs-lookup"><span data-stu-id="fbec1-124">Audio codec optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="fbec1-125">這是最常用於串流的串流編解碼器。</span><span class="sxs-lookup"><span data-stu-id="fbec1-125">This is the preferred codec for streams consisting mostly of spoken words.</span></span> <span data-ttu-id="fbec1-126">針對混合音樂和語音的內容，此編解碼器可以動態變更用來取得最佳品質的編碼演算法。</span><span class="sxs-lookup"><span data-stu-id="fbec1-126">For content that is mixed music and speech, this codec can dynamically change the encoding algorithm used to get optimal quality.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbec1-127">Windows Media 視訊9</span><span class="sxs-lookup"><span data-stu-id="fbec1-127">Windows Media Video 9</span></span></td>
<td><span data-ttu-id="fbec1-128">適用于編碼複雜影片（例如電影）的一般使用的影片編解碼器。</span><span class="sxs-lookup"><span data-stu-id="fbec1-128">Video codec for general use in encoding complex video, such as movies.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbec1-129">Windows Media 視訊 9 Advanced Profile</span><span class="sxs-lookup"><span data-stu-id="fbec1-129">Windows Media Video 9 Advanced Profile</span></span></td>
<td><span data-ttu-id="fbec1-130">影片編解碼器包含先進的編碼功能，包括交錯編碼。</span><span class="sxs-lookup"><span data-stu-id="fbec1-130">Video codec incorporating advanced encoding features, including interlaced encoding.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbec1-131">Windows Media 視訊9螢幕</span><span class="sxs-lookup"><span data-stu-id="fbec1-131">Windows Media Video 9 Screen</span></span></td>
<td><span data-ttu-id="fbec1-132">針對編碼順序螢幕擷取畫面優化的影片編解碼器。</span><span class="sxs-lookup"><span data-stu-id="fbec1-132">Video codec optimized for encoding sequential screenshots.</span></span> <span data-ttu-id="fbec1-133">此編解碼器通常用於軟體訓練或支援，方法是使用電腦應用程式錄製監視器映射。</span><span class="sxs-lookup"><span data-stu-id="fbec1-133">This codec is often used for software training or support by recording monitor images as computer applications are used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbec1-134">Windows Media 視訊映射</span><span class="sxs-lookup"><span data-stu-id="fbec1-134">Windows Media Video Image</span></span></td>
<td><span data-ttu-id="fbec1-135">將點陣圖影像轉換成壓縮影片的影片編解碼器。此編解碼器有兩種版本：</span><span class="sxs-lookup"><span data-stu-id="fbec1-135">Video codec for converting bitmap images with deformation information into compressed video.There are two version of this codec:</span></span><br/>
<ul>
<li><span data-ttu-id="fbec1-136">Windows Media 視訊9映射</span><span class="sxs-lookup"><span data-stu-id="fbec1-136">Windows Media Video 9 Image</span></span></li>
<li><span data-ttu-id="fbec1-137">Windows Media 視訊9映射 v2</span><span class="sxs-lookup"><span data-stu-id="fbec1-137">Windows Media Video 9 Image v2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fbec1-138">您可以根據所安裝的 Windows Media 格式 SDK 版本，使用不同版本的 Windows Media 音訊和影片編解碼器進行編碼。</span><span class="sxs-lookup"><span data-stu-id="fbec1-138">Different versions of the Windows Media Audio and Video codecs are available for encoding depending on the version of the Windows Media Format SDK that you install.</span></span> <span data-ttu-id="fbec1-139">當您使用方法來列舉編解碼器和編解碼器格式的 [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) 介面時，只會列舉最新支援的版本。</span><span class="sxs-lookup"><span data-stu-id="fbec1-139">When you use the methods if the [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interface to enumerate codecs and codec formats, only the latest supported versions are enumerated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbec1-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="fbec1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbec1-141">**選擇編碼方法**</span><span class="sxs-lookup"><span data-stu-id="fbec1-141">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="fbec1-142">**編解碼器功能**</span><span class="sxs-lookup"><span data-stu-id="fbec1-142">**Codec Features**</span></span>](codec-features.md)
</dt> </dl>

 

 





