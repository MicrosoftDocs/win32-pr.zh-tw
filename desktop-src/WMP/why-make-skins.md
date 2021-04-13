---
title: 為何要建立外觀
description: 為何要建立外觀
ms.assetid: 7aca14a3-5fd8-4244-b023-fa21a76e00fc
keywords:
- Windows Media Player，外觀
- Windows Media Player 的外觀、用途
- 外觀、用途
- Windows Media Player 的外觀範例
- 外觀，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2df762857b34edc91969b7f58eb294a10fbbcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301312"
---
# <a name="why-make-skins"></a><span data-ttu-id="f063a-108">為何要建立外觀？</span><span class="sxs-lookup"><span data-stu-id="f063a-108">Why Make Skins?</span></span>

<span data-ttu-id="f063a-109">當有人在圖形化運算環境（例如 Microsoft Windows）中使用程式時，使用者互動的視覺元件會構成使用者介面。</span><span class="sxs-lookup"><span data-stu-id="f063a-109">When someone uses a program in a graphical computing environment such as Microsoft Windows, the visual components with which the user interacts make up the user interface.</span></span> <span data-ttu-id="f063a-110">Microsoft Windows 的目的之一是提供標準使用者介面，讓所有程式都能以類似、熟悉的方式運作。</span><span class="sxs-lookup"><span data-stu-id="f063a-110">One of the purposes of Microsoft Windows is to provide a standard user interface so that all programs will operate in a similar, familiar way.</span></span> <span data-ttu-id="f063a-111">例如，Microsoft 建議您在 Microsoft Windows 使用者體驗中，每個程式都在程式主視窗的右上角提供 [ **關閉** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f063a-111">For example, Microsoft recommends, in the Microsoft Windows User Experience, that every program provide a **Close** button in the upper-right corner of the main window of the program.</span></span>

<span data-ttu-id="f063a-112">Windows Media Player 提供建立您自己的使用者介面的功能。</span><span class="sxs-lookup"><span data-stu-id="f063a-112">Windows Media Player provides the capabilities for creating your own user interface.</span></span> <span data-ttu-id="f063a-113">如果您想要將 [ **關閉** ] 按鈕放在畫面中間，可以這麼做。</span><span class="sxs-lookup"><span data-stu-id="f063a-113">If you want to put the **Close** button in the middle of the screen, you can do that.</span></span> <span data-ttu-id="f063a-114">您可能不喜歡 [ **關閉** ] 按鈕的外觀 (看起來像是方塊內的 X) ;如果您想要讓它看起來像是 skull 和 crossbones，您可以建立一個使用者介面，其中的 [ **關閉** ] 按鈕就是這樣！</span><span class="sxs-lookup"><span data-stu-id="f063a-114">Perhaps you do not like the way the **Close** button looks (it looks like an X inside a box); if you want it to look like a skull and crossbones, you can make a user interface where the **Close** button is just that!</span></span> <span data-ttu-id="f063a-115">Windows Media Player 提供您建立自訂使用者介面來播放音樂和影片所需的所有工具：按鈕、滑杆列、影片視窗、視覺效果視窗、均衡列等等。</span><span class="sxs-lookup"><span data-stu-id="f063a-115">Windows Media Player gives you all the tools you need to make a custom user interface for playing music and video: buttons, slider bars, video windows, visualization windows, equalization bars, and so on.</span></span>

<span data-ttu-id="f063a-116">您可能會想要為 Windows Media Player 建立自己的使用者介面，有幾個很好的原因。</span><span class="sxs-lookup"><span data-stu-id="f063a-116">There are several good reasons why you might want to create your own user interface for Windows Media Player.</span></span> <span data-ttu-id="f063a-117">其中一個原因是您可能會想要新增尚未存在 Windows Media Player 中的功能。</span><span class="sxs-lookup"><span data-stu-id="f063a-117">One reason is that you might want to add functionality that is not already in Windows Media Player.</span></span> <span data-ttu-id="f063a-118">例如，您可能會想要建立播放程式，以根據一天的時間播放播放清單中的音樂，讓您在早上樂觀，以及晚上減緩的爵士樂。</span><span class="sxs-lookup"><span data-stu-id="f063a-118">For example, you might want to create a player that plays music from playlists that are based on the time of day, so that you have upbeat rock in the morning and slow jazz in the evening.</span></span> <span data-ttu-id="f063a-119">或者，您可能想要讓面板變成有很大的紅色按鈕，以快速停止音樂。</span><span class="sxs-lookup"><span data-stu-id="f063a-119">Or perhaps you want to make a skin with a big red button that will stop the music quickly.</span></span> <span data-ttu-id="f063a-120">Windows Media Player 並沒有「立即播放相同的歌曲，直到我的室友變得很奇怪」按鈕，但如果您想要的話，也可以建立它。</span><span class="sxs-lookup"><span data-stu-id="f063a-120">Windows Media Player does not come with a "play the same song over and over again until my roommate goes crazy" button, but if you want one, you can create it.</span></span>

<span data-ttu-id="f063a-121">建立面板的另一個原因是要進行 Windows Media Player 的品牌化尋找。</span><span class="sxs-lookup"><span data-stu-id="f063a-121">Another reason for creating a skin is to make a branded look for Windows Media Player.</span></span> <span data-ttu-id="f063a-122">如果您是從網站發佈音樂並使用特定的標誌，您可能會想要設計一個使用您標誌的面板，以提醒他人您的網站。</span><span class="sxs-lookup"><span data-stu-id="f063a-122">If you are distributing music from your website and use a particular logo, you might want to design a skin that uses your logo to remind people about your site.</span></span> <span data-ttu-id="f063a-123">如果您有一個岩石區，您可以在其上建立具有您寬線圖片的外觀。</span><span class="sxs-lookup"><span data-stu-id="f063a-123">If you have a rock band, you can make a skin with pictures of your band on it.</span></span>

<span data-ttu-id="f063a-124">另外還有一個原因，就是要讓它成為可裝飾桌面的唯一東西。</span><span class="sxs-lookup"><span data-stu-id="f063a-124">And another reason to make skins is to make something unique that can dress up your desktop.</span></span> <span data-ttu-id="f063a-125">當您的朋友回頭詢問您的畫面上的酷炫程式時，您可以自行製作。</span><span class="sxs-lookup"><span data-stu-id="f063a-125">When your friends come over and ask you what that cool program on your screen is, you can say you made it yourself.</span></span> <span data-ttu-id="f063a-126">您甚至可以拍攝狗的圖片、將它掃描到電腦上、新增一些按鈕，以及建立一個面板，在其中按一下狗的鼻子開始播放音樂，然後按一下 tail 來停止它。</span><span class="sxs-lookup"><span data-stu-id="f063a-126">You can even take a picture of your dog, scan it into your computer, add some buttons, and create a skin in which clicking on your dog's nose starts the music and clicking on the tail stops it.</span></span> <span data-ttu-id="f063a-127">您可以針對不同類型的音樂建立不同的外觀，也可以針對每一周的每一天使用不同的面板。</span><span class="sxs-lookup"><span data-stu-id="f063a-127">You can create different skins for different kinds of music or have a different skin for every day of the week.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f063a-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="f063a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f063a-129">**關於外觀**</span><span class="sxs-lookup"><span data-stu-id="f063a-129">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




