---
title: 關於 (Mobile) 的外觀
description: 瞭解行動裝置播放機的外觀。 面板是 Windows Media Player 的自訂使用者介面。
ms.assetid: 105c11ce-705b-4a0c-8982-d0f9dd9ae3ac
keywords:
- Windows Media Player 行動裝置、外觀
- Windows Media Player 行動外觀
- Windows Media Player 行動外觀，建立
- Windows Media Player 行動裝置的外觀
- 建立外觀 Windows Media Player 行動裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdffdc4075456c6cb7ccf9d1940c5253c732cd3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011221"
---
# <a name="about-skins-mobile"></a><span data-ttu-id="a0f9a-109">關於 (Mobile) 的外觀</span><span class="sxs-lookup"><span data-stu-id="a0f9a-109">About Skins (Mobile)</span></span>

<span data-ttu-id="a0f9a-110">面板是 Windows Media Player 的自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-110">A skin is a customized user interface to Windows Media Player.</span></span> <span data-ttu-id="a0f9a-111">您可以建立自己的按鈕來開始和停止播放數位媒體、新增滑杆來變更媒體專案中的音量和播放位置，以及為使用者提供文字資訊，例如歌曲的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-111">You can create your own buttons to start and stop playback of digital media, add sliders to change volume and playback position in the media item, and provide the user with text information such as the name of a song.</span></span> <span data-ttu-id="a0f9a-112">最棒的是，您可以新增自己的作品，或使用現有的藝術來為您的外觀建立獨特的外觀。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-112">Best of all, you can add your own artwork or use existing art to create a unique appearance for your skin.</span></span>

<span data-ttu-id="a0f9a-113">建立面板的基本步驟如下：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-113">The basic steps in creating a skin are:</span></span>

1.  <span data-ttu-id="a0f9a-114">**設計** 您的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-114">**Design** your user interface.</span></span> <span data-ttu-id="a0f9a-115">決定您想要提供給使用者的按鈕、文字方塊和 trackbars，讓他們可以控制您在步驟1中選擇的功能。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-115">Decide which buttons, text boxes, and trackbars you want to provide to the user so that they can control the functions you chose in step 1.</span></span> <span data-ttu-id="a0f9a-116">您可能會想要草擬您的想法，以瞭解它們如何符合您將使用的影像大小。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-116">You may want to sketch out your ideas to see how they fit on the image size you will be working with.</span></span>
2.  <span data-ttu-id="a0f9a-117">**建立** 您想要顯示使用者的圖片。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-117">**Create** the art you want to show the user.</span></span> <span data-ttu-id="a0f9a-118">這會包含數個影像，其中顯示背景影像、您可能想要顯示的其他影像，以及使用 [區域] 按鈕時的地圖影像。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-118">This will consist of several images that show the background images, other images you may want to display, and mapping images if you use region buttons.</span></span>
3.  <span data-ttu-id="a0f9a-119">**撰寫** 會將數位媒體功能、使用者介面和影像連結在一起的面板定義檔。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-119">**Write** the skin definition file that will link together the digital media functions, user interface, and images.</span></span> <span data-ttu-id="a0f9a-120">您必須遵循特定的規則，將文字資料輸入檔案，但您可以查看預設的面板作為指南。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-120">You must follow certain rules for entering the text data into the file, but you can look at the default skin as a guide.</span></span>

<span data-ttu-id="a0f9a-121">您不需要依照指定的順序遵循這些步驟，但有一個良好的設計，就是要注意所有的可能性，並負責處理所有細節。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-121">You do not need to follow these steps in the order given, but a good design will come from being aware of all the possibilities and taking care of all the details.</span></span>

<span data-ttu-id="a0f9a-122">下列各節提供有關外觀的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-122">The following sections provide detailed information about skins.</span></span>



| <span data-ttu-id="a0f9a-123">區段</span><span class="sxs-lookup"><span data-stu-id="a0f9a-123">Section</span></span>                                                                                    | <span data-ttu-id="a0f9a-124">描述</span><span class="sxs-lookup"><span data-stu-id="a0f9a-124">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0f9a-125">關於相容性</span><span class="sxs-lookup"><span data-stu-id="a0f9a-125">About Compatibility</span></span>](about-compatibility.md)                                             | <span data-ttu-id="a0f9a-126">列出不同版本的 Windows Media Player 行動裝置、硬體需求、Windows Media Player 可用性，以及針對每個軟體版本引進的外觀功能。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-126">Lists the different versions of Windows Media Player Mobile, the hardware requirements, availability of Windows Media Player, and the skin features introduced for each version of the software.</span></span> |
| [<span data-ttu-id="a0f9a-127">Windows Media Player 行動功能</span><span class="sxs-lookup"><span data-stu-id="a0f9a-127">Windows Media Player Mobile Functionality</span></span>](windows-media-player-mobile-functionality.md) | <span data-ttu-id="a0f9a-128">描述您的外觀可以支援的功能。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-128">Describes the features your skin can support.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="a0f9a-129">消費者介面元素</span><span class="sxs-lookup"><span data-stu-id="a0f9a-129">User Interface Elements</span></span>](user-interface-elements.md)                                     | <span data-ttu-id="a0f9a-130">描述您可以為面板建立的使用者介面元素，例如按鈕、trackbars 和影片顯示。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-130">Describes the user interface elements you can create for your skin, such as buttons, trackbars, and video displays.</span></span>                                                                              |
| [<span data-ttu-id="a0f9a-131">美工檔案</span><span class="sxs-lookup"><span data-stu-id="a0f9a-131">Art Files</span></span>](art-files-mobile.md)                                                          | <span data-ttu-id="a0f9a-132">描述您為面板建立的美工檔案。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-132">Describes the art files you create for your skin.</span></span>                                                                                                                                                |
| [<span data-ttu-id="a0f9a-133">外觀定義檔</span><span class="sxs-lookup"><span data-stu-id="a0f9a-133">Skin Definition File</span></span>](skin-definition-file-mobile.md)                                    | <span data-ttu-id="a0f9a-134">描述您必須建立的檔案，以描述您的外觀。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-134">Describes the file you must create to describe your skin.</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="a0f9a-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0f9a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f9a-136">**Windows Media Player 行動外觀**</span><span class="sxs-lookup"><span data-stu-id="a0f9a-136">**Windows Media Player Mobile Skins**</span></span>](windows-media-player-mobile-skins.md)
</dt> </dl>

 

 




