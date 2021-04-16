---
title: 翻轉模型、中途矩形、捲動區域
description: DXGI 1.2 支援新的翻轉模型交換鏈、中途矩形和捲動區域。 我們將說明使用新翻轉模型交換鏈的優點，以及藉由指定未變更的矩形和捲動區域來優化簡報。
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "104564077"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a>翻轉模型、中途矩形、捲動區域

DXGI 1.2 支援新的翻轉模型交換鏈、中途矩形和捲動區域。 我們將說明使用新翻轉模型交換鏈的優點，以及藉由指定未變更的矩形和捲動區域來優化簡報。

## <a name="dxgi-flip-model-presentation"></a>DXGI 翻轉模型簡報

DXGI 1.2 新增了 Direct3D 10 和更新版本 Api 之翻轉表示模型的支援。 在 Windows 7 中，Direct3D 9EX 會先採用 [反轉模型呈現](../direct3darticles/direct3d-9ex-improvements.md) ，以避免不必要地複製交換鏈緩衝區。 藉由使用翻轉模型，背景緩衝區會在執行時間和桌面視窗管理員 (DWM) 之間翻轉，因此 DWM 一律會直接從後端緩衝區撰寫，而不是複製回緩衝區內容。

DXGI 1.2 Api 包含修改過的 DXGI 交換連結口 [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1)。 您可以使用多個 [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2)介面方法來建立適當的 IDXGISwapChain1 物件，以搭配 [**HWND**](../winprog/windows-data-types.md)控制碼、 [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041)物件、 [DirectComposition](../directcomp/directcomposition-portal.md)或物件 [**使用。**](/uwp/api/Windows.UI.Xaml?view=winrt-19041)

您可以藉由在 [**dxgi \_ 交換 \_ 鏈 \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)結構的 **SwapEffect** 成員中指定 [**dxgi \_ 交換 \_ 效果 \_ \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) ，以及將 **dxgi \_ 交換 \_ 鏈 \_ DESC1** 的 **BufferCount** 成員設定為最小值2，來選取翻轉展示模型。 如需如何使用 DXGI 反轉模型的詳細資訊，請參閱 [dxgi 翻轉模型](dxgi-flip-model.md)。 由於反轉展示模型的呈現方式和其他新功能，我們建議您針對使用 Direct3D 10 和更新版本的 Api 撰寫的所有新應用程式使用 flip 展示模型。

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a>在交換鏈簡報中使用中途矩形和滾動矩形

藉由在交換鏈簡報中使用中途矩形和捲軸矩形，您可以節省記憶體頻寬的使用量和系統電源的相關使用方式，因為如果作業系統不需要繪製整個框架，作業系統需要繪製下一個所呈現畫面格的圖元資料量就會降低。 對於通常透過遠端桌面連線和其他遠端存取技術所顯示的應用程式，省下的成本特別明顯，因為這些技術會使用中途矩形和捲軸中繼資料。

您只能使用 scroll presentation model 中執行的 DXGI 交換鏈來進行滾動。 您可以使用中途的矩形，搭配在 flip 模型和 bitblt 模型中執行的 DXGI 交換鏈， (以 [**dxgi \_ 交換 \_ 效果 \_ 順序**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)) 來設定。

在此案例中，我們會示範使用中途矩形和滾動的功能。 在這裡，可滾動的應用程式包含文字和動畫動畫。 應用程式會使用中途矩形來更新視窗的動畫動畫和新行，而不是更新整個視窗。 捲軸矩形可讓作業系統複製和轉譯先前在新框架上轉譯的內容，並只在新的框架上轉譯新的一行。

應用程式會藉由呼叫 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 方法來執行簡報。 在此呼叫中，應用程式會將指標傳遞至 [**DXGI \_ 目前的 \_ 參數**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) 結構，其中包含中途矩形和中途矩形的數目、捲軸矩形和相關聯的捲軸位移，或是已變更的矩形和捲軸矩形。 我們的應用程式會傳遞2個中途的矩形和捲軸矩形。 捲軸矩形是上一個框架的區域，作業系統必須先將它複製到目前的框架，才能呈現目前的畫面格。 應用程式會將影片和新行的動畫指定為中途矩形，而作業系統會將它們呈現在目前的框架上。

![捲軸和中途矩形重迭的圖例](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

虛線矩形會顯示目前框架中的滾動矩形。 捲軸矩形是由 [**DXGI \_ 目前 \_ 參數**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters)的 **pScrollRect** 成員所指定。 箭號會顯示捲軸位移。 捲軸位移是由 **DXGI \_ 目前 \_ 參數** 的 **pScrollOffset** 成員所指定。 填滿的矩形會顯示應用程式以新內容更新的已變更矩形。 填滿的矩形是由 **DXGI \_ 目前 \_ 參數** 的 **DirtyRectsCount** 和 **pDirtyRects** 成員所指定。

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a>範例 2-緩衝區翻轉模型交換鏈與中途矩形和捲軸矩形

下圖和序列顯示使用中途矩形和捲軸矩形的 DXGI 翻轉模型展示作業範例。 在此範例中，我們會使用翻轉模型呈現的最小緩衝區數目，也就是兩個緩衝區計數、一個包含應用程式顯示內容的前端緩衝區，以及一個包含應用程式想要轉譯之目前框架的後端緩衝區。

1.  如框架開頭的前端緩衝區所示，可滾動的應用程式一開始會顯示具有一些文字和動畫動畫的畫面格。
2.  為了呈現下一個畫面格，應用程式會在背景緩衝區上轉譯更新動畫動畫的中途矩形，以及視窗的新線條。
3.  當應用程式呼叫 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)時，它會指定中途矩形和捲軸矩形和位移。 執行時間接著會將上一個框架中的滾動矩形複製到目前的背景緩衝區，減去更新的中途矩形。
4.  執行時間最後會交換前端和後端緩衝區。

![具有捲軸和中途矩形的翻轉模型交換鏈範例](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a>跨多個畫面格追蹤中途的矩形並滾動矩形

當您在應用程式中使用中途的矩形時，必須追蹤中途的矩形以支援累加式呈現。 當您的應用程式呼叫具有中途矩形的 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 時，您必須確定中途矩形內的每個圖元都是最新的。 如果您未完全重新轉譯中途矩形的整個區域，或是您不知道某些變動總數的區域，則必須先將一些資料從先前的完整一致背景緩衝區複製到目前的過時緩衝區，然後再開始轉譯。

執行時間只會複製上一個畫面格更新區域與目前框架的更新區域之間的差異到目前的背景緩衝區。 如果這些區域交集，則執行時間只會複製它們之間的差異。 如您在下圖和順序中所見，您必須將中途矩形之間的交集，從畫面格2複製到框架2的中途矩形。

1.  顯示畫面格1中的已變更矩形。
2.  從畫面格1的中途矩形和框架2中的中途矩形將交集複製到框架2的中途矩形。
3.  在畫面格2中顯示中途的矩形。

![跨多個框架追蹤滾動和中途的矩形](images/track-dirty-rects-scroll-rects.png)

為了一般化，如果是具有 N 個緩衝區的交換鏈，則執行時間從最後一個畫面格複製到目前框架上目前框架的區域是：

![要計算執行時間複本區域的方程式](images/runtime-copy-equation.png)

其中，緩衝區會在交換鏈中指出緩衝區索引，從目前的緩衝區索引零開始。

您可以使用上一個畫面格的適當內容，來追蹤上一個框架與目前框架的中途矩形之間的任何交集，方法是保留先前框架的已中途矩形複本，或重新呈現新框架的已變更矩形。

同樣地，在交換鏈有2個以上的背景緩衝區的情況下，您必須確保複製或重新轉譯目前緩衝區的已中途矩形與所有先前畫面格之中途矩形之間的重迭區域。

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a>追蹤2個中途矩形之間的單一交集

在最簡單的情況下，當您更新每個畫面格的單一未變更矩形時，跨兩個框架的中途矩形可能會交集。 若要找出先前畫面格的中途矩形和目前框架的中途矩形是否重迭，您必須確認上一個框架的中途矩形是否與目前框架的中途矩形交集。 您可以呼叫 GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) 函式來判斷兩個 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構是否交集。

在此程式碼片段中，呼叫 [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) 會傳回另一個 [**矩形**](/previous-versions//dd162897(v=vs.85)) 中稱為 dirtyRectCopy 的兩個中途矩形的交集。 在程式碼片段判斷兩個中途的矩形相交之後，它會呼叫 [**ID3D11DeviceCoNtext1：： CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) 方法，將交集區域複製到目前的框架中。

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

如果您在應用程式中使用此程式碼片段，則應用程式就可以開始呼叫 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) ，以目前的已變更矩形來更新目前的畫面格。

### <a name="tracking-intersections-between-n-dirty-rectangles"></a>追蹤 N 個中途矩形之間的交集

如果您指定多個中途的矩形（可以針對新出現的捲軸，包含每個框架的中途矩形），就必須確認並追蹤上一個框架的所有已中途矩形和目前框架的所有已中途矩形之間可能發生的任何重迭。 若要計算前一個框架的中途矩形與目前框架的中途矩形之間的交集，您可以將中途矩形分組為區域。

在此程式碼片段中，我們會呼叫 GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) 函式，將每個中途矩形轉換成矩形區域，然後呼叫 gdi [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) 函式，將所有已變更的矩形區域合併成一個群組。

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

您現在可以使用 GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) 函式來判斷上一個框架的中途區域與目前框架的中途區域之間的交集。 取得相交區域之後，呼叫 GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) 函式以從交集區域取得每個個別的矩形，然後呼叫 [**ID3D11DeviceCoNtext1：： CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) 方法，將每個相交的矩形複製到目前的背景緩衝區。 下一個程式碼片段說明如何使用這些 GDI 和 Direct3D 函數。

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a>具有中途矩形的 Bitblt 模型交換鏈

您可以將中途的矩形與 bitblt 模型中執行的 DXGI 交換鏈搭配使用， (以 [**dxgi \_ 交換 \_ 效果 \_ 順序**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)) 來設定。 使用多個緩衝區的 Bitblt 模型交換鏈，也必須在不同的框架中追蹤重迭的矩形，其方式與 [追蹤中途矩形和跨多個框架的捲軸](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) ，以進行翻轉模型交換鏈。 只有一個緩衝區的 Bitblt 模型交換鏈不需要追蹤重迭的已中途矩形，因為整個緩衝區會重繪每個畫面格。

## <a name="related-topics"></a>相關主題

[DXGI 1.2 改進](dxgi-1-2-improvements.md)
