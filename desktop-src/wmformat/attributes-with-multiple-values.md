---
title: '具有多個值的屬性 (Windows Media Format 11 SDK) '
description: 深入瞭解 Windows Media Format 11 SDK 中具有多個值的屬性。 某些媒體專案屬性可以有多個值。
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性，多個值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262690"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="892fb-108">具有多個值的屬性 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="892fb-108">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="892fb-109">某些預先定義的屬性可以有多個指派的值。</span><span class="sxs-lookup"><span data-stu-id="892fb-109">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="892fb-110">例如，「 **演出者** 」是可以有多個值的屬性。</span><span class="sxs-lookup"><span data-stu-id="892fb-110">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="892fb-111">您可以呼叫 [**IWMHeaderInfo3：： AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) 多次，以依您的需求新增多個 **演出者** 值。</span><span class="sxs-lookup"><span data-stu-id="892fb-111">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="892fb-112">如果您對不支援多個值的屬性進行多個 **AddAttribute** 呼叫，方法可能會傳回錯誤碼，或直接忽略您的要求。</span><span class="sxs-lookup"><span data-stu-id="892fb-112">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="892fb-113">下表列出支援多個值的屬性。</span><span class="sxs-lookup"><span data-stu-id="892fb-113">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="892fb-114">某些屬性只能在 ASF 檔案中有多個值，而其他屬性在 ASF 和 MP3 檔案中可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="892fb-114">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="892fb-115">屬性</span><span class="sxs-lookup"><span data-stu-id="892fb-115">Attribute</span></span>                                                 | <span data-ttu-id="892fb-116">支援多個值</span><span class="sxs-lookup"><span data-stu-id="892fb-116">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="892fb-117">**作者**</span><span class="sxs-lookup"><span data-stu-id="892fb-117">**Author**</span></span>](author.md)                                  | <span data-ttu-id="892fb-118">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="892fb-118">ASF, MP3</span></span>                    |
| [<span data-ttu-id="892fb-119">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="892fb-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="892fb-120">ASF</span><span class="sxs-lookup"><span data-stu-id="892fb-120">ASF</span></span>                         |
| [<span data-ttu-id="892fb-121">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="892fb-121">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="892fb-122">ASF</span><span class="sxs-lookup"><span data-stu-id="892fb-122">ASF</span></span>                         |
| [<span data-ttu-id="892fb-123">**WM/類別**</span><span class="sxs-lookup"><span data-stu-id="892fb-123">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="892fb-124">ASF</span><span class="sxs-lookup"><span data-stu-id="892fb-124">ASF</span></span>                         |
| [<span data-ttu-id="892fb-125">**WM/編輯器**</span><span class="sxs-lookup"><span data-stu-id="892fb-125">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="892fb-126">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="892fb-126">ASF, MP3</span></span>                    |
| [<span data-ttu-id="892fb-127">**WM/導體**</span><span class="sxs-lookup"><span data-stu-id="892fb-127">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="892fb-128">ASF</span><span class="sxs-lookup"><span data-stu-id="892fb-128">ASF</span></span>                         |
| [<span data-ttu-id="892fb-129">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="892fb-129">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="892fb-130">ASF</span><span class="sxs-lookup"><span data-stu-id="892fb-130">ASF</span></span>                         |
| [<span data-ttu-id="892fb-131">**WM/內容類型**</span><span class="sxs-lookup"><span data-stu-id="892fb-131">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="892fb-132">ASF</span><span class="sxs-lookup"><span data-stu-id="892fb-132">ASF</span></span>                         |
| [<span data-ttu-id="892fb-133">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="892fb-133">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="892fb-134">ASF</span><span class="sxs-lookup"><span data-stu-id="892fb-134">ASF</span></span>                         |
| [<span data-ttu-id="892fb-135">**WM/語言**</span><span class="sxs-lookup"><span data-stu-id="892fb-135">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="892fb-136">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="892fb-136">ASF, MP3</span></span>                    |
| [<span data-ttu-id="892fb-137">**WM/歌詞 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="892fb-137">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="892fb-138">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="892fb-138">ASF, MP3</span></span>                    |
| [<span data-ttu-id="892fb-139">**WM/情緒**</span><span class="sxs-lookup"><span data-stu-id="892fb-139">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="892fb-140">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="892fb-140">ASF, MP3</span></span>                    |
| [<span data-ttu-id="892fb-141">**WM/圖片**</span><span class="sxs-lookup"><span data-stu-id="892fb-141">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="892fb-142">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="892fb-142">ASF, MP3</span></span>                    |
| [<span data-ttu-id="892fb-143">**WM/生產者**</span><span class="sxs-lookup"><span data-stu-id="892fb-143">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="892fb-144">ASF</span><span class="sxs-lookup"><span data-stu-id="892fb-144">ASF</span></span>                         |
| [<span data-ttu-id="892fb-145">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="892fb-145">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="892fb-146">ASF</span><span class="sxs-lookup"><span data-stu-id="892fb-146">ASF</span></span>                         |
| [<span data-ttu-id="892fb-147">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="892fb-147">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="892fb-148">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="892fb-148">ASF, MP3</span></span>                    |
| [<span data-ttu-id="892fb-149">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="892fb-149">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="892fb-150">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="892fb-150">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="892fb-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="892fb-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="892fb-152">**屬性**</span><span class="sxs-lookup"><span data-stu-id="892fb-152">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




