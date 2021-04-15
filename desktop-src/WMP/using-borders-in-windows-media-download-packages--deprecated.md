---
title: '在 Windows Media 下載套件中使用框線 (已淘汰) '
description: '在 Windows Media 下載套件中使用框線 (已淘汰) '
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Windows Media 中繼檔，Windows Media 下載套件
- Windows Media Player，Windows Media 下載套件
- 中繼檔，Windows Media 下載套件
- Windows Media、Windows Media 下載套件
- 框線，關於
- Windows Media 下載套件、框線
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372279"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="f38c1-109">在 Windows Media 下載套件中使用框線 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="f38c1-109">Using Borders in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="f38c1-110">本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="f38c1-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="f38c1-111">框線可讓您為已封裝的內容建立自訂的圖形化使用者介面。</span><span class="sxs-lookup"><span data-stu-id="f38c1-111">Borders enable you to create a customized graphical user interface for your packaged content.</span></span> <span data-ttu-id="f38c1-112">框線可以包含影像、互動式控制項和網站的連結等元素。</span><span class="sxs-lookup"><span data-stu-id="f38c1-112">The border can include elements such as images, interactive controls, and links to websites.</span></span> <span data-ttu-id="f38c1-113">如果您想要在已封裝的內容中新增額外的值（例如商標或廣告），您可以使用框線。</span><span class="sxs-lookup"><span data-stu-id="f38c1-113">You can use borders in cases where you want to add additional value to your packaged content, such as for branding or advertising.</span></span> <span data-ttu-id="f38c1-114">當使用者下載並開啟您的 Windows Media 下載套件之後，Windows Media Player 會在播放封裝的內容時自動顯示您的自訂框線。</span><span class="sxs-lookup"><span data-stu-id="f38c1-114">After users download and open your Windows Media Download package, Windows Media Player automatically displays your custom border when it plays the packaged content.</span></span>

<span data-ttu-id="f38c1-115">不同于能讓使用者完全取代 Windows Media Player 使用者介面的面板，只會在完整模式播放程式的 [ **現正播放** ] 窗格中顯示框線。</span><span class="sxs-lookup"><span data-stu-id="f38c1-115">Unlike a skin, which enables users to completely replace the Windows Media Player user interface, a border is displayed only in the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="f38c1-116">不過，您用來建立面板的相同工具和技術也會用來建立框線。</span><span class="sxs-lookup"><span data-stu-id="f38c1-116">However, the same tools and technologies that you use to create skins are also used to create borders.</span></span> <span data-ttu-id="f38c1-117">下圖顯示框線。</span><span class="sxs-lookup"><span data-stu-id="f38c1-117">The following illustration shows a border.</span></span>

![顯示的框線 windows media player 10](images/border-v10.png)

<span data-ttu-id="f38c1-119">在嘗試建立框線之前，請務必瞭解建立面板的基本技巧。</span><span class="sxs-lookup"><span data-stu-id="f38c1-119">It is important to understand the basic techniques for creating a skin before attempting to create a border.</span></span> <span data-ttu-id="f38c1-120">您可以使用兩種程式設計語言來完成框執行緒序設計：可延伸標記語言 (XML)  (XML) 和 Microsoft JScript。</span><span class="sxs-lookup"><span data-stu-id="f38c1-120">Border programming is accomplished using two programming languages: Extensible Markup Language (XML) and Microsoft JScript.</span></span> <span data-ttu-id="f38c1-121">XML 是用來定義介面元素，例如按鈕、滑杆和文字方塊。</span><span class="sxs-lookup"><span data-stu-id="f38c1-121">XML is used to define interface elements such as buttons, sliders, and text boxes.</span></span> <span data-ttu-id="f38c1-122">您不需要瞭解 XML 的所有詳細資料，因為您不需要撰寫新的 XML 程式碼元素;您可以直接使用 Windows Media Player 所提供的專案。</span><span class="sxs-lookup"><span data-stu-id="f38c1-122">You don't need to understand all the details of XML since you don't have to write new XML code elements; you can simply use the ones provided by Windows Media Player.</span></span> <span data-ttu-id="f38c1-123">雖然建立框線不需要 JScript，但它可以用來提供額外的功能。</span><span class="sxs-lookup"><span data-stu-id="f38c1-123">Although JScript is not required for creating borders, it can be used to provide additional functionality.</span></span>

<span data-ttu-id="f38c1-124">副檔名為 wmz 的壓縮框線檔包含具有 wms 副檔名的框線定義檔，以及框線內使用的所有影像檔案。</span><span class="sxs-lookup"><span data-stu-id="f38c1-124">A compressed border file with a .wmz file name extension includes a border definition file with a .wms file name extension and all the image files used within the border.</span></span>

<span data-ttu-id="f38c1-125">若要在 Windows Media 下載套件中包含框線，只要建立框線，並在 Windows Media 中繼檔播放清單中參考該框線即可。</span><span class="sxs-lookup"><span data-stu-id="f38c1-125">To include a border in a Windows Media Download package, simply create a border and reference that border in a Windows Media metafile playlist.</span></span> <span data-ttu-id="f38c1-126">當播放程式剖析中繼檔並解讀參考框線的 **外觀** 專案之後，就會將 border 檔案載入 Windows Media Player 中。</span><span class="sxs-lookup"><span data-stu-id="f38c1-126">The border file is loaded into Windows Media Player after the Player parses the metafile and interprets the **SKIN** element that references the border.</span></span> <span data-ttu-id="f38c1-127">面板 **元素僅** 用於框線，而面板元素的 HREF 屬性只能參考每個套件的一個外觀。</span><span class="sxs-lookup"><span data-stu-id="f38c1-127">The **SKIN** element is used only for borders, and the HREF attribute of the **SKIN** element can reference only one skin for each package.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f38c1-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="f38c1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f38c1-129">**Windows Media Player (已淘汰) 的框線**</span><span class="sxs-lookup"><span data-stu-id="f38c1-129">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="f38c1-130">**(淘汰的 Windows Media 下載套件)**</span><span class="sxs-lookup"><span data-stu-id="f38c1-130">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="f38c1-131">**Windows Media Player 的外觀**</span><span class="sxs-lookup"><span data-stu-id="f38c1-131">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




