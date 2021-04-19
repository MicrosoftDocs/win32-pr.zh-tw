---
title: 使用 Win32 和 c + +) 開始的滑鼠輸入 (
description: 滑鼠輸入
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106966074"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a><span data-ttu-id="ee0b9-103">使用 Win32 和 c + +) 開始的滑鼠輸入 (</span><span class="sxs-lookup"><span data-stu-id="ee0b9-103">Mouse Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="ee0b9-104">Windows 最多可支援具有五個按鈕的滑鼠：左方、中間和右邊，還有兩個額外的按鈕，稱為 XBUTTON1 和 XBUTTON2。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-104">Windows supports mice with up to five buttons: left, middle, and right, plus two additional buttons called XBUTTON1 and XBUTTON2.</span></span>

![顯示左 (1) 、右邊 (2) 、中間 (3) 和 xbutton1 (4) 按鈕的圖例。](images/mouse.png)

<span data-ttu-id="ee0b9-106">Windows 大部分的滑鼠都至少有左方和右邊的按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-106">Most mice for Windows have at least the left and right buttons.</span></span> <span data-ttu-id="ee0b9-107">滑鼠左鍵用於指標、選取、拖曳等等。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-107">The left mouse button is used for pointing, selecting, dragging, and so forth.</span></span> <span data-ttu-id="ee0b9-108">滑鼠右鍵通常會顯示內容功能表。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-108">The right mouse button typically displays a context menu.</span></span> <span data-ttu-id="ee0b9-109">有些滑鼠具有滾輪，位於左右按鈕之間。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-109">Some mice have a scroll wheel located between the left and right buttons.</span></span> <span data-ttu-id="ee0b9-110">視滑鼠的不同，滾輪也可以按一下，使其成為中間按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-110">Depending on the mouse, the scroll wheel might also be clickable, making it the middle button.</span></span>

<span data-ttu-id="ee0b9-111">[XBUTTON1] 和 [XBUTTON2] 按鈕通常位於靠近基底之滑鼠的側邊。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-111">The XBUTTON1 and XBUTTON2 buttons are often located on the sides of the mouse, near the base.</span></span> <span data-ttu-id="ee0b9-112">這些額外的按鈕不會出現在所有滑鼠上。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-112">These extra buttons are not present on all mice.</span></span> <span data-ttu-id="ee0b9-113">如果有的話，XBUTTON1 和 XBUTTON2 按鈕通常會對應到應用程式函式，例如在網頁瀏覽器中向前和向後流覽。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-113">If present, the XBUTTON1 and XBUTTON2 buttons are often mapped to an application function, such as forward and backward navigation in a Web browser.</span></span>

<span data-ttu-id="ee0b9-114">左邊的使用者通常會發現，更適合用來交換左右按鈕的函式（使用右按鈕做為指標），以及使用左側按鈕顯示操作功能表。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-114">Left-handed users often find it more comfortable to swap the functions of the left and right buttons—using the right button as the pointer, and the left button to show the context menu.</span></span> <span data-ttu-id="ee0b9-115">基於這個理由，Windows 說明文件會使用 [ *主要] 按鈕* 和 *次要按鈕* 來參考邏輯函式，而不是實體放置。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-115">For this reason, the Windows help documentation uses the terms *primary button* and *secondary button*, which refer to logical function rather than physical placement.</span></span> <span data-ttu-id="ee0b9-116">在預設的 (右手) ] 設定中，左側按鈕是主要按鈕，右邊是次要按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-116">In the default (right-handed) setting, the left button is the primary button and the right is the secondary button.</span></span> <span data-ttu-id="ee0b9-117">不過，以 *滑鼠右鍵按一下* ，然後 *按一下滑鼠左鍵* ，則會參考邏輯動作。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-117">However, the terms *right click* and *left click* refer to logical actions.</span></span> <span data-ttu-id="ee0b9-118">以 *滑鼠右鍵按一下* 是指按一下主要按鈕，該按鈕是在滑鼠的右方或左邊。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-118">*Right clicking* means clicking the primary button, whether that button is physically on the right or left side of the mouse.</span></span>

<span data-ttu-id="ee0b9-119">不論使用者如何設定滑鼠，Windows 都會自動轉譯滑鼠訊息，使其一致。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-119">Regardless of how the user configures the mouse, Windows automatically translates mouse messages so they are consistent.</span></span> <span data-ttu-id="ee0b9-120">使用者可以在使用您的程式時交換主要和次要按鈕，而不會影響您的程式列為。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-120">The user can swap the primary and secondary buttons in the middle of using your program, and it will not affect how your program behaves.</span></span>

<span data-ttu-id="ee0b9-121">MSDN 檔使用 [將詞彙 *右移* ] 按鈕和 [ *左] 按鈕* ，以表示 *主要* 和 *次要* 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-121">MSDN documentation uses the terms *right button* and *left button* to mean *primary* and *secondary* button.</span></span> <span data-ttu-id="ee0b9-122">這項術語與滑鼠輸入的視窗訊息名稱一致。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-122">This terminology is consistent with the names of the window messages for mouse input.</span></span> <span data-ttu-id="ee0b9-123">請記住，實體的左和右按鈕可能會被交換。</span><span class="sxs-lookup"><span data-stu-id="ee0b9-123">Just remember that the physical left and right buttons might be swapped.</span></span>

## <a name="next"></a><span data-ttu-id="ee0b9-124">下一個</span><span class="sxs-lookup"><span data-stu-id="ee0b9-124">Next</span></span>

[<span data-ttu-id="ee0b9-125">回應滑鼠點擊</span><span class="sxs-lookup"><span data-stu-id="ee0b9-125">Responding to Mouse Clicks</span></span>](mouse-clicks.md)

 

 




