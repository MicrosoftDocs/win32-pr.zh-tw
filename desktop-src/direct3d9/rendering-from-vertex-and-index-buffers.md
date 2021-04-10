---
description: Direct3D 支援索引和非索引的繪圖方法。
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: '從頂點和索引緩衝區轉譯 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845960"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>從頂點和索引緩衝區轉譯 (Direct3D 9) 

Direct3D 支援索引和非索引的繪圖方法。 索引的方法會針對所有頂點元件使用一組索引。 頂點資料會儲存在頂點緩衝區中，而索引資料會儲存在索引緩衝區中。 以下列出使用頂點和索引緩衝區繪製基本專案的一些常見案例。

這些範例會比較 IDirect3DDevice9 的使用 [**：:D rawprimitive**](/windows/desktop/api) 和 [**IDirect3DDevice9：:D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>案例1：繪製兩個三角形但不編制索引

假設您想要繪製下圖所示的四顆四個。

![由兩個三角形組成的正方形圖例](images/dip-fig1.png)

如果您使用三角形清單基本型別來呈現兩個三角形，每個三角形都會儲存為3個個別頂點，並產生類似的頂點緩衝區給下圖。

![頂點緩衝區的圖表，定義兩個三角形的三個頂點](images/dip-fig2.png)

繪圖呼叫很簡單;從頂點緩衝區內的位置0開始，繪製兩個三角形。 如果已啟用 [剔除]，頂點的順序將會很重要。 此範例假設預設的逆時針剔除狀態，因此必須以順時針順序繪製可見的三角形。 三角形清單基本型別直接從每個三角形的緩衝區讀取三個頂點，因此此呼叫會繪製三角形 (0、1、2) 和 (3、4、5) ：


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>案例2：繪製具有索引的兩個三角形

您將會注意到，頂點緩衝區包含位置0和4、2和5中的重復資料。 這是合理的，因為這兩個三角形共用兩個共通頂點。 這項重複的資料很浪費，而且可以使用索引緩衝區來壓縮頂點緩衝區。 較小的頂點緩衝區可減少必須傳送至圖形介面卡的頂點資料量。 更重要的是，使用索引緩衝區可讓介面卡在頂點快取中儲存頂點;如果所繪製的基本物件包含最近使用的頂點，則可以從快取中提取該頂點，而不是從頂點緩衝區中讀取，這會導致大幅提升效能。

索引緩衝區在頂點緩衝區中的索引，因此每個唯一頂點都只需要在頂點緩衝區中儲存一次。 下圖顯示先前繪圖案例的索引方法。

![先前頂點緩衝區的索引緩衝區圖表](images/dip-fig3.png)

索引緩衝區會儲存 VB 索引值，而這些值會參考頂點緩衝區內的特定頂點。 頂點緩衝區可以視為頂點的陣列，因此 VB 索引只是目標頂點之頂點緩衝區中的索引。 同樣地，IB 索引是索引緩衝區中的索引。 如果您不小心，這可能會非常混淆，因此請確定您已清楚使用的詞彙：在頂點緩衝區中使用 VB 索引值索引、將 IB 索引值索引放入索引緩衝區，以及索引緩衝區本身儲存 VB 索引值。

繪圖呼叫如下所示。 在下一個繪製案例中，所有引數的意義都會以最長的時間進行討論;現在，請注意，此呼叫會再次指示 Direct3D 轉譯包含兩個三角形的三角形清單（從索引緩衝區中的位置0開始）。 此呼叫會以與之前完全相同的順序繪製相同的兩個三角形，以確保適當的順時針方向：


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>案例3：使用索引繪製一個三角形

假設您現在只想要繪製第二個三角形，但是您想要使用繪製整個四個時所使用的相同頂點緩衝區和索引緩衝區，如下圖所示。

![第二個三角形的索引緩衝區和頂點緩衝區圖表](images/dip-fig4.png)

針對此繪製呼叫，第一個使用的 IB 索引為 3;此值稱為 StartIndex。 使用的最低 VB 索引為 0;此值稱為 MinIndex。 雖然繪製三角形只需要三個頂點，但這三個頂點會散佈到頂點緩衝區中的四個相鄰位置;繪製呼叫所需的相鄰頂點緩衝區記憶體區塊中的位置數目稱為 NumVertices，在此呼叫中將設定為4。 MinIndex 和 NumVertices 值其實只是協助 Direct3D 在軟體頂點處理期間優化記憶體存取的提示，而且可以直接設定為包含整個頂點緩衝區（以效能的價格為限）。

以下是單一三角形案例的繪圖呼叫;接下來會說明 BaseVertexIndex 引數的意義：


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>案例4：使用位移索引繪製一個三角形

BaseVertexIndex 是一個值，可有效地新增至儲存在索引緩衝區中的每個 VB 索引。 例如，如果我們在上一個呼叫期間為 BaseVertexIndex 傳遞的值為50，則在 DrawIndexedPrimitive 呼叫的持續時間內，其功能與使用下圖中的索引緩衝區相同：

![索引緩衝區的圖表，其值為50表示 basevertexindex](images/dip-fig5.png)

此值很少會設定為0以外的任何值，但如果您想要將索引緩衝區與頂點緩衝區分離，則會很有用：如果在特定網格中填入索引緩衝區時，在頂點緩衝區內找不到網格的位置，您可以直接假裝網格頂點位於頂點緩衝區的開頭;當您需要進行繪製呼叫時，只要將實際的開始位置當作 BaseVertexIndex 傳遞。

這項技術也可以在使用單一索引緩衝區繪製多個網格實例時使用;例如，如果頂點緩衝區包含兩個具有相同繪製順序但不同頂點 (可能有不同的擴散色彩或紋理座標) 的網格，則可以使用不同的 BaseVertexIndex 值來繪製這兩個格線。 進一步瞭解這個概念，您可以使用一個索引緩衝區來繪製網格的多個實例，每個實例都包含在不同的頂點緩衝區中，只要迴圈的是作用中的頂點緩衝區，然後視需要調整 BaseVertexIndex。 請注意，BaseVertexIndex 值也會自動加入至 MinIndex 引數，這在您看到其使用方式時很合理：

假設我們現在再次想要使用與之前相同的索引緩衝區來繪製四個四個三角形;不過，在使用不同的頂點緩衝區時，四位在 VB 索引50。 四個頂點的相對順序保持不變，只有頂點緩衝區內的起始位置不同。 索引緩衝區和頂點緩衝區看起來如下圖所示。

![具有 vb 索引50的索引緩衝區和頂點緩衝區圖表](images/dip-fig6.png)

以下是適當的繪製呼叫;請注意，BaseVertexIndex 是從上一個案例中變更的唯一值：


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[呈現基本專案](rendering-primitives.md)
</dt> </dl>

 

 
