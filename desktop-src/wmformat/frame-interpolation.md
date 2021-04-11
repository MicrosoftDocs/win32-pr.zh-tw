---
title: 框架插補
description: 框架插補
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media Format SDK，框架插補
- 編解碼器，框架插補
- 框架插補
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023044"
---
# <a name="frame-interpolation"></a><span data-ttu-id="3b0e4-106">框架插補</span><span class="sxs-lookup"><span data-stu-id="3b0e4-106">Frame Interpolation</span></span>

<span data-ttu-id="3b0e4-107">框架插補是以兩個連續的編碼影片框架中的資料為基礎建立中繼影片框架的程式。</span><span class="sxs-lookup"><span data-stu-id="3b0e4-107">Frame interpolation is the process of creating intermediate video frames based on the data in two consecutive frames of encoded video.</span></span> <span data-ttu-id="3b0e4-108">實際上，框架插補會在解碼時，增加編碼影片的 [*畫面播放速率*](wmformat-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="3b0e4-108">In effect, frame interpolation increases the [*frame rate*](wmformat-glossary.md) of encoded video at the time of decoding.</span></span> <span data-ttu-id="3b0e4-109">您可以使用畫面格插補來改善以較低畫面播放速率播放影片的平滑。</span><span class="sxs-lookup"><span data-stu-id="3b0e4-109">You can use frame interpolation to improve the smoothness of playback for video streams with low frame rates.</span></span>

<span data-ttu-id="3b0e4-110">因為這是解碼功能，所以它不會牽涉到任何特殊的編碼選項，也不會增加內容的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="3b0e4-110">Because this is a decoding feature, it does not involve any special encoding options and adds no overhead to the content.</span></span> <span data-ttu-id="3b0e4-111">框架插補會指定為讀取器物件中的輸出設定。</span><span class="sxs-lookup"><span data-stu-id="3b0e4-111">Frame interpolation is specified as an output setting in the reader object.</span></span>

<span data-ttu-id="3b0e4-112">只有 Windows Media 視訊9編解碼器支援框架插補。</span><span class="sxs-lookup"><span data-stu-id="3b0e4-112">Only the Windows Media Video 9 codec supports frame interpolation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b0e4-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b0e4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b0e4-114">**編解碼器功能**</span><span class="sxs-lookup"><span data-stu-id="3b0e4-114">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="3b0e4-115">**IWMReaderAdvanced2::SetOutputSetting**</span><span class="sxs-lookup"><span data-stu-id="3b0e4-115">**IWMReaderAdvanced2::SetOutputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[<span data-ttu-id="3b0e4-116">**輸出設定**</span><span class="sxs-lookup"><span data-stu-id="3b0e4-116">**Output Settings**</span></span>](output-settings.md)
</dt> </dl>

 

 




