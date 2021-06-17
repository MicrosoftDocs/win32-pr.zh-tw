---
description: 瞭解如何轉譯 Direct3D 10 的效果。 您可以使用效果來儲存資訊，或使用一組狀態來呈現。
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: 轉譯 (Direct3D 10) 的效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262570"
---
# <a name="rendering-an-effect-direct3d-10"></a>轉譯 (Direct3D 10) 的效果

您可以使用效果來儲存資訊，或使用一組狀態來呈現。 每項技術都會指定頂點著色器、幾何著色器、圖元著色器、著色器狀態、取樣器和材質狀態，以及其他管線狀態。 因此，當您將狀態組織成某個效果之後，您可以藉由建立和轉譯效果，來封裝該狀態所產生的轉譯效果。

有幾個步驟可準備轉譯的效果。 第一個是編譯，它會根據 HLSL 語言語法和效果架構規則來檢查 HLSL，例如程式碼。 您可以使用 API 呼叫來編譯應用程式的效果，也可以使用效果編譯器公用程式來離線編譯效果。 成功編譯效果之後，請呼叫不同 (但非常類似的) 組 Api 來建立它。

建立效果之後，有兩個剩餘的步驟可以使用它。 首先，您必須使用數個設定狀態的方法，將效果狀態值初始化 (的效果變數值) 。 針對某些變數，您可以在建立效果時完成這項操作;每次您的應用程式呼叫轉譯迴圈時，都必須更新其他專案。 設定效果變數後，您可以指示執行時間藉由套用技術來呈現影響。 以下將詳細討論這些主題。

-   [編譯效果 (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [ (Direct3D 10 建立效果) ](d3d10-graphics-programming-guide-effects-create.md)
-   [設定效果狀態 (Direct3D 10) ](d3d10-graphics-programming-guide-effects-set-state.md)
-   [將技術套用 (Direct3D 10) ](d3d10-graphics-programming-guide-effects-apply-technique.md)

當然，使用效果會有 [效能考慮](d3d10-graphics-programming-guide-effects-performance.md) 。 如果您不是使用效果，則這些考慮大致相同。 例如，將狀態變更的數量降到最低，或組織需要依頻率更新的變數。 這些策略可用來將需要從 CPU 傳送到 GPU 的資料量降到最低，因此可將可能的同步處理問題降至最低。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的效果 ](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



