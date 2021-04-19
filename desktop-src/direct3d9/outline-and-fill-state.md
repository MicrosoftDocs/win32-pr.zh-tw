---
description: 沒有紋理的基本專案會以其材質所指定的色彩，或以頂點指定的色彩（如果有的話）來呈現。
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: " (Direct3D 9) 的大綱和填滿狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973941"
---
# <a name="outline-and-fill-state-direct3d-9"></a> (Direct3D 9) 的大綱和填滿狀態

沒有紋理的基本專案會以其材質所指定的色彩，或以頂點指定的色彩（如果有的話）來呈現。 您可以藉由指定 D3DRS FILLMODE 轉譯狀態的 [**D3DFILLMODE**](./d3dfillmode.md) 列舉類型所定義的值，來選取要填入的方法 \_ 。

若要啟用遞色，您的應用程式必須傳遞 D3DRS \_ DITHERENABLE 列舉值做為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)的第一個參數。 它必須將第二個參數設定為 **TRUE** 以啟用遞色，而 **FALSE** 則會停用。

有時候，繪製線條的最後一個圖元可能會使周圍的基本專案發生不美觀的重迭。 您可以使用 D3DRS LASTPIXEL 列舉值來控制這一點 \_ 。 不過，請勿變更此設定，而不需要一些深謀遠慮。 在某些情況下，隱藏最後圖元的轉譯可能會導致基本專案之間的間距不美觀。

您可以藉由設定適當的線條繪圖模式來繪製物件大綱。 預設的線條繪製狀態是繪製實線。 如需詳細資訊，請參閱 [D3DX 中的線條繪圖支援 (Direct3D 9) ](line-drawing-support-in-d3dx.md) 轉譯狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 
