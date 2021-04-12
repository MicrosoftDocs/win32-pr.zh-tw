---
title: Windows Media Player SDK) 的點陣圖 (
description: 點陣圖
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Windows Media Player 行動外觀、點陣圖
- 外觀，點陣圖
- 外觀、點陣圖的參考
- 外觀中的點陣圖，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464005"
---
# <a name="bitmaps-windows-media-player-sdk"></a><span data-ttu-id="a838c-107">Windows Media Player SDK) 的點陣圖 (</span><span class="sxs-lookup"><span data-stu-id="a838c-107">Bitmaps (Windows Media Player SDK)</span></span>

<span data-ttu-id="a838c-108">您必須在面板中使用一或多個映射，而且每個影像都必須定義于面板定義檔中。</span><span class="sxs-lookup"><span data-stu-id="a838c-108">You must use one or more images in your skin, and each image must be defined in the skin definition file.</span></span> <span data-ttu-id="a838c-109">如果您未在此區段中定義影像，您的面板將無法使用它。</span><span class="sxs-lookup"><span data-stu-id="a838c-109">If you do not define an image in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="a838c-110">整個參考中都會使用「點陣圖」一詞，並使用 .bmp 副檔名、GIF 影像（副檔名為 .jpg）、JPEG 影像（副檔名為 .jpg）和 PNG 影像（副檔名為 .png）來參考點陣圖影像。</span><span class="sxs-lookup"><span data-stu-id="a838c-110">The term "bitmap" is used throughout the reference in a generic sense, and refers to bitmap images with a .bmp extension, GIF images with a .gif extension, JPEG images with a .jpg extension, and PNG images with a .png extension.</span></span>

<span data-ttu-id="a838c-111">面板定義檔的點陣圖區段開頭為以下這一行：</span><span class="sxs-lookup"><span data-stu-id="a838c-111">The Bitmaps section of the skin definition file begins with this line:</span></span>


```C++
[ Bitmaps ]

```



<span data-ttu-id="a838c-112">然後，您必須新增一或多行，其中包含面板中每個影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a838c-112">You then must add one or more lines that contain information about each of the images in your skin.</span></span>

<span data-ttu-id="a838c-113">一般的行可能是：</span><span class="sxs-lookup"><span data-stu-id="a838c-113">A typical line might be:</span></span>


```C++
    Background  Background.bmp  0,0

```



<span data-ttu-id="a838c-114">您可以使用下列範本作為面板定義檔的點陣圖區段：</span><span class="sxs-lookup"><span data-stu-id="a838c-114">You can use the following template for the Bitmaps section of your skin definition file:</span></span>


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



<span data-ttu-id="a838c-115">點陣圖區段中每一行的點陣圖資訊都必須使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="a838c-115">You must use the following order for bitmap information for each line in the Bitmap section.</span></span> <span data-ttu-id="a838c-116">這一行的每個部分都是必要的。</span><span class="sxs-lookup"><span data-stu-id="a838c-116">Each part of the line is required.</span></span>

1.  [<span data-ttu-id="a838c-117">點陣圖類型</span><span class="sxs-lookup"><span data-stu-id="a838c-117">Bitmap Type</span></span>](bitmap-type.md)
2.  [<span data-ttu-id="a838c-118">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="a838c-118">File Name</span></span>](file-name.md)
3.  [<span data-ttu-id="a838c-119">座標</span><span class="sxs-lookup"><span data-stu-id="a838c-119">Coordinates</span></span>](coordinates.md)

<span data-ttu-id="a838c-120">如需點陣圖程式碼的範例，請參閱 [範例點陣圖一節](sample-bitmap-section.md)。</span><span class="sxs-lookup"><span data-stu-id="a838c-120">For an example of bitmap code, see [Sample Bitmap Section](sample-bitmap-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a838c-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="a838c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a838c-122">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="a838c-122">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




