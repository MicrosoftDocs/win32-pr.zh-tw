---
title: 範例轉譯程式碼
description: 範例轉譯程式碼
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- 視覺效果，範例程式碼
- 自訂視覺效果，範例程式碼
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- Render 函式，範例程式碼
- 範例、視覺效果的轉譯函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021690"
---
# <a name="sample-render-code"></a><span data-ttu-id="d8c15-109">範例轉譯程式碼</span><span class="sxs-lookup"><span data-stu-id="d8c15-109">Sample Render Code</span></span>

<span data-ttu-id="d8c15-110">以下是一些範例程式碼，它會使用 **Render** 函式在畫面上繪製線條。</span><span class="sxs-lookup"><span data-stu-id="d8c15-110">Here is some sample code that uses the **Render** function to draw a line across the screen.</span></span> <span data-ttu-id="d8c15-111">直線的高度是由波形值所定義。</span><span class="sxs-lookup"><span data-stu-id="d8c15-111">The height of the line is defined by the waveform value.</span></span>


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



<span data-ttu-id="d8c15-112">轉譯函式是程式 **代碼的主要** 工作發生的位置。</span><span class="sxs-lookup"><span data-stu-id="d8c15-112">The **Render** function is where the main work of your code takes place.</span></span> <span data-ttu-id="d8c15-113">每次 Windows Media Player 取得音訊的快照時，它就會呼叫這個函式，而您的程式碼將會執行。</span><span class="sxs-lookup"><span data-stu-id="d8c15-113">Every time Windows Media Player takes a snapshot of the audio, it will call this function and your code will run.</span></span>

<span data-ttu-id="d8c15-114">此程式碼會執行下列工作。</span><span class="sxs-lookup"><span data-stu-id="d8c15-114">This code performs the following tasks.</span></span> <span data-ttu-id="d8c15-115">如需特定功能的詳細資訊，請參閱 Microsoft Windows Platform SDK for 32 位 Windows。</span><span class="sxs-lookup"><span data-stu-id="d8c15-115">Refer to the Microsoft Windows Platform SDK for 32-bit Windows for more details about specific functions.</span></span>

## <a name="creating-objects"></a><span data-ttu-id="d8c15-116">建立物件</span><span class="sxs-lookup"><span data-stu-id="d8c15-116">Creating Objects</span></span>

<span data-ttu-id="d8c15-117">通常您會使用 Microsoft Windows 圖形化顯示介面隨附的繪圖函式 (GDI) 。</span><span class="sxs-lookup"><span data-stu-id="d8c15-117">Usually you will be using the drawing functions that come with the Microsoft Windows Graphical Display Interface (GDI).</span></span> <span data-ttu-id="d8c15-118">您必須建立畫筆來繪製線條和筆刷以填滿區域。</span><span class="sxs-lookup"><span data-stu-id="d8c15-118">You need to create pens to draw lines and brushes to fill areas.</span></span>

<span data-ttu-id="d8c15-119">建立實心的黑色筆刷以填滿背景。</span><span class="sxs-lookup"><span data-stu-id="d8c15-119">A solid black brush is created to fill in the background.</span></span>

<span data-ttu-id="d8c15-120">建立實心畫筆來繪製線條。</span><span class="sxs-lookup"><span data-stu-id="d8c15-120">A solid pen is created to draw a line.</span></span> <span data-ttu-id="d8c15-121">色彩會是即將顯示視覺效果的面板所定義的前景色彩。</span><span class="sxs-lookup"><span data-stu-id="d8c15-121">The color will be the foreground color as defined by the skin that is going to display the visualization.</span></span>

## <a name="adding-the-object-to-the-dc"></a><span data-ttu-id="d8c15-122">將物件新增至 DC</span><span class="sxs-lookup"><span data-stu-id="d8c15-122">Adding the Object to the DC</span></span>

<span data-ttu-id="d8c15-123">您必須將畫筆新增至裝置內容 (DC) 。</span><span class="sxs-lookup"><span data-stu-id="d8c15-123">You need to add the pen to the device context (DC).</span></span> <span data-ttu-id="d8c15-124">DC 是儲存所有繪圖資料和物件的記憶體部分。</span><span class="sxs-lookup"><span data-stu-id="d8c15-124">The DC is the portion of memory that all drawing data and objects are stored in.</span></span> <span data-ttu-id="d8c15-125">基本上，DC 是視窗流量管理員，可讓您以圖形方式追蹤所有內容。</span><span class="sxs-lookup"><span data-stu-id="d8c15-125">Essentially the DC is the window traffic manager that keeps track of everything graphical.</span></span>

<span data-ttu-id="d8c15-126">您需要 *轉換* 您所建立的畫筆物件，並將它儲存為舊的畫筆。</span><span class="sxs-lookup"><span data-stu-id="d8c15-126">You need to *cast* the pen object you created and store it as an old pen.</span></span> <span data-ttu-id="d8c15-127">針對所有新的畫筆使用此編碼技術。</span><span class="sxs-lookup"><span data-stu-id="d8c15-127">Use this coding technique for all new pens.</span></span> <span data-ttu-id="d8c15-128">這是32位程式設計所需的技術。</span><span class="sxs-lookup"><span data-stu-id="d8c15-128">This technique is required for 32-bit programming.</span></span>

## <a name="filling-in-the-background"></a><span data-ttu-id="d8c15-129">填滿背景</span><span class="sxs-lookup"><span data-stu-id="d8c15-129">Filling in the Background</span></span>

<span data-ttu-id="d8c15-130">您現在已準備好進行繪製。</span><span class="sxs-lookup"><span data-stu-id="d8c15-130">You now are ready to draw.</span></span> <span data-ttu-id="d8c15-131">**FillRect** 函式會填滿視窗的矩形，如 **Render** 函式的參數所定義。</span><span class="sxs-lookup"><span data-stu-id="d8c15-131">The **FillRect** function will fill the rectangle of the window, as defined by the parameters of the **Render** function.</span></span> <span data-ttu-id="d8c15-132">矩形會填入黑色筆刷。</span><span class="sxs-lookup"><span data-stu-id="d8c15-132">The rectangle is filled with a black brush.</span></span>

## <a name="getting-audio-data"></a><span data-ttu-id="d8c15-133">取得音訊資料</span><span class="sxs-lookup"><span data-stu-id="d8c15-133">Getting Audio Data</span></span>

<span data-ttu-id="d8c15-134">接下來，程式碼會從 Windows Media Player 取得一些音訊資料。</span><span class="sxs-lookup"><span data-stu-id="d8c15-134">Next the code gets some audio data from Windows Media Player.</span></span> <span data-ttu-id="d8c15-135">藉由使用波形陣列，您可以在拍攝快照集時取得音訊電源的目前值。</span><span class="sxs-lookup"><span data-stu-id="d8c15-135">By using the waveform array, you can get the current value of the audio power at the moment the snapshot was taken.</span></span> <span data-ttu-id="d8c15-136">在此情況下，您會取得左方頻道的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="d8c15-136">In this case, you are taking the audio data of the left channel.</span></span> <span data-ttu-id="d8c15-137">陣列中的第一個值是音訊電源快照的第一個1024th。</span><span class="sxs-lookup"><span data-stu-id="d8c15-137">The first value in the array is the first 1024th of the audio power snapshot.</span></span>

<span data-ttu-id="d8c15-138">這項資訊會用來顯示高度將符合音訊電源快照集的行。</span><span class="sxs-lookup"><span data-stu-id="d8c15-138">This information will be used to display a line whose height will match the audio power snapshot.</span></span>

## <a name="draw-the-line"></a><span data-ttu-id="d8c15-139">劃清底線</span><span class="sxs-lookup"><span data-stu-id="d8c15-139">Draw the Line</span></span>

<span data-ttu-id="d8c15-140">這一行是使用 **MoveToEx** 和 **LineTo** GDI 函數，從左至右繪製。</span><span class="sxs-lookup"><span data-stu-id="d8c15-140">The line is drawn from left to right using the **MoveToEx** and **LineTo** GDI functions.</span></span>

<span data-ttu-id="d8c15-141">首先，將畫筆移至起始點。</span><span class="sxs-lookup"><span data-stu-id="d8c15-141">First you move the pen to the starting point.</span></span> <span data-ttu-id="d8c15-142">在此情況下，會使用 x 和 y 來定義使用者將在螢幕上看到的由左至右和由上到下的值。</span><span class="sxs-lookup"><span data-stu-id="d8c15-142">In this case, x and y are used to define the left-to-right and top-to-bottom values the user will see on the screen.</span></span> <span data-ttu-id="d8c15-143">X 是由中國的矩形所定義，特別是由 prc >左方的值所定義。</span><span class="sxs-lookup"><span data-stu-id="d8c15-143">X is defined by the rectangle prc and specifically by the value of prc->left.</span></span> <span data-ttu-id="d8c15-144">Y 會定義為該時間的波形資料值。</span><span class="sxs-lookup"><span data-stu-id="d8c15-144">Y is defined as the value of the waveform data at that moment.</span></span>

<span data-ttu-id="d8c15-145">然後，您可以在視窗的另一端繪製線條。</span><span class="sxs-lookup"><span data-stu-id="d8c15-145">Then you draw a line to the other side of the window.</span></span> <span data-ttu-id="d8c15-146">您用來繪製線條的點也會是 x，y 值。</span><span class="sxs-lookup"><span data-stu-id="d8c15-146">The point you draw the line to is again an x, y value.</span></span> <span data-ttu-id="d8c15-147">X 是由中國的矩形所定義，但這次由 prc >右邊。</span><span class="sxs-lookup"><span data-stu-id="d8c15-147">X is defined by the rectangle prc, but this time by prc->right.</span></span> <span data-ttu-id="d8c15-148">Y 仍然是由波形資料定義，而且與您開始的點相同，因為您是從左至右繪製一條直線。</span><span class="sxs-lookup"><span data-stu-id="d8c15-148">Y is still defined by the waveform data and is the same as the point you started from, because you are drawing a straight line from left to right.</span></span>

## <a name="clean-up-everything"></a><span data-ttu-id="d8c15-149">清除所有專案</span><span class="sxs-lookup"><span data-stu-id="d8c15-149">Clean up Everything</span></span>

<span data-ttu-id="d8c15-150">您必須刪除您所建立的物件。</span><span class="sxs-lookup"><span data-stu-id="d8c15-150">You must delete the objects you create.</span></span> <span data-ttu-id="d8c15-151">具體來說，您必須刪除您所建立的任何筆刷和畫筆。</span><span class="sxs-lookup"><span data-stu-id="d8c15-151">Specifically you must delete any and all brushes and pens you create.</span></span> <span data-ttu-id="d8c15-152">當您完成使用畫筆和筆刷時，最好先將它們刪除。</span><span class="sxs-lookup"><span data-stu-id="d8c15-152">It is good practice to delete pens and brushes when you finish using them.</span></span>

<span data-ttu-id="d8c15-153">如果您未在完成 **轉譯函數的** 執行之前將其刪除，您的視覺效果會在一分鐘內損毀。</span><span class="sxs-lookup"><span data-stu-id="d8c15-153">If you do not delete them before finishing your implementation of the **Render** function, your visualization will crash in a minute or less.</span></span> <span data-ttu-id="d8c15-154">您必須保留畫筆和筆刷的計數，並終結每一個筆刷。</span><span class="sxs-lookup"><span data-stu-id="d8c15-154">You must keep a count of your pens and brushes and destroy every single one.</span></span> <span data-ttu-id="d8c15-155">請特別小心，不要在程式碼迴圈內建立畫筆。</span><span class="sxs-lookup"><span data-stu-id="d8c15-155">Be especially careful not to create pens inside a code loop.</span></span>

<span data-ttu-id="d8c15-156">使用範例中提供的程式碼撰寫技術來終結畫筆和筆刷。</span><span class="sxs-lookup"><span data-stu-id="d8c15-156">Use the coding technique given in the example to destroy your pens and brushes.</span></span>

-   <span data-ttu-id="d8c15-157">**重要** 摧毀您的畫筆和筆刷！</span><span class="sxs-lookup"><span data-stu-id="d8c15-157">**Important** Destroy your pens and brushes!</span></span>

<span data-ttu-id="d8c15-158">當您完成清除時，請務必返回 \_ [確定]，讓 Windows Media Player 知道您已完成繪製。</span><span class="sxs-lookup"><span data-stu-id="d8c15-158">When you have finished cleaning up, be sure to return S\_OK so that Windows Media Player knows you are finished drawing.</span></span> <span data-ttu-id="d8c15-159">一旦完成，您的繪圖就會傳送至視窗，將會取得另一個快照集，然後轉譯會要求您的程式碼再次 **繪製，依此類推** 。</span><span class="sxs-lookup"><span data-stu-id="d8c15-159">Once you finish, your drawing will be transferred to the window, another snapshot will be taken, **Render** will ask your code to draw again, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8c15-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8c15-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8c15-161">**執行轉譯**</span><span class="sxs-lookup"><span data-stu-id="d8c15-161">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




