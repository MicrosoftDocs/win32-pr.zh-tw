---
title: '具有多個值的屬性 (Windows Media Format 11 SDK) '
description: 具有多個值的屬性
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性，多個值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024440"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="13e00-107">具有多個值的屬性 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="13e00-107">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="13e00-108">某些預先定義的屬性可以有多個指派的值。</span><span class="sxs-lookup"><span data-stu-id="13e00-108">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="13e00-109">例如，「 **演出者** 」是可以有多個值的屬性。</span><span class="sxs-lookup"><span data-stu-id="13e00-109">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="13e00-110">您可以呼叫 [**IWMHeaderInfo3：： AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) 多次，以依您的需求新增多個 **演出者** 值。</span><span class="sxs-lookup"><span data-stu-id="13e00-110">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="13e00-111">如果您對不支援多個值的屬性進行多個 **AddAttribute** 呼叫，方法可能會傳回錯誤碼，或直接忽略您的要求。</span><span class="sxs-lookup"><span data-stu-id="13e00-111">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="13e00-112">下表列出支援多個值的屬性。</span><span class="sxs-lookup"><span data-stu-id="13e00-112">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="13e00-113">某些屬性只能在 ASF 檔案中有多個值，而其他屬性在 ASF 和 MP3 檔案中可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="13e00-113">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="13e00-114">屬性</span><span class="sxs-lookup"><span data-stu-id="13e00-114">Attribute</span></span>                                                 | <span data-ttu-id="13e00-115">支援多個值</span><span class="sxs-lookup"><span data-stu-id="13e00-115">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="13e00-116">**作者**</span><span class="sxs-lookup"><span data-stu-id="13e00-116">**Author**</span></span>](author.md)                                  | <span data-ttu-id="13e00-117">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="13e00-117">ASF, MP3</span></span>                    |
| [<span data-ttu-id="13e00-118">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="13e00-118">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="13e00-119">ASF</span><span class="sxs-lookup"><span data-stu-id="13e00-119">ASF</span></span>                         |
| [<span data-ttu-id="13e00-120">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="13e00-120">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="13e00-121">ASF</span><span class="sxs-lookup"><span data-stu-id="13e00-121">ASF</span></span>                         |
| [<span data-ttu-id="13e00-122">**WM/類別**</span><span class="sxs-lookup"><span data-stu-id="13e00-122">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="13e00-123">ASF</span><span class="sxs-lookup"><span data-stu-id="13e00-123">ASF</span></span>                         |
| [<span data-ttu-id="13e00-124">**WM/編輯器**</span><span class="sxs-lookup"><span data-stu-id="13e00-124">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="13e00-125">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="13e00-125">ASF, MP3</span></span>                    |
| [<span data-ttu-id="13e00-126">**WM/導體**</span><span class="sxs-lookup"><span data-stu-id="13e00-126">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="13e00-127">ASF</span><span class="sxs-lookup"><span data-stu-id="13e00-127">ASF</span></span>                         |
| [<span data-ttu-id="13e00-128">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="13e00-128">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="13e00-129">ASF</span><span class="sxs-lookup"><span data-stu-id="13e00-129">ASF</span></span>                         |
| [<span data-ttu-id="13e00-130">**WM/內容類型**</span><span class="sxs-lookup"><span data-stu-id="13e00-130">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="13e00-131">ASF</span><span class="sxs-lookup"><span data-stu-id="13e00-131">ASF</span></span>                         |
| [<span data-ttu-id="13e00-132">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="13e00-132">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="13e00-133">ASF</span><span class="sxs-lookup"><span data-stu-id="13e00-133">ASF</span></span>                         |
| [<span data-ttu-id="13e00-134">**WM/語言**</span><span class="sxs-lookup"><span data-stu-id="13e00-134">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="13e00-135">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="13e00-135">ASF, MP3</span></span>                    |
| [<span data-ttu-id="13e00-136">**WM/歌詞 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="13e00-136">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="13e00-137">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="13e00-137">ASF, MP3</span></span>                    |
| [<span data-ttu-id="13e00-138">**WM/情緒**</span><span class="sxs-lookup"><span data-stu-id="13e00-138">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="13e00-139">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="13e00-139">ASF, MP3</span></span>                    |
| [<span data-ttu-id="13e00-140">**WM/圖片**</span><span class="sxs-lookup"><span data-stu-id="13e00-140">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="13e00-141">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="13e00-141">ASF, MP3</span></span>                    |
| [<span data-ttu-id="13e00-142">**WM/生產者**</span><span class="sxs-lookup"><span data-stu-id="13e00-142">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="13e00-143">ASF</span><span class="sxs-lookup"><span data-stu-id="13e00-143">ASF</span></span>                         |
| [<span data-ttu-id="13e00-144">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="13e00-144">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="13e00-145">ASF</span><span class="sxs-lookup"><span data-stu-id="13e00-145">ASF</span></span>                         |
| [<span data-ttu-id="13e00-146">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="13e00-146">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="13e00-147">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="13e00-147">ASF, MP3</span></span>                    |
| [<span data-ttu-id="13e00-148">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="13e00-148">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="13e00-149">ASF、MP3</span><span class="sxs-lookup"><span data-stu-id="13e00-149">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="13e00-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="13e00-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13e00-151">**屬性**</span><span class="sxs-lookup"><span data-stu-id="13e00-151">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




