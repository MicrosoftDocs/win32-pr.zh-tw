---
description: " (Direct3D 10) 的效能考慮"
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: " (Direct3D 10) 的效能考慮"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025867"
---
# <a name="performance-considerations-direct3d-10"></a> (Direct3D 10) 的效能考慮

## <a name="using-effect-pools"></a>使用效果集區

轉譯管線通常會使用許多著色器來呈現不同的物件類型和特殊效果。 著色器是所有著色器（例如世界矩陣或光線位置）中常見的狀態，以及每個著色器（例如物件的擴散色彩或反射反白顯示計算）特定的狀態。 效果集區是記憶體中的位置，用於儲存許多著色器所使用的狀態，以及一般裝置物件（例如著色器、轉譯狀態物件和常數緩衝區）。 效能改進的結果是針對所有需要該狀態的著色器，更新常見狀態一次。

效果集區是作用中狀態的共用記憶體位置。 建立集區的方式類似于效果;您可以從記憶體 (或檔案或資源) 來建立它。 這會導致兩種不同類型的效果：不依賴其他效果中狀態的全域效果，以及相依于其他效果中狀態的子效果。

您可以在建立效果時，藉由提供 [D3D10 \_ 效果 \_ 編譯 \_ 子 \_ 效果](d3d10-effect.md) 旗標) ，指定效果是否為全域效果 (預設案例) 或子效果 (。 全域效果可以作為效果集區;子效果不能是效果集區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呈現效果](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[ (Direct3D 10) 的效果 ](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



