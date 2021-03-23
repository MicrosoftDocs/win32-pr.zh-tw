---
title: 使用 Direct3D 12 的管線和著色器
description: 相較于上一代圖形程式設計介面，Direct3D 12 程式化管線可大幅提高轉譯效能。
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548383"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a>使用 Direct3D 12 的管線和著色器

相較于上一代圖形程式設計介面，Direct3D 12 程式化管線可大幅提高轉譯效能。

-   [Direct3D 12 圖形管線](#direct3d-12-graphics-pipeline)
-   [管線狀態物件](#pipeline-state-objects)
-   [Direct3D 12 計算管線](#direct3d-12-compute-pipeline)
-   [相關主題](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a>Direct3D 12 圖形管線

下圖說明 Direct3D 12 圖形管線和狀態。

![說明 direct3d 12 管線和狀態的圖表](images/pipeline.png)

圖形管線是 GPU 轉譯畫面格時，資料輸入和輸出的連續流程。 由於有管線狀態和輸入，GPU 會執行一連串的作業來建立產生的映射。 圖形管線包含著色器，可執行可程式化的轉譯效果和計算，以及固定的函式作業。

參考管線狀態圖表時，請注意下列事項：

-   描述項資料表和堆積可以任意排列： SRVs、CBVs 和 UAVs 可依任何順序參考及配置。
-   管線的某些作業是可設定的。 例如，輸出合併通常會以「轉譯目標」和「深度」樣板視圖的讀取-修改-寫入為基礎運作。 不過，您可以設定管線，讓其中一個視圖為唯讀或僅限寫入。
-   靜態取樣器不是根引數的一部分，因為它們是靜態引數。

## <a name="pipeline-state-objects"></a>管線狀態物件

Direct3D 12 引進 (PSO) 的管線狀態物件。 像輸入組合語言、轉譯器、圖元著色器和輸出合併等管線元件的狀態會儲存在 PSO 中，而不是儲存和表示大量高階物件的管線狀態。 PSO 是在建立之後不可變的整合管線狀態物件。 目前選取的 PSO 可以快速且動態地進行變更，而硬體和驅動程式可以直接將 PSO 轉換成原生硬體指示和狀態，讓 GPU 進行圖形處理。 為了套用 PSO，硬體會將最少量的預先計算狀態直接複製到硬體暫存器。 這會移除圖形驅動程式根據所有目前適用的轉譯和管線設定持續重新計算硬體狀態所造成的額外負荷。 結果會大幅減少繪製呼叫的額外負荷、提升效能，以及每個畫面格的繪製呼叫。

目前套用的 PSO 會定義並連接轉譯管線中使用的所有著色器。 [Microsoft 高階著色器語言 (HLSL) ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) 會預先編譯成著色器物件，然後在執行時間用來當做管線狀態物件的輸入。 如需有關如何在圖形管線內 PSO 函式的詳細資訊，請參閱 [在 Direct3D 12 中管理圖形管線狀態](managing-graphics-pipeline-state-in-direct3d-12.md)。

## <a name="direct3d-12-compute-pipeline"></a>Direct3D 12 計算管線

下圖說明 Direct3D 12 計算管線和狀態。

![顯示 Direct3D 12 計算管線的圖表。](images/compute-pipeline.png)

此管線中沒有固定的函式單位，不過，在計算中仍可使用描述元堆積、取樣器堆積和靜態取樣器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 Direct3D 12 中提交工作](command-queues-and-command-lists.md)
</dt> </dl>

 

 