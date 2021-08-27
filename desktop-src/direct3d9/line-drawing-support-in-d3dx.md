---
description: 深入瞭解 D3DX 中的線條繪製支援。 D3DX 是提供 helper 服務的公用程式庫。 它是 Direct3D 元件之上的一層。
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: 'D3DX 中的線條繪圖支援 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9cf107615410da6dcfba02d6f708129429e31586360183277fb8f669653d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799679"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>D3DX 中的線條繪圖支援 (Direct3D 9) 

D3DX 是提供 helper 服務的公用程式庫。 它是 Direct3D 元件之上的一層。

D3DX 支援全圖元的反鋸齒線條。 不再支援行模式。

線條繪圖程式庫會使用材質三角形來模擬線條，並假設如下：

-   透過 Direct3D 9 介面可取得硬體。
-   至少有一個材質階段可供使用。
-   使用64x64 紋理。
-   可用的模式如下：
    -   雙線性篩選
    -   夾具位址模式
    -   換行位址模式
    -   Alpha op lambert
    -   Alpha 混色 (SRCBLEND = SRC \_ Alpha，DESTBLEND = INV \_ src \_ Alpha) 
    -   Alpha 測試是否無法使用 Alpha 混色;低品質結果

若要在多重取樣轉譯目標中呈現反鋸齒線條，請使用會產生紋理多邊形的 [**ID3DXLine**](id3dxline.md) 。 以反鋸齒線分隔的圖元涵蓋範圍值，lambert 圖元著色器所計算的圖元 Alpha 值。 若要繪製反鋸齒線，應用程式必須啟用 Alpha 混合，然後必須將 D3DRS \_ ANTIALIASEDLINEENABLE 轉譯狀態設為 **TRUE**。

## <a name="functionality-description"></a>功能描述

此程式庫支援以下列線條功能繪製彩色的行條紋，其中每個功能都與任何其他功能無關：

-   線條寬度
-   具有重複 (行模式計數器會隨著每個 ID3DXLine 而重設的行模式 [**：:D raw**](id3dxline--draw.md) 或 [**ID3DXLine：:D rawtransform**](id3dxline--drawtransform.md) 呼叫。 它不會隨著行帶的每個區段重設。 ) 
-   消除鋸齒
-   OpenGL 樣式行

> [!Note]  
> 不支援 mitering。

 

程式庫會使用原生硬體線路繪圖支援 (如果只有在下列情況才可在裝置) ：

-   線條寬度為1。
-   未啟用行模式。

某些硬體支援全圖元的反鋸齒程式列，因此，程式庫會使用該程式碼（如果有的話）。 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構的 LineCaps 成員會列舉線條繪圖基本專案的硬體功能。

使用軟體線繪圖時，每一行都會展開至矩形，並將四個頂點向下傳送至驅動程式。

每個線段都會以兩個三角形繪製。 基本的寬度是指定的寬度加上1.0，這可能會導致額外的資料列或資料行的圖元。 當線條變得更寬時，材質中的消除鋸齒漸層會變得更粗糙，而在中間會複寫更完全不透明的材質。 漸層是以材質的 v 方向進行編碼，通常是沿著 u 方向進行複製。 V 的材質定址模式是夾具。

清單中的每個線條區段都可以被視為從上一個結束點開始的另一行。

沿著邊緣平行至原始線條長度的消除鋸齒品質，會隨著線條變得更寬而受到影響。 如果行寬度大於32.0，則會開始展示這些邊緣的成品。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



