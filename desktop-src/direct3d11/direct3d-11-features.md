---
title: Direct3D 11 功能
description: 程式設計指南包含如何使用 Direct3D 11 可程式化管線，為遊戲以及科學和桌面應用程式建立即時3D 圖形的相關資訊。
ms.assetid: ee4dae04-1a52-4587-87c1-006abb687a91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b6ec64e315275ca6faaf513d04f996609615a2
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024303"
---
# <a name="direct3d-11-features"></a>Direct3D 11 功能

程式設計指南包含如何使用 Direct3D 11 可程式化管線，為遊戲以及科學和桌面應用程式建立即時3D 圖形的相關資訊。

-   [計算著色器](#compute-shader)
-   [動態著色器連結](#dynamic-shader-linking)
-   [多執行緒](#multithreading)
-   [鑲嵌式](#tessellation)
-   [完整的功能清單](#full-listing-of-features)
-   [先前版本中新增的功能](#features-added-in-previous-releases)
-   [相關主題](#related-topics)

## <a name="compute-shader"></a>計算著色器

計算著色器是專為一般用途的資料平行處理而設計的可程式化著色器。 換句話說，計算著色器允許使用 GPU 作為一般用途的平行處理器。 計算著色器類似于其他可程式化管線著色器 (例如頂點、圖元、幾何在存取輸入和輸出的方式) 。 計算著色器技術也稱為 DirectCompute 技術。 計算著色器已整合至 Direct3D，可透過 Direct3D 裝置存取。 它可以使用 Direct3D 裝置，直接與圖形著色器共用記憶體資源。 但是，它不會直接連接到其他著色器階段。

計算著色器是針對以互動費率執行計算的大量市場應用程式所設計，當 API (與其相關聯的軟體) 堆疊之間的轉換成本時，以及 CPU 可能會耗用太多額外負荷。

計算著色器有自己的一組狀態。 計算著色器不一定會有強制的1-1 對應到輸入記錄 (例如頂點著色器會) 或輸出記錄 (例如圖元著色器) 。 支援圖形著色器的某些功能，但已移除其他功能，因此可以新增計算著色器特定功能。

為了支援計算著色器特有的功能，現在已有數種新的資源類型可供使用，例如讀取/寫入緩衝區、紋理和結構化緩衝區。

如需其他資訊，請參閱 [計算著色器總覽](direct3d-11-advanced-stages-compute-shader.md) 。

## <a name="dynamic-shader-linking"></a>動態著色器連結

轉譯系統在管理著色器時必須處理大量的複雜性，同時提供優化著色器程式碼的機會。 這會成為更大的挑戰，因為著色器必須在不同硬體設定之間的轉譯場景中支援各種不同的材質。 為了解決這項挑戰，著色器開發人員經常會被帶到兩種一般方法的其中一種。 他們建立了功能完整的大型、一般用途的著色器，可供各種不同的場景專案使用，以針對彈性來權衡某些效能，或針對每個幾何資料流程、材質類型或所需的光源類型組合建立個別的著色器。

這些大型的一般用途著色器會藉由使用不同的預處理器定義來重新編譯相同的著色器來處理這項挑戰，而後者的方法則是使用暴力密碼開發人員能力來達成相同的結果。 如果開發人員現在必須在其遊戲和資產管線中管理數千種不同的著色器排列，著色器排列爆炸通常會造成問題。

Direct3D 11 和著色器模型5引進了物件導向的語言結構，並提供著色器連結的執行時間支援，以協助開發人員程式著色器。

如需其他資訊，請參閱 [動態連結](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking) 。

## <a name="multithreading"></a>多執行緒

許多圖形應用程式都有 CPU 系結，因為這類的活動很高，例如場景圖形遍歷、物件排序和物理模擬。 由於多核心系統逐漸推出，因此 Direct3D 11 已改善其多執行緒支援，以在多個 CPU 執行緒和 D3D11 圖形 Api 之間啟用有效率的互動。

Direct3D 11 啟用下列功能以支援多執行緒處理：

-   並行物件現在是在不同的執行緒中建立的，讓可自由執行緒建立物件的進入點函數可讓許多執行緒同時建立物件。 例如，應用程式現在可以編譯著色器，或在另一個執行緒上載入材質。
-   您可以在多個執行緒上建立命令清單，命令清單是已錄製的圖形命令序列。 使用 Direct3D 11 時，您可以在多個 CPU 執行緒上建立命令清單，以平行方式在多個執行緒上進行場景資料庫或物理處理。 這會釋放主要轉譯執行緒，以將命令緩衝區分派至硬體。

如需其他資訊，請參閱 [多執行緒](overviews-direct3d-11-render-multi-thread.md) 。

## <a name="tessellation"></a>鑲嵌

鑲嵌可以用來呈現具有不同詳細資料層級的單一模型。 這種方法會產生更具幾何的精確模型，取決於場景所需的詳細程度。 在詳細資料層級允許較低幾何模型的場景中使用鑲嵌，可減少轉譯期間耗用的記憶體頻寬需求。

在 Direct3D 中，會在 GPU 上執行鑲嵌，以從粗略 (較不詳細的) 輸入修補程式來計算更平滑的曲線表面。 每個 (四或三角形) patch 臉部都會細分成較小的三角形臉部，以更接近您想要的表面。

如需在圖形管線中執行鑲嵌的詳細資訊，請參閱 [鑲嵌式總覽](direct3d-11-advanced-stages-tessellation.md)。

## <a name="full-listing-of-features"></a>完整的功能清單

這是 Direct3D 11 中功能的完整清單。

-   您可以在建立裝置時 specifing[功能等級](overviews-direct3d-11-devices-downlevel-intro.md)，在舊版[硬體](overviews-direct3d-11-devices-downlevel.md)上執行 Direct3D 11。
-   您可以使用下列著色器類型來執行鑲嵌式 (參閱 [鑲嵌式總覽](direct3d-11-advanced-stages-tessellation.md)) ：

    -   輪廓著色器
    -   網域著色器

-   Direct3D 11 支援多執行緒 (查看 [多執行緒](overviews-direct3d-11-render-multi-thread.md)) 

    -   多執行緒資源/著色器/物件建立
    -   多執行緒顯示清單建立

-   Direct3D 11 使用下列功能來擴充著色器 (參閱 [著色器模型 5](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) 

    -   可定址的資源-紋理、常數緩衝區和取樣器
    -   其他資源類型（例如讀取/寫入緩衝區和紋理） (查看 [新的資源類型](direct3d-11-advanced-stages-cs-resources.md)) 。
    -   子 例 程
    -   計算著色器 (查看 [計算著色](direct3d-11-advanced-stages-compute-shader.md) 器的總覽) -著色器可在數個軟體執行緒或執行緒群組之間劃分問題空間，以加速計算，並在著色器暫存器之間共用資料，以大幅減少輸入著色器所需的資料量。 計算著色器可大幅改善的演算法包括 post 處理、動畫、物理及人工智慧。
    -   幾何著色器 (請參閱 [幾何著色器功能](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-gs-features)) 

        -   實例-可讓幾何著色器輸出最多1024個頂點，或實例和頂點的任意組合，最多 1024 (最多每) 32 頂點的32實例。

    -   像素著色器

        -   作為 PS 輸入的涵蓋範圍
        -   可程式化輸入的內插補點-圖元著色器可以評估圖元內的屬性，在 [取樣] 方格上的任何位置
        -   屬性的距心取樣必須遵守下列規則：

            -   如果涵蓋了基本型別中的所有樣本，則不論範例模式是否在圖元中心都有範例位置，屬性都會在圖元中心進行評估。
            -   否則，會在第一個涵蓋的範例中評估屬性，也就是在所有範例索引之間具有最低索引的範例。 在此情況下，會在將邏輯 AND 運算套用至涵蓋範圍和樣本遮罩轉譯器狀態之後，判斷範例涵蓋範圍。
            -   如果未涵蓋任何樣本 (例如，在協助程式圖元上執行，以填滿2x2 圖元戳記) 的協助程式圖元，則會以下列其中一種方式評估屬性：

                -   如果範例遮罩轉譯器的狀態是圖元中樣本的子集，則範例遮罩轉譯器狀態所涵蓋的第一個範例就是評估點。
                -   否則，在完整的範例遮罩條件中，圖元中心就是評估點。

-   Direct3D 11 展開材質 (請參閱 [材質總覽](overviews-direct3d-11-resources-textures.md)) ，其中包含下列功能

    -   Gather4

        -   支援多元件紋理-指定要載入的通道
        -   支援可程式化位移

    -   串流

        -   用來限制 WDDM 預先載入的材質個

    -   16K 材質限制
    -   紋理篩選需要8位的 subtexel 和子 mip 精確度
    -   新的材質壓縮格式 (1 個新的 LDR 格式和1個新的 HDR 格式) 

-   Direct3D 11 支援保守 oDepth-此演算法可讓圖元著色器比較圖元著色器的每圖元深度值與轉譯器中的圖元著色器。 結果可進行早期的剔除作業，同時維持從圖元著色器輸出 oDepth 的能力。
-   Direct3D 11 支援大型記憶體

    -   允許資源 > 4GB
    -   將資源的索引保持在32位，但資源較大

-   Direct3D 11 支援資料流程輸出改進

    -   可定址的資料流程輸出
    -   將資料流程輸出計數增加至4
    -   將所有資料流程輸出緩衝區變更為多元素

-   Direct3D 11 支援著色器模型 5 (請參閱 [著色器模型 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)) 

    -   使用 denorms 的雙精度浮點數
    -   Count 位 set 指令
    -   尋找第一個位設定指令
    -   執行/溢位處理
    -   FFTs 的位反轉指示
    -   條件式交換內建函式
    -   緩衝區上的 Resinfo
    -   降低精確度的倒數
    -   著色器轉換指示-fp16 至 fp32，反之亦然
    -   結構化緩衝區，這是包含結構化元素的新緩衝區類型。

-   Direct3D 11 支援唯讀深度或樣板視圖

    -   停用唯讀元件的寫入，並允許使用材質作為輸入和深度剔除

-   Direct3D 11 支援繪製間接 Direct3D 10 實 DrawAuto，它會取得 GPU) 所產生的內容 (，並將其呈現 (在 GPU) 上。 Direct3D 11 一般化 DrawAuto，使其可由使用 DrawInstanced 和 DrawIndexedInstanced 的計算著色器來呼叫。
-   Direct3D 11 支援其他功能

    -   浮點數區
    -   每一資源 mipmap 固定
    -   深度偏差-此演算法會使用轉譯器狀態來更新深度偏差的行為。 結果會排除計算偏差可能是 NaN 的案例。
    -   資源限制-資源索引仍然需要 <= 32 位，但資源可能大於 4 GB。
    -   轉譯器精確度
    -   MSAA 需求
    -   計數器減少
    -   已移除1位格式和文字篩選

## <a name="features-added-in-previous-releases"></a>先前版本中新增的功能

如需先前版本中新增的功能清單，請參閱下列主題：

-   [2009年8月 Windows 7/Direct3D 11 SDK 的新功能](dx11-whats-new.md)
-   [2008年11月版 Direct3D 11 Technical Preview 的新功能](dx11-08nov-whats-new.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 的新功能](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 