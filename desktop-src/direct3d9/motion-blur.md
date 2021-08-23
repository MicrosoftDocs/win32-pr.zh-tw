---
description: 您可以藉由模糊處理物件，並在物件後面留下模糊的物件影像軌跡，以增強3D 場景中物件的感覺速度。 Direct3D 應用程式會針對每個畫面格多次轉譯物件來完成這項工作。
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: " (Direct3D 9) 的動作模糊"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3daa0b35a0c375cc798b619f18f1e363001050de4dcc950e6c6828a7d365801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628318"
---
# <a name="motion-blur-direct3d-9"></a> (Direct3D 9) 的動作模糊

您可以藉由模糊處理物件，並在物件後面留下模糊的物件影像軌跡，以增強3D 場景中物件的感覺速度。 Direct3D 應用程式會針對每個畫面格多次轉譯物件來完成這項工作。

回想一下，Direct3D 應用程式通常會將幕後轉譯成螢幕緩衝。 當應用程式呼叫 IDirect3DDevice9 時，緩衝區的內容會顯示在螢幕上 [**：:P 重發**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 的方法。 在螢幕上顯示框架之前，您的 Direct3D 應用程式可以將物件多次轉譯成場景。

以程式設計的方式，您的應用程式會對 DrawPrimitive 方法進行多次呼叫，重複傳遞相同的3D 物件。 在每次呼叫之前，物件的位置會稍微更新，在目標呈現介面上產生一連串模糊的物件影像。 如果物件有一或多個紋理，您的應用程式可以藉由轉譯物件的第一個影像，使其所有紋理幾乎透明，以增強動畫模糊效果。 每次物件轉譯時，物件材質的透明度都會減少。 當您的應用程式將物件呈現在其最終位置時，它應該會轉譯物件的材質而不會有透明度。 例外狀況是，如果您要將動作模糊新增至其他需要材質透明度的效果。 在任何情況下，框架中物件的初始影像都應該是最透明的。 最後的影像應該是最不透明的。

當您的應用程式將一系列的物件影像轉譯到目標呈現介面上，並呈現場景的其餘部分之後，它應該呼叫 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 重新傳送的方法，在螢幕上顯示畫面格。

如果您的應用程式正在模擬使用者以高速方式在場景中移動的效果，則可以將動態模糊新增至整個場景。 在此情況下，您的應用程式會針對每個畫面格多次呈現整個場景。 每次呈現場景時，您的應用程式都必須稍微移動觀點。 如果場景高度複雜，使用者可能會看到效能降低，因為加速增加的原因是每個畫面格的場景轉譯數目增加。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消除鋸齒](antialiasing.md)
</dt> </dl>

 

 
