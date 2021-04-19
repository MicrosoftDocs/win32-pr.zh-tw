---
title: '使用矩形 (Windows Media Player SDK) '
description: 使用矩形
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- 視覺效果、矩形
- 自訂視覺效果，矩形
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 轉譯函數、矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967513"
---
# <a name="using-rectangles-windows-media-player-sdk"></a><span data-ttu-id="ad2db-108">使用矩形 (Windows Media Player SDK) </span><span class="sxs-lookup"><span data-stu-id="ad2db-108">Using Rectangles (Windows Media Player SDK)</span></span>

<span data-ttu-id="ad2db-109">矩形可用來指定 Microsoft Windows 中的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="ad2db-109">Rectangles are used to specify rectangular areas in Microsoft Windows.</span></span> <span data-ttu-id="ad2db-110">您可以在視窗中建立許多矩形，但 Windows Media Player 透過 [IWMPEffects：： Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) 函數提供一個矩形的值。</span><span class="sxs-lookup"><span data-stu-id="ad2db-110">You can create many rectangles in your window, but Windows Media Player supplies the values of one rectangle through the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function.</span></span> <span data-ttu-id="ad2db-111">如果您的外掛程式使用視窗轉譯，矩形就是視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="ad2db-111">If your plug-in renders using a window, the rectangle is the client area of the window.</span></span> <span data-ttu-id="ad2db-112">這稱為中國矩形，它會定義 Windows Media Player 將顯示視覺效果的矩形。</span><span class="sxs-lookup"><span data-stu-id="ad2db-112">This is called the prc rectangle, and it defines the rectangle that Windows Media Player will display your visualization through.</span></span> <span data-ttu-id="ad2db-113">請經常使用此方法，以確保您不會在 Windows Media Player 所提供的矩形範圍之外進行繪製。</span><span class="sxs-lookup"><span data-stu-id="ad2db-113">Use this frequently to be sure you do not draw beyond the extents of the rectangle supplied by Windows Media Player.</span></span>

<span data-ttu-id="ad2db-114">矩形有四個定義它的值。</span><span class="sxs-lookup"><span data-stu-id="ad2db-114">A rectangle has four values that define it.</span></span> <span data-ttu-id="ad2db-115">它們是 left、top、right 和底端。</span><span class="sxs-lookup"><span data-stu-id="ad2db-115">They are left, top, right, and bottom.</span></span> <span data-ttu-id="ad2db-116">矩形的左上角是由左和上定義，而矩形的右下角則由右下角定義。</span><span class="sxs-lookup"><span data-stu-id="ad2db-116">The top, left corner of the rectangle is defined by left and top, and the bottom, right corner of the rectangle is defined by bottom and right.</span></span>

<span data-ttu-id="ad2db-117">使用下列程式碼來取得繪圖矩形的範圍。</span><span class="sxs-lookup"><span data-stu-id="ad2db-117">Use the following code to get the extents of your drawing rectangle.</span></span> <span data-ttu-id="ad2db-118">您需要這麼做，是因為使用者可能會調整視窗的大小，而您想要確定一律是在使用者可以看到的區域中繪製。</span><span class="sxs-lookup"><span data-stu-id="ad2db-118">You need to do this because the user may resize the window, and you want to be sure that you are always drawing in an area the user can see.</span></span>


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



<span data-ttu-id="ad2db-119">例如，若要從左至右繪製，請在視窗的頂端，使用如下的程式碼：</span><span class="sxs-lookup"><span data-stu-id="ad2db-119">For example, to draw from left to right, along the top of the window, use code like this:</span></span>


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a><span data-ttu-id="ad2db-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad2db-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad2db-121">**執行轉譯**</span><span class="sxs-lookup"><span data-stu-id="ad2db-121">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




