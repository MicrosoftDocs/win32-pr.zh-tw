---
description: 下列功能已新增至 Microsoft DirectX Graphic Infrastructure (DXGI) 1.3 （從 Windows 8.1 開始包含在內）。
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: DXGI 1.3 改進
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c863bc30ffdf27705492b56a5348040c8e12f4fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846044"
---
# <a name="dxgi-13-improvements"></a>DXGI 1.3 改進

下列功能已新增至 Microsoft DirectX Graphic Infrastructure (DXGI) 1.3 （從 Windows 8.1 開始包含在內）。

## <a name="trim-dxgi-adapter-memory-usage"></a>修剪 DXGI 介面卡記憶體使用量

從 Windows 8.1 開始，DXGI 1.3 會新增功能，以排清和釋放由 DXGI 介面卡配置的未使用記憶體資源。 這可讓應用程式在暫停時釋出暫存記憶體，減少應用程式將終止的機率，以供其他應用程式的免費資源之用。 當應用程式繼續時，支援 trim 的設備磁碟機會視需要重新建立資源。 從 Windows 8.1，應用程式所建立的所有 Direct3D 裝置都必須在暫停時呼叫 [**IDXGIDevice3：： Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) ，以減少記憶體使用量，並減少應用程式將終止的機會回收系統資源。

## <a name="multi-plane-overlays"></a>多平面重迭

從 Windows 8.1 開始，DXGI 1.3 支援多平面重迭。 您可以使用 [**IDXGIOutput2：： SupportsOverlays**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays)，找出裝置是否支援硬體中的多平面重迭。

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>重迭的交換鏈和交換鏈縮放比例

從 Windows 8.1 開始，DXGI 1.3 支援重迭的交換鏈。 重迭的交換鏈是用來以非原生解析度繪製3D 圖形 (搭配硬體消除倍增) ，同時以原生解析度呈現 UI。 這可讓遊戲利用較高的填滿率來回應遊戲，而不會降低 UI 元素的視覺品質，例如播放程式分數和對話文字。 在支援多平面重迭的裝置上，Direct3D 會針對重迭的交換鏈使用多平面重迭。 建立前景交換鏈，方法是在建立交換鏈時指定 [ [**DXGI \_ swap \_ chain \_ 旗標 \_ 前景 \_ 圖層**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) ] 旗標，並使用 [**IDXGISwapChain2：： SetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) 和 [**IDXGISwapChain2：： GetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) 來調整用於遊戲的交換鏈。

## <a name="select-backbuffer-subregion-for-swap-chain"></a>選取交換鏈的背景緩衝區子領域

從 Windows 8.1 開始，可以使用 DXGI 1.3 來選取背景緩衝區的子領域以與交換鏈搭配使用，讓您可以轉譯成較小的後置緩衝區，而不需要重新建立交換鏈。 請參閱 [**IDXGISwapChain2：： SetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) 和 [**IDXGISwapChain2：： GetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize)。

## <a name="lower-latency-swap-chain-presentation"></a>低延遲交換鏈簡報

從 Windows 8.1 開始，DXGI 1.3 可讓交換鏈在開始使用裝置來繪製下一個畫面格之前，先完成上一個畫面格的呈現，以降低延遲。 請參閱 [**IDXGISwapChain2：： GetFrameLatencyWaitableObject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject)、 [**IDXGISwapChain2：： GetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)和 [**IDXGISwapChain2：： SetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency)。

## <a name="related-topics"></a>相關主題

[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
