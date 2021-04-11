---
description: 在 Direct3D 中，所有二維 (2D) 影像都是由稱為 surface 的線性範圍記憶體表示。
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: " (Direct3D 9) 的表面格式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109376"
---
# <a name="surface-formats-direct3d-9"></a><span data-ttu-id="b7139-103"> (Direct3D 9) 的表面格式</span><span class="sxs-lookup"><span data-stu-id="b7139-103">Surface Formats (Direct3D 9)</span></span>

<span data-ttu-id="b7139-104">在 Direct3D 中，所有二維 (2D) 影像都是由稱為 surface 的線性範圍記憶體表示。</span><span class="sxs-lookup"><span data-stu-id="b7139-104">In Direct3D, all two-dimensional (2D) images are represented by a linear range of memory called a surface.</span></span> <span data-ttu-id="b7139-105">您可以將介面視為2D 陣列，其中每個專案都有一個代表影像小型區段的色彩值，稱為圖元。</span><span class="sxs-lookup"><span data-stu-id="b7139-105">A surface can be thought of as a 2D array where each element holds a color value representing a small section of the image, called a pixel.</span></span> <span data-ttu-id="b7139-106">影像的詳細層級是由代表影像所需的圖元數，以及影像的色頻所需的位數來定義。</span><span class="sxs-lookup"><span data-stu-id="b7139-106">An image's detail level is defined by both the number of pixels needed to represent the image, and the number of bits needed for the image's color spectrum.</span></span> <span data-ttu-id="b7139-107">例如，以800圖元寬、600圖元高，且每個 (圖元的32位（以 800x600x32) 撰寫）的影像，將會比以 640x480x16) 撰寫的每個 (圖元的480圖元高度為640圖元的影像更詳細。</span><span class="sxs-lookup"><span data-stu-id="b7139-107">For example, an image that is 800 pixels wide by 600 pixels high with 32 bits of color for each pixel (written as 800x600x32) will be more detailed than an image that is 640 pixels wide by 480 pixels tall with 16 bits of color for each pixel (written as 640x480x16).</span></span> <span data-ttu-id="b7139-108">同樣地，更詳細的影像也需要較大的介面來儲存資料。</span><span class="sxs-lookup"><span data-stu-id="b7139-108">Likewise, the more detailed image will require a larger surface to store the data.</span></span> <span data-ttu-id="b7139-109">針對800x600x32 影像，介面的陣列維度將會是800x600，而且每個元素都會保存32位值以代表其色彩。</span><span class="sxs-lookup"><span data-stu-id="b7139-109">For an 800x600x32 image, the surface's array dimensions will be 800x600, and each element will hold a 32-bit value to represent its color.</span></span>

<span data-ttu-id="b7139-110">所有表面都有大小，並且會儲存代表色彩的特定位數。</span><span class="sxs-lookup"><span data-stu-id="b7139-110">All surfaces have a size and store a specific number of bits that represent color.</span></span> <span data-ttu-id="b7139-111">代表色彩的位會分成個別的色彩元素：紅色、綠色和藍色。</span><span class="sxs-lookup"><span data-stu-id="b7139-111">The bits that represent color are separated into individual color elements: red, green, and blue.</span></span> <span data-ttu-id="b7139-112">在 Direct3D 中，所有色彩元素都是由 [D3DFORMAT](d3dformat.md) 列舉型別定義。</span><span class="sxs-lookup"><span data-stu-id="b7139-112">In Direct3D all color elements are defined by the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="b7139-113">Direct3D 色彩格式會細分為每個色彩所保留的 byes 數目。</span><span class="sxs-lookup"><span data-stu-id="b7139-113">A Direct3D color format is broken down into the number of byes reserved for each color.</span></span> <span data-ttu-id="b7139-114">例如，Direct3D 中的16位色彩格式定義為 D3DFMT \_ R5G6B5，其中5位會保留給 red (R) 、6位表示綠色 (G) ，以及5位表示藍色 (B) 。</span><span class="sxs-lookup"><span data-stu-id="b7139-114">For example, a 16-bit color format in Direct3D is defined as D3DFMT\_R5G6B5, where 5 bits are reserved for red (R), 6 bits for green (G), and 5 bits for blue (B).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7139-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7139-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7139-116">Direct3D 表面</span><span class="sxs-lookup"><span data-stu-id="b7139-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 



