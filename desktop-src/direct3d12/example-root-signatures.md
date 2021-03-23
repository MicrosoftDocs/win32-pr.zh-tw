---
title: 範例根簽章
description: 下一節顯示從空白到完全完整的根目錄簽章變化。
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103785"
---
# <a name="example-root-signatures"></a>範例根簽章

下一節顯示從空白到完全完整的根目錄簽章變化。

-   [空白的根簽章](#an-empty-root-signature)
-   [一個常數](#one-constant)
-   [加入根常數緩衝區視圖](#adding-a-root-constant-buffer-view)
-   [系結描述中繼資料表](#binding-descriptor-tables)
-   [更複雜的根簽章](#a-more-complex-root-signature)
-   [串流著色器資源檢視](#streaming-shader-resource-views)
-   [相關主題](#related-topics)

## <a name="an-empty-root-signature"></a>空白的根簽章

![空白的根簽章沒有系結](images/root-tables-0.png)

空白的根簽章不太可能有用，但可用於只使用輸入組合語言的簡單轉譯階段，以及不會存取任何描述項的最小頂點和圖元著色器。 此外，也可以使用 blend 階段、轉譯目標和深度樣板階段，即使是空的根簽章也是一樣。

## <a name="one-constant"></a>一個常數

![單一根常數](images/root-tables-constant.png)

API 系結位置是此參數的根引數會在命令清單記錄時間進行系結。 API 系結位置的數目是隱含的，根據根簽章中的參數順序 (第一個一律為零) 。 HLSL 系結位置是著色器會看到根參數顯示的位置。 上述) 範例中的 "uint" ( 類型對硬體而言是未知的，但只是映射中的批註，而硬體只會看到單一 DWORD 作為內容。

若要在命令清單記錄時間系結常數，請使用類似下列的命令：

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a>加入根常數緩衝區視圖

![將常數緩衝區視圖新增至根簽章](images/root-tables-cbv.png)

此範例顯示兩個根常數，而根常數緩衝區視圖 (CBV 成本為兩個 DWORD 位置的) 。

若要系結常數緩衝區視圖，請使用下列命令： 請注意，第一個參數 (2) 是影像中所顯示的位置。 通常會設定常數陣列，然後以 CBV 形式提供給 b0 的著色器。

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a>系結描述中繼資料表

![將描述中繼資料表新增至根簽章](images/root-tables-2.png)

此範例示範如何使用兩個描述中繼資料表;其中一個宣告可在執行時間于 CBV SRV UAV 描述元堆積中使用的五個描述項的資料表 \_ \_ ，以及另一個宣告兩個描述項的資料表，這些描述項將在執行時間于取樣器描述元堆積中顯示。

在記錄命令清單時系結描述項資料表。

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

根簽章的另一項功能是 float4 的根常數，大小為四個 DWORD。 下列命令只會系結四的中間兩個 DWORD。

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a>更複雜的根簽章

![具有許多元素的複雜根簽章](images/root-tables-3.png)

此範例顯示具有大部分專案類型的密集根簽章。 兩個描述項資料表 (在插槽3和 6) 包含未系結的大小陣列。 這裡的負擔在於應用程式只能在堆積中接觸有效的描述項。 無限制或非常大型的陣列，需要硬體層 2 + 資源系結支援。

有兩個靜態取樣器 (系結，而不需要) 的根簽章位置。

在插槽9，UAV u4 和 UAV u5 是在相同的描述項資料表位移中宣告。 這是使用別名描述項，記憶體中的一個描述項在 HLSL 著色器中會顯示為 u4 和 u5。 在此情況下，必須使用 D3D10 \_ 著色器資源的 \_ \_ \_ 別名選項或 `/res_may_alias` fxc.exe 中的或選項來編譯著色器。 別名描述項可讓一個描述元系結至多個系結點，而不需要對著色器進行任何變更。

## <a name="streaming-shader-resource-views"></a>串流著色器資源檢視

![此根簽章中的串流著色器資源瀏覽器](images/root-tables-4.png)

此根簽章說明將所有 SRVs 流入和移出一個大型陣列的案例。 在執行時間，當設定根簽章時，可以設定描述中繼資料表一次。 然後透過前幾個根引數所送出的常數，在陣列中編制所有材質讀取的功能。 只需要單一描述元堆積，而且只會在有可用的描述項位置或流出紋理時進行更新。

大型堆積中的描述項位移是使用常數緩衝區視圖中的常數，以著色器來識別。 例如，如果為著色器指定了材質識別碼，它可以使用常數來索引至一個大型陣列，以存取所需的描述項 (參考所需的材質) 。

此案例需要具有資源系結第2層 + 的硬體。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源系結硬體層](hardware-support.md)
</dt> <dt>

[HLSL 中的資源系結](resource-binding-in-hlsl.md)
</dt> <dt>

[根簽章](root-signatures.md)
</dt> </dl>

 

 




