---
title: Windows Media Player 的外觀
description: Windows Media Player 的外觀
ms.assetid: 0cd23497-9a47-4391-a2c1-0e3102dcc1d2
keywords:
- Windows Media Player，外觀
- Windows Media Player 的外觀
- 外觀、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e649a3a3708a04af5c21d059c3f06b5badc815d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839815"
---
# <a name="windows-media-player-skins"></a><span data-ttu-id="ec1a4-106">Windows Media Player 的外觀</span><span class="sxs-lookup"><span data-stu-id="ec1a4-106">Windows Media Player Skins</span></span>

<span data-ttu-id="ec1a4-107">Windows Media Player 提供程式設計平臺來建立自訂的外觀。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-107">Windows Media Player provides a programming platform to create custom skins.</span></span> <span data-ttu-id="ec1a4-108">面板是腳本、藝術、媒體和文字檔的集合，可以合併以建立 Windows Media Player 的新外觀。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-108">Skins are sets of scripts, art, media, and text files that can be combined to create a new appearance for Windows Media Player.</span></span> <span data-ttu-id="ec1a4-109">您可以使用面板來變更 Windows Media Player 的外觀，但不只變更它的運作方式。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-109">Using skins, you can change not only the way Windows Media Player looks, but how it functions.</span></span> <span data-ttu-id="ec1a4-110">不只是旋鈕的位置，也不是它們看起來的樣子，而是根據基礎 Windows Media Player 核心技術的限制。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-110">Not just where the knobs are and what they look like, but what they do, given the limits of the underlying Windows Media Player core technology.</span></span>

<span data-ttu-id="ec1a4-111">外觀技術與其他類型的程式設計非常不同;基本上，您會將程式設計和美工混合在相同的部分。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-111">Skin technology is very different from other kinds of programming; essentially you will be mixing programming and art in equal parts.</span></span> <span data-ttu-id="ec1a4-112">如果您已經建立網頁並完成一些簡單的腳本) ，您也不需要是一位專家的程式設計師 (，只要您可以) 使用圖形編輯應用程式，也不需要是演出者 (。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-112">You do not need to be an expert programmer (not much more than you already know if you have created webpages and done some simple scripting), nor do you need to be an artist (as long as you can use a graphics editing application).</span></span> <span data-ttu-id="ec1a4-113">您將會使用 XML (，類似于 HTML) 、Microsoft JScript，以及您選擇的任何藝術程式。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-113">You'll be using XML (similar to HTML), Microsoft JScript, and whatever art programs you choose.</span></span>

<span data-ttu-id="ec1a4-114">面板檔案包含下列四個區段。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-114">The skins documentation contains the following four sections.</span></span>



| <span data-ttu-id="ec1a4-115">區段</span><span class="sxs-lookup"><span data-stu-id="ec1a4-115">Section</span></span>                                                                    | <span data-ttu-id="ec1a4-116">描述</span><span class="sxs-lookup"><span data-stu-id="ec1a4-116">Description</span></span>                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec1a4-117">關於外觀</span><span class="sxs-lookup"><span data-stu-id="ec1a4-117">About Skins</span></span>](about-skins.md)                                             | <span data-ttu-id="ec1a4-118">討論以抽象術語表示的外觀理論。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-118">Discusses the theory of skins in abstract terms.</span></span> <span data-ttu-id="ec1a4-119">建議您至少流覽本節，因為外觀技術與其他類型的程式設計不同。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-119">You are advised to at least browse this section because skin technology is so different from other kinds of programming.</span></span> <span data-ttu-id="ec1a4-120">本節將告訴您原因和運作方式，但只略述詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-120">This section tells you why and how things work, but only skims over the details.</span></span>                                             |
| [<span data-ttu-id="ec1a4-121">外觀建立指南</span><span class="sxs-lookup"><span data-stu-id="ec1a4-121">Skin Creation Guide</span></span>](skin-creation-guide.md)                             | <span data-ttu-id="ec1a4-122">說明建立面板的必要動作。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-122">Explains what you need to do to create a skin.</span></span> <span data-ttu-id="ec1a4-123">您可能會想要閱讀這一節，因為它涵蓋建立簡單外觀的詳細資料，以及使用特定面板元素的更複雜的外觀。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-123">You will probably want to read this section because it covers the details of creating simple skins, and then more complicated skins that use particular skin elements.</span></span> <span data-ttu-id="ec1a4-124">本節也包含建立面板所需之藝術的教學課程。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-124">This section also includes tutorials on creating the art needed to create skins.</span></span> |
| [<span data-ttu-id="ec1a4-125">外觀程式設計參考</span><span class="sxs-lookup"><span data-stu-id="ec1a4-125">Skin Programming Reference</span></span>](skin-programming-reference.md)               | <span data-ttu-id="ec1a4-126">包含面板所支援之每個元素和屬性的參考專案。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-126">Contains reference entries for every element and attribute supported by skins.</span></span> <span data-ttu-id="ec1a4-127">閱讀說明您想要使用之功能的主題。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-127">Read the topics that explain the functionality that you want to use.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="ec1a4-128">Windows Media Player 行動外觀</span><span class="sxs-lookup"><span data-stu-id="ec1a4-128">Windows Media Player Mobile Skins</span></span>](windows-media-player-mobile-skins.md) | <span data-ttu-id="ec1a4-129">提供為 Windows Media Player Mobile 建立面板的完整資訊。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-129">Provides complete information for creating skins for Windows Media Player Mobile.</span></span>                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="ec1a4-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="ec1a4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec1a4-131">**Windows Media Player SDK**</span><span class="sxs-lookup"><span data-stu-id="ec1a4-131">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




