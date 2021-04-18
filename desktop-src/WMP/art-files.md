---
title: 美工檔案
description: 美工檔案
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Windows Media Player 的外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 適用于面板的美工圖案，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968454"
---
# <a name="art-files"></a><span data-ttu-id="b321e-107">美工檔案</span><span class="sxs-lookup"><span data-stu-id="b321e-107">Art Files</span></span>

<span data-ttu-id="b321e-108">您必須為您的面板建立一或多個美工檔案。</span><span class="sxs-lookup"><span data-stu-id="b321e-108">You must create one or more art files for your skin.</span></span> <span data-ttu-id="b321e-109">如果沒有藝術，使用者將不會看到任何內容。</span><span class="sxs-lookup"><span data-stu-id="b321e-109">Without art, the user will have nothing to look at.</span></span> <span data-ttu-id="b321e-110">您可以建立不可見的面板，但看不到它。</span><span class="sxs-lookup"><span data-stu-id="b321e-110">You could create an invisible skin, but no one would see it!</span></span> <span data-ttu-id="b321e-111">甚至，您仍然必須建立美工檔案來保存隱藏的影像，因為面板定義檔需要特定專案的美工檔案。</span><span class="sxs-lookup"><span data-stu-id="b321e-111">And even then, you would still have to create art files to hold your invisible images, because the skin definition file requires art files for specific elements.</span></span>

<span data-ttu-id="b321e-112">在面板中有三種用途：主要影像、地圖影像和替代影像。</span><span class="sxs-lookup"><span data-stu-id="b321e-112">There are three uses for art in skins: primary images, mapping images, and alternate images.</span></span>

## <a name="primary-images"></a><span data-ttu-id="b321e-113">主要映射</span><span class="sxs-lookup"><span data-stu-id="b321e-113">Primary Images</span></span>

<span data-ttu-id="b321e-114">您必須為您的面板建立主要映射。</span><span class="sxs-lookup"><span data-stu-id="b321e-114">You must create a primary image for your skin.</span></span> <span data-ttu-id="b321e-115">這是使用者安裝面板時將看到的內容。</span><span class="sxs-lookup"><span data-stu-id="b321e-115">This is what the users will see when they install your skin.</span></span> <span data-ttu-id="b321e-116">主要映射是由特定面板控制項所建立的一或多個影像所組成。</span><span class="sxs-lookup"><span data-stu-id="b321e-116">The primary image is composed of one or more images that are created by specific skin controls.</span></span>

<span data-ttu-id="b321e-117">如果您有一個以上的控制項，您必須指定迭置順序，以定義哪些控制項會顯示在其他控制項的前方。</span><span class="sxs-lookup"><span data-stu-id="b321e-117">If you have more than one control, you must specify the z-order, which defines which controls are displayed in front of other controls.</span></span> <span data-ttu-id="b321e-118">每個 **View** 元素都會有一個背景影像，您可以將其他元素影像新增至其中，讓您建立主要複合影像。</span><span class="sxs-lookup"><span data-stu-id="b321e-118">Each **View** element will have a background image that you can add other element images to, allowing you to create a primary composite image.</span></span>

<span data-ttu-id="b321e-119">您也可能有次要影像（例如滑動紙匣）第一次出現時未顯示，但會在使用者採取某些動作時顯示。</span><span class="sxs-lookup"><span data-stu-id="b321e-119">You also may have secondary images, such as a sliding tray, that do not display when your skin first appears, but that show up when the user takes some action.</span></span> <span data-ttu-id="b321e-120">這些會遵循與主要映射相同的規則，因為它們是以一組控制項來建立。</span><span class="sxs-lookup"><span data-stu-id="b321e-120">These follow the same rules as primary images, in that they are created with a set of controls.</span></span>

## <a name="mapping-images"></a><span data-ttu-id="b321e-121">對應影像</span><span class="sxs-lookup"><span data-stu-id="b321e-121">Mapping Images</span></span>

<span data-ttu-id="b321e-122">Windows Media Player 面板最強大的功能之一，就是您可以使用影像對應來觸發面板的事件。</span><span class="sxs-lookup"><span data-stu-id="b321e-122">One of the most powerful features of Windows Media Player skins is that you can use image mapping to trigger events for your skin.</span></span> <span data-ttu-id="b321e-123">影像對應是包含特殊映射的檔案。</span><span class="sxs-lookup"><span data-stu-id="b321e-123">Image maps are files that contain special images.</span></span> <span data-ttu-id="b321e-124">不過，影像地圖檔中的影像並不是要供使用者查看，而是由 Windows Media Player 在使用者按一下您的面板時，用來執行動作。</span><span class="sxs-lookup"><span data-stu-id="b321e-124">The images in an image map file, however, are not meant to be viewed by the user, but are used by Windows Media Player to take action when the user clicks on your skin.</span></span>

<span data-ttu-id="b321e-125">不同的控制項需要不同類型的影像地圖。</span><span class="sxs-lookup"><span data-stu-id="b321e-125">Different controls need different kinds of image maps.</span></span> <span data-ttu-id="b321e-126">例如，如果您將某個影像地圖的一部分標示為特定的紅色值，而且使用者按一下主要影像的對應區域，按鈕就會引發事件。</span><span class="sxs-lookup"><span data-stu-id="b321e-126">For example, if you color part of an image map a specific red value, and the user clicks on the corresponding area of your primary image, a button will fire an event.</span></span> <span data-ttu-id="b321e-127">色彩是用來定義在面板的特定區域中按一下所觸發的事件。</span><span class="sxs-lookup"><span data-stu-id="b321e-127">Color is used to define which events are triggered by clicking in a particular area of the skin.</span></span>

## <a name="alternate-images"></a><span data-ttu-id="b321e-128">替代映射</span><span class="sxs-lookup"><span data-stu-id="b321e-128">Alternate Images</span></span>

<span data-ttu-id="b321e-129">您也可以設定當使用者執行某些工作時，要顯示的替代影像。</span><span class="sxs-lookup"><span data-stu-id="b321e-129">You can also set up alternate images to display when a user does something.</span></span> <span data-ttu-id="b321e-130">例如，您可以建立按鈕的替代影像，只有在滑鼠停留在按鈕上時才會顯示。</span><span class="sxs-lookup"><span data-stu-id="b321e-130">For example, you can create an alternate image of a button that will be displayed only when the mouse hovers over the button.</span></span> <span data-ttu-id="b321e-131">這是讓使用者知道其運作方式的好方法，也可讓使用者介面擁有高度可探索性。</span><span class="sxs-lookup"><span data-stu-id="b321e-131">This is a good way to let users know what they can do, and also allows for a highly discoverable user interface.</span></span> <span data-ttu-id="b321e-132">藉由謹慎使用工具提示和暫留影像，您可以建立不尋常的使用者介面，讓使用者有關于哪些可用選項的意見反應。</span><span class="sxs-lookup"><span data-stu-id="b321e-132">By using ToolTips and hover images carefully, you can create unusual user interfaces that still give the user feedback about what options are available.</span></span>

<span data-ttu-id="b321e-133">下列各節提供有關美工檔案的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="b321e-133">The following sections provide more information about art files:</span></span>

-   [<span data-ttu-id="b321e-134">主要映射</span><span class="sxs-lookup"><span data-stu-id="b321e-134">Primary Images</span></span>](primary-images.md)
-   [<span data-ttu-id="b321e-135">對應影像</span><span class="sxs-lookup"><span data-stu-id="b321e-135">Mapping Images</span></span>](mapping-images.md)
-   [<span data-ttu-id="b321e-136">替代映射</span><span class="sxs-lookup"><span data-stu-id="b321e-136">Alternate Images</span></span>](alternate-images.md)
-   [<span data-ttu-id="b321e-137">美工檔案格式</span><span class="sxs-lookup"><span data-stu-id="b321e-137">Art File Formats</span></span>](art-file-formats.md)
-   [<span data-ttu-id="b321e-138">簡易藝術範例</span><span class="sxs-lookup"><span data-stu-id="b321e-138">Simple Art Example</span></span>](simple-art-example.md)

## <a name="related-topics"></a><span data-ttu-id="b321e-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="b321e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b321e-140">**面板檔案**</span><span class="sxs-lookup"><span data-stu-id="b321e-140">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




