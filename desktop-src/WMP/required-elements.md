---
title: 必要元素
description: 必要元素
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Windows Media Player 行動外觀、元素
- 外觀，元素
- 外觀定義檔，元素
- 元素、外觀定義檔
- Windows Media Player Mobile 的元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673451"
---
# <a name="required-elements"></a><span data-ttu-id="1f718-108">必要元素</span><span class="sxs-lookup"><span data-stu-id="1f718-108">Required Elements</span></span>

<span data-ttu-id="1f718-109">您必須在您的外觀定義檔中提供下列元素：</span><span class="sxs-lookup"><span data-stu-id="1f718-109">You must provide the following elements in your skin definition file:</span></span>

-   <span data-ttu-id="1f718-110">**頭。**</span><span class="sxs-lookup"><span data-stu-id="1f718-110">**Header.**</span></span> <span data-ttu-id="1f718-111">需要主要的外觀定義檔案標頭。</span><span class="sxs-lookup"><span data-stu-id="1f718-111">The main skin definition file header is required.</span></span> <span data-ttu-id="1f718-112">如需標頭版本資訊，請參閱 [建立面板定義](creating-a-skin-definition-file.md) 檔一節中的表格。</span><span class="sxs-lookup"><span data-stu-id="1f718-112">For header version information, see the table in the [Creating a Skin Definition File](creating-a-skin-definition-file.md) section.</span></span>
-   <span data-ttu-id="1f718-113">**描述區段。**</span><span class="sxs-lookup"><span data-stu-id="1f718-113">**Description section.**</span></span> <span data-ttu-id="1f718-114">建立適用于 Windows Mobile 的 Windows Media Player 9 系列的面板時，需要描述區段。</span><span class="sxs-lookup"><span data-stu-id="1f718-114">The Description section is required when creating skins for Windows Media Player 9 Series for Windows Mobile.</span></span> <span data-ttu-id="1f718-115">它必須是面板定義檔中的第一個區段，而且必須為維度指定有效的值。</span><span class="sxs-lookup"><span data-stu-id="1f718-115">It must be the first section in the skin definition file, and it must specify valid values for Dimensions.</span></span> <span data-ttu-id="1f718-116">您可以選擇是否要指定方向的值。</span><span class="sxs-lookup"><span data-stu-id="1f718-116">Specifying a value for Orientation is optional.</span></span>
-   <span data-ttu-id="1f718-117">**點陣圖區段。**</span><span class="sxs-lookup"><span data-stu-id="1f718-117">**Bitmaps section.**</span></span> <span data-ttu-id="1f718-118">需要點陣圖區段。</span><span class="sxs-lookup"><span data-stu-id="1f718-118">The Bitmaps section is required.</span></span> <span data-ttu-id="1f718-119">此外，點陣圖區段必須指定背景、停用、推送、區域和超級影像檔案的有效名稱。</span><span class="sxs-lookup"><span data-stu-id="1f718-119">Additionally, the Bitmaps section must specify valid names for Background, Disabled, Pushed, Region, and Super image files.</span></span>
-   <span data-ttu-id="1f718-120">**影像檔。**</span><span class="sxs-lookup"><span data-stu-id="1f718-120">**Image files.**</span></span> <span data-ttu-id="1f718-121">您必須提供背景、停用、推送、區域和超級影像檔案作為面板的一部分。</span><span class="sxs-lookup"><span data-stu-id="1f718-121">You must provide Background, Disabled, Pushed, Region, and Super image files as part of your skin.</span></span> <span data-ttu-id="1f718-122">如果您要建立 Windows Media Player 10 行動裝置版或更新版本的面板，則不需要包含區域或超級影像檔案。</span><span class="sxs-lookup"><span data-stu-id="1f718-122">If you are creating skins for Windows Media Player 10 Mobile or later, you do not need to include Region or Super image files.</span></span>

<span data-ttu-id="1f718-123">如果您建立只定義影像的面板，則會顯示該面板，但不會對使用者提供任何有意義的功能。</span><span class="sxs-lookup"><span data-stu-id="1f718-123">If you create a skin with only images defined, the skin will be visible, but will not offer any meaningful functionality to the user.</span></span> <span data-ttu-id="1f718-124">如果您決定建立沒有按鈕的面板，或許是為了防止使用者略過某些內容，請注意，您仍然可以將功能對應至裝置上的硬體按鈕。</span><span class="sxs-lookup"><span data-stu-id="1f718-124">If you decide to create a skin without buttons, perhaps to prevent the user from skipping over certain content, be aware that it may still be possible to map functionality to the hardware buttons on the device.</span></span>

<span data-ttu-id="1f718-125">需要 Thumb 檔案，而且您的 trackbars 不能使用。</span><span class="sxs-lookup"><span data-stu-id="1f718-125">Thumb files are required and your trackbars cannot be used without thumbs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f718-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f718-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f718-127">**外觀定義檔**</span><span class="sxs-lookup"><span data-stu-id="1f718-127">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 




