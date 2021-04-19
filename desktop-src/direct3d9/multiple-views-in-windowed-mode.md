---
description: 除了透過 Direct3DDevice 物件所擁有和操作的交換鏈之外，應用程式也可以使用 IDirect3DDevice9：： CreateAdditionalSwapChain 方法來建立額外的交換鏈，以顯示來自相同裝置的多個視圖。
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: '視窗模式中的多個視圖 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970284"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a>視窗模式中的多個視圖 (Direct3D 9) 

除了透過 Direct3DDevice 物件所擁有和操作的交換鏈之外，應用程式也可以使用 [**IDirect3DDevice9：： CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) 方法來建立額外的交換鏈，以顯示來自相同裝置的多個視圖。

一般而言，應用程式會為每個視圖建立一個交換鏈，並將每個交換鏈與特定的視圖產生關聯。 應用程式會在每個交換鏈的後置緩衝區中轉譯影像，然後使用 [**IDirect3DDevice9：:P 重發**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 的方法來個別呈現這些影像。 請注意，每個介面卡上一次只能有一個可全螢幕的交換鏈。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呈現場景](presenting-a-scene.md)
</dt> </dl>

 

 
