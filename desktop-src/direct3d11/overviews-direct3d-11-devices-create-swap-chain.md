---
title: 如何建立交換鏈
description: 本主題說明如何建立交換鏈，以封裝兩個或多個用於呈現和顯示的緩衝區。
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375981"
---
# <a name="how-to-create-a-swap-chain"></a>如何：建立交換鏈

本主題說明如何建立交換鏈，以封裝兩個或多個用於呈現和顯示的緩衝區。 它們通常會包含顯示裝置的前端緩衝區，以及做為呈現目標的背景緩衝區。 當立即內容完成轉譯至背景緩衝區之後，交換鏈會藉由交換這兩個緩衝區來呈現後端緩衝區。

交換鏈定義了數種轉譯特性，包括：

-   轉譯區域的大小。
-   顯示更新率。
-   顯示模式。
-   介面格式。

藉由填妥 [**DXGI \_ 交換 \_ 鏈 \_ DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) 結構並初始化 [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) 介面，來定義交換鏈的特性。 藉由呼叫 [**IDXGIFactory：： CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)，初始化交換鏈。

## <a name="create-a-device-and-a-swap-chain"></a>建立裝置和交換鏈

若要初始化裝置和交換鏈，請使用下列兩個函式的其中一種：

-   當您想要在裝置初始化時同時初始化交換鏈時，請使用 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) 函數。 這通常是最簡單的選項。

-   當您已經使用 [**IDXGIFactory：： CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)建立交換鏈時，請使用 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置](overviews-direct3d-11-devices.md)
</dt> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 