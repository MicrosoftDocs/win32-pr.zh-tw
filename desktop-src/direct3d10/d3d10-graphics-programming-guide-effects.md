---
description: DirectX 效果是管線狀態的集合，由以 HLSL 撰寫的運算式所設定，以及某些特定于效果架構的語法。
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: " (Direct3D 10) 的效果"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e08d0c79a6f7f52982a74d5127da70d7b82f84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970541"
---
# <a name="effects-direct3d-10"></a> (Direct3D 10) 的效果

DirectX 效果是管線狀態的集合，由以 [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) 撰寫的運算式所設定，以及某些特定于效果架構的語法。 編譯效果之後，請使用效果架構 Api 來呈現。 效果功能的範圍可以像是頂點著色器一樣簡單，也就是轉換幾何和圖元著色器以輸出純色、轉換成需要多個行程的轉譯技術、使用圖形管線的每個階段，以及操作著色器狀態以及未與可程式化著色器相關聯的管線狀態。

第一個步驟是將您想要控制的狀態組織成一個效果。 這包括著色器狀態 (頂點、幾何和圖元著色器) 、著色器所使用的材質和取樣器狀態，以及其他無法程式化的管線狀態。 您可以在記憶體中以文字字串的形式建立效果，但一般來說，大小夠大，因為在效果檔案中儲存效果的狀態， (一個以 fx 副檔名) 結尾的文字檔。 若要使用效果，您必須將它編譯 (以檢查 HLSL 語法以及效果架構語法) 、透過 API 呼叫初始化效果狀態，以及修改轉譯迴圈來呼叫轉譯 Api。

-   [組織效果中的狀態](d3d10-graphics-programming-guide-effects-organize.md)
-   [效果系統介面](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [專用介面](d3d10-graphics-reference-effect-specializing.md)
-   [呈現效果](d3d10-graphics-programming-guide-effects-render.md)

效果會將特定效果所需的所有轉譯狀態封裝到稱為技術的單一轉譯函數中。 Pass 是技術的子集合，其中包含呈現狀態。 若要執行多重傳遞轉譯效果，請在技術內執行一或多個階段。 例如，假設您想要使用一組深度/樣板緩衝區來轉譯某些幾何，然後在其上方繪製一些 sprite。 您可以在第一個階段中執行幾何轉譯，並在第二個階段中執行 sprite 繪製。 若要轉譯效果，您只需在轉譯迴圈中轉譯這兩個階段。 您可以在效果中執行任何數目的技巧。 當然，技術的數目愈大，結果的編譯時間就愈大。 利用這項功能的其中一種方法，就是使用專為在不同硬體上執行而設計的技術來建立效果。 這可讓應用程式根據偵測到的硬體功能，適當地將效能降級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 10 程式設計手冊](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
