---
description: Direct3D 應用程式通常會在背景緩衝區產生動畫的畫面格，並依序顯示動畫，以顯示動畫序列。
ms.assetid: 4ca9a845-f433-4d4a-939e-4b9ab2983927
title: " (Direct3D 9 中翻轉表面) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dafd263de0f907b33ff6f20ffcbb2cce69943da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688111"
---
# <a name="flipping-surfaces-direct3d-9"></a> (Direct3D 9 中翻轉表面) 

Direct3D 應用程式通常會在背景緩衝區產生動畫的畫面格，並依序顯示動畫，以顯示動畫序列。 背景緩衝區會組織成交換鏈。 交換鏈是一系列的緩衝區，會將一系列的緩衝區「翻轉」至畫面。 這可以用來呈現記憶體中的一個場景，然後在轉譯完成時將場景翻轉至螢幕。 這可避免稱為撕裂的現象，並允許更流暢的動畫。

在 Direct3D 中建立的每個裝置都至少有一個交換鏈。 當您初始化第一個 Direct3D 裝置時，您會設定 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)的 BackBufferCount 成員，以告訴 Direct3D 將在交換鏈中的後端緩衝區數目。 然後，對 [**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 的呼叫會建立 Direct3D 裝置和對應的交換鏈。

當您使用 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 重新傳送以要求介面翻轉作業時，會交換前端緩衝區和背景緩衝區的介面記憶體指標。 翻轉的執行方式是切換顯示裝置用於參考記憶體的指標，而不是藉由複製介面記憶體。 當翻轉鏈包含一個前端緩衝區和一個以上的背景緩衝區時，指標會以迴圈模式切換，如下圖所示。

![具有前端緩衝區和兩個背景緩衝區的翻轉鏈圖表](images/trplflip.png)

您可以藉由呼叫 [**IDirect3DDevice9：： CreateAdditionalSwapChain**](/windows/desktop/api)來建立裝置的新增交換鏈。 應用程式可以為每個視圖建立一個交換鏈，並將每個交換鏈與特定視窗建立關聯。 應用程式會在每個交換鏈的後置緩衝區中轉譯影像，然後個別呈現。 **IDirect3DDevice9：： CreateAdditionalSwapChain** 所採用的兩個參數是 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)結構的指標，以及 [**IDirect3DSwapChain9**](/windows/desktop/api)介面指標的位址。 然後，您可以使用 [**IDirect3DSwapChain9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) 重新傳送，將下一個後端緩衝區的內容顯示到前一個緩衝區。 請注意，裝置只能有一個全螢幕交換鏈。

您可以藉由呼叫 [**IDirect3DDevice9：： GetBackBuffer**](/windows/desktop/api) 或 [**IDirect3DSwapChain9：： GetBackBuffer**](/windows/desktop/api) 方法來存取特定的上一頁緩衝區，這會傳回代表傳回之緩衝區介面的 [**IDirect3DSurface9**](/windows/desktop/api) 介面指標。 請注意，呼叫這個方法會增加 [**IDirect3DDevice9**](/windows/desktop/api) 介面上的內部參考計數，因此當您使用此介面完成時，請務必呼叫 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ，否則會發生記憶體流失。

請記住，Direct3D 會在交換鏈內交換介面記憶體指標，而不是藉由交換介面本身來翻轉介面。 這表示，您一律會轉譯為接下來將顯示的後端緩衝區。

請務必注意「翻轉作業」與「顯示配接器」驅動程式所執行的差異，以及套用至使用 D3DSWAPEFFECT FLIP 所建立交換鏈的「目前」作業 \_ 。

「反轉」一詞是指一項作業，此作業會改變顯示器介面卡用來產生其輸出信號的影片記憶體位址範圍，進而顯示先前隱藏的背景緩衝區內容。 在 Direct3D 9 中，常使用的詞彙通常是用來描述在使用 D3DSWAPEFFECT 翻轉交換效果所建立的任何交換鏈中呈現的背面緩衝區 \_ 。

當交換鏈是全螢幕時，這類「目前」作業幾乎都是由翻轉作業所執行，而且當交換鏈為視窗時，它們一定會由複製作業來執行。 此外，顯示器介面卡驅動程式可能會使用反向操作，根據 D3DSWAPEFFECT \_ 捨棄和 D3DSWAPEFFECT 複本針對全螢幕交換鏈來執行目前的作業 \_ 。

上述討論適用于使用 D3DSWAPEFFECT FLIP 所建立全螢幕交換鏈的常用案例 \_ 。

如需視窗和全螢幕交換鏈的不同交換效果的一般討論，請參閱 [**D3DSWAPEFFECT**](./d3dswapeffect.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 表面](direct3d-surfaces.md)
</dt> </dl>

 

 
