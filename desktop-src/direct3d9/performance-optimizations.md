---
description: 建立使用3D 圖形之即時應用程式的每位開發人員都關心效能優化。 本節提供從程式碼取得最佳效能的指導方針。
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: " (Direct3D 9) 的效能優化"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e22ff22e3cde3673a1fc5ccd1da1bdccd95c6a094d670f59742178b28954773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520425"
---
# <a name="performance-optimizations-direct3d-9"></a> (Direct3D 9) 的效能優化

建立使用3D 圖形之即時應用程式的每位開發人員都關心效能優化。 本節提供從程式碼取得最佳效能的指導方針。

-   [一般效能提示](#general-performance-tips)
-   [資料庫和剔除](#databases-and-culling)
-   [批次處理基本專案](#batching-primitives)
-   [光源提示](#lighting-tips)
-   [材質大小](#texture-size)
-   [矩陣轉換](#matrix-transforms)
-   [使用動態紋理](#using-dynamic-textures)
-   [使用動態頂點和索引緩衝區](#using-dynamic-vertex-and-index-buffers)
-   [使用網格](#using-meshes)
-   [Z 緩衝區效能](#z-buffer-performance)

## <a name="general-performance-tips"></a>一般效能提示

-   只有在您必須時才清除。
-   將狀態變更降至最低，並將剩餘的狀態變更為群組。
-   如果您可以，請使用較小的紋理。
-   從前方到上一頁繪製場景中的物件。
-   使用三角形的停車線，而不是清單和風扇。 為了獲得最佳的頂點快取效能，請將帶狀排列成更快重複使用三角形頂點，而不是稍後使用。
-   正常降低需要不相稱的系統資源分享的特殊效果。
-   持續測試您的應用程式效能。
-   最小化頂點緩衝區參數。
-   盡可能使用靜態頂點緩衝區。
-   針對靜態物件，每個 FVF 使用一個大型靜態頂點緩衝區，而不是每個物件一個。
-   如果您的應用程式需要隨機存取 AGP 記憶體中的頂點緩衝區，請選擇屬於32個位元組倍數的頂點格式大小。 否則，請選取最小的適當格式。
-   使用索引基本專案繪製。 這可讓您在硬體內有更有效率的頂點快取。
-   如果深度緩衝區格式包含樣板通道，請一律同時清除深度和樣板通道。
-   盡可能結合著色器指令和資料輸出。 例如：
    ```
    // Rather than doing a multiply and add, and then output the data with 
    //   two instructions:
    mad r2, r1, v0, c0
    mov oD0, r2

    // Combine both in a single instruction, because this eliminates an  
    //   additional register copy.
    mad oD0, r1, v0, c0 
    ```

    

## <a name="databases-and-culling"></a>資料庫和剔除

在您的世界中建立可靠的物件資料庫，是 Direct3D 中絕佳效能的關鍵。 它比對柵格化或硬體的改進更為重要。

您應維持可能管理的最小多邊形計數。 從頭開始建立低多邊形模型，以設計較低的多邊形計數。 如果您這樣做，請新增多邊形，而不會在開發過程中犧牲效能。 請記住，最快的多邊形是您未繪製的多邊形。

## <a name="batching-primitives"></a>批次處理基本專案

若要在執行期間取得最佳轉譯效能，請嘗試以批次方式處理基本專案，並盡可能減少轉譯狀態變更的數目。 例如，如果您有一個具有兩個材質的物件，請將使用第一個材質的三角形分組，並依照所需的轉譯狀態來變更材質。 然後，將使用第二個材質的所有三角形分組。 最簡單的 Direct3D 硬體支援是透過硬體抽象層（ (HAL) ），以批次呈現狀態和基本專案的批次來呼叫。 更有效地批處理指示，執行期間會執行較少的 HAL 呼叫。

## <a name="lighting-tips"></a>光源提示

由於燈光會將每個頂點的成本加入至每個呈現的框架，因此您可以在應用程式中使用它們，以大幅改善效能。 下列大部分的秘訣都是衍生自背道而馳「最快的程式碼是永遠不會呼叫的程式碼」。

-   盡可能使用較少的輕量來源。 例如，若要提高整體光源層級，請使用環境光源，而不是加入新的燈光來源。
-   方向光線比點燈或聚光燈更有效率。 針對方向光源，光的方向是固定的，而且不需要以每個頂點為基礎來計算。
-   聚光燈的結果可能比點燈更有效率，因為光線的範圍外的區域會快速計算。 聚光燈是否更有效率，而不會取決於焦點在您的場景中的程度。
-   您可以使用 range 參數，將您的燈光限制為只有您需要照亮的場景部分。 所有的光線類型在超出範圍時，就會相當早結束。
-   反光幾乎會醒目顯示光線成本的兩倍。 只有在您必須時才使用它們。 盡可能將 D3DRS \_ SPECULARENABLE 轉譯狀態設定為0（預設值）。 定義材質時，您必須將反射功率值設定為零，以關閉該材質的高光。只是將反射色彩設定為0、0、0就夠了。

## <a name="texture-size"></a>材質大小

紋理對應效能與記憶體的速度非常相關。 有數種方式可將應用程式材質的快取效能最大化。

-   讓紋理保持小。 紋理越小，就可以在主要 CPU 的次要快取中維護更好的機會。
-   請勿變更每個基本的材質。 請嘗試將多邊形依其使用的紋理順序分組。
-   盡可能使用正方形紋理。 其維度為256x256 的紋理最快。 例如，如果您的應用程式使用四個128x128 材質，請試著確定它們使用相同的調色板，並將它們全部放在一個256x256 材質中。 這項技術也可減少材質交換的量。 當然，除非您的應用程式需要太多紋理，否則除非您的應用程式需要太多紋理，否則您不應該使用256x256 紋理。

## <a name="matrix-transforms"></a>矩陣轉換

Direct3D 使用世界和檢視矩陣，讓您設定數個內部資料結構。 每當您設定世界或檢視矩陣，系統會重新計算相關內部結構。 頻繁地設定這些矩陣（例如，每個框架上千次）都是計算時間耗用量。 您可以串連世界和檢視矩陣成為世界檢視矩陣 (您將其設為世界矩陣)，然後將檢視矩陣設為單位矩陣，將所需的計算次數最小化。 保留個別世界和檢視矩陣的快取複本，讓您可以視需要修改、串連並重設世界矩陣。 為了清楚起見，在本檔中，Direct3D 範例很少使用這項優化。

## <a name="using-dynamic-textures"></a>使用動態紋理

若要查明驅動程式是否支援動態材質，請檢查 \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 D3DCAPS2 DYNAMICTEXTURES 旗標。

使用動態紋理時，請記住下列事項。

-   無法進行管理。 例如，其集區無法 D3DPOOL \_ 管理。
-   動態紋理可以鎖定，即使它們是在 D3DPOOL 預設中建立的 \_ 。
-   D3DLOCK \_ 捨棄是動態紋理的有效鎖定旗標。

最好只針對每一種格式建立一個動態材質，而且可能會依大小來建立。 由於鎖定每個層級的額外負荷，因此不建議使用動態 mipmap、cube 和磁片區。 若為 mipmap， \_ 則只允許在最上層使用 D3DLOCK 捨棄。 只要鎖定最上層，就會捨棄所有層級。 此行為對於磁片區和 cube 而言是相同的。 針對 cube，最上層和臉部0會被鎖定。

下列虛擬程式碼顯示使用動態材質的範例。


```
DrawProceduralTexture(pTex)
{
    // pTex should not be very small because overhead of 
    //   calling driver every D3DLOCK_DISCARD will not 
    //   justify the performance gain. Experimentation is encouraged.
    pTex->Lock(D3DLOCK_DISCARD);
    <Overwrite *entire* texture>
    pTex->Unlock();
    pDev->SetTexture();
    pDev->DrawPrimitive();
}
```



## <a name="using-dynamic-vertex-and-index-buffers"></a>使用動態頂點和索引緩衝區

當圖形處理器使用緩衝區時，鎖定靜態頂點緩衝區可能會對效能造成顯著的影響。 鎖定呼叫必須等到圖形處理器從緩衝區讀取頂點或索引資料之後，才可以傳回給呼叫的應用程式，這會造成嚴重的延遲。 針對每個畫面格的靜態緩衝區進行鎖定，然後再進行轉譯，也可防止圖形處理器緩衝轉譯命令，因為它必須在傳回鎖定指標之前完成命令。 如果沒有緩衝的命令，圖形處理器會維持閒置，直到應用程式完成填滿頂點緩衝區或索引緩衝區併發出轉譯命令為止。

在理想的情況下，頂點或索引資料永遠不會變更，不過這不一定是可行的。 在許多情況下，應用程式需要在每個框架中變更頂點或索引資料，甚至是每個框架的次數。 在這些情況下，應該使用 D3DUSAGE 動態來建立頂點或索引緩衝區 \_ 。 此使用旗標會導致 Direct3D 針對頻繁的鎖定作業進行優化。 D3DUSAGE \_ DYNAMIC 只適用于經常鎖定緩衝區的情況; 保持不變的資料應放置在靜態頂點或索引緩衝區中。

若要在使用動態頂點緩衝區時獲得效能改進，應用程式必須使用適當的旗標來呼叫 [**IDirect3DVertexBuffer9：： lock**](/windows/desktop/api) 或 [**IDirect3DIndexBuffer9：： lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) 。 D3DLOCK \_ 捨棄表示應用程式不需要將舊的頂點或索引資料保留在緩衝區中。 如果使用 D3DLOCK 捨棄呼叫鎖定時，圖形處理器仍在使用緩衝區 \_ ，則會傳回新記憶體區域的指標，而不是舊的緩衝區資料。 這可讓圖形處理器在應用程式將資料放在新的緩衝區時，繼續使用舊的資料。 應用程式不需要額外的記憶體管理;當圖形處理器已完成時，舊的緩衝區會自動重複使用或損毀。 請注意，使用 D3DLOCK 捨棄來鎖定緩衝區 \_ 一律會捨棄整個緩衝區，指定非零位移或受限大小欄位不會在緩衝區的已解除鎖定區域中保留資訊。

在某些情況下，應用程式每個鎖定所需儲存的資料量很小，例如新增四個頂點來轉譯 sprite。 D3DLOCK \_ NOOVERWRITE 表示應用程式不會覆寫動態緩衝區中已在使用中的資料。 鎖定呼叫會傳回舊資料的指標，讓應用程式在頂點或索引緩衝區未使用的區域中加入新的資料。 應用程式不應該修改繪製作業中使用的頂點或索引，因為它們可能仍由圖形處理器使用中。 然後，應用程式應該在 \_ 動態緩衝區已滿時使用 D3DLOCK 捨棄，以接收新的記憶體區域，然後在圖形處理器完成後捨棄舊的頂點或索引資料。

非同步查詢機制很適合用來判斷圖形處理器是否仍在使用頂點。 \_在最後一個使用頂點的 DrawPrimitive 呼叫之後發出類型 D3DQUERYTYPE 事件的查詢。 當 [**IDirect3DQuery9：：：：：：**](/windows/desktop/api) 時，不會再使用頂點 \_ 。 使用 D3DLOCK \_ 捨棄或沒有旗標來鎖定緩衝區，一律保證頂點會與圖形處理器正確地同步處理，不過，使用沒有旗標的鎖定將會產生稍早所述的效能負面影響。 其他 API 呼叫（例如 [**IDirect3DDevice9：： BeginScene**](/windows/desktop/api)、 [**IDirect3DDevice9：： EndScene**](/windows/desktop/api)和 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 重新傳送）不保證圖形處理器已使用頂點完成。

以下是使用動態緩衝區和適當鎖定旗標的方式。


```
    // USAGE STYLE 1
    // Discard the entire vertex buffer and refill with thousands of vertices.
    // Might contain multiple objects and/or require multiple DrawPrimitive 
    //   calls separated by state changes, etc.
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // Discard and refill the used portion of the vertex buffer.
    CONST DWORD dwLockFlags = D3DLOCK_DISCARD;
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( 0, 0, &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, nNumberOfVertices/3)
```




```
    // USAGE STYLE 2
    // Reusing one vertex buffer for multiple objects
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // No overwrite will be used if the vertices can fit into 
    //   the space remaining in the vertex buffer.
    DWORD dwLockFlags = D3DLOCK_NOOVERWRITE;
    
    // Check to see if the entire vertex buffer has been used up yet.
    if( m_nNextVertexData > m_nSizeOfVB - nSizeOfData )
    {
        // No space remains. Start over from the beginning 
        //   of the vertex buffer.
        dwLockFlags = D3DLOCK_DISCARD;
        m_nNextVertexData = 0;
    }
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( (UINT)m_nNextVertexData, nSizeOfData, 
               &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 
               m_nNextVertexData/m_nVertexStride, nNumberOfVertices/3)
 
    // Advance to the next position in the vertex buffer.
    m_nNextVertexData += nSizeOfData;
```



## <a name="using-meshes"></a>使用網格

您可以使用 Direct3D 索引三角形來優化網格，而不是使用索引的三角形。 硬體會發現連續三角形的95% 其實形成條紋並據以調整。 許多驅動程式也適用于較舊的硬體。

D3DX 網格物件可以有標記有 DWORD 的每個三角形（或臉部），稱為該臉部的屬性。 DWORD 的語法是使用者定義的。 D3DX 會使用它們來將網格分類為子集。 應用程式會使用 [**ID3DXMesh：： LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md) 呼叫來設定每一臉部屬性。 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md)方法有一個選項，可使用 D3DXMESHOPT ATTRSORT 選項，將網格頂點和屬性的臉部群組在一起 \_ 。 完成此動作時，網格物件會計算可透過呼叫 [**ID3DXBaseMesh：： GetAttributeTable**](id3dxbasemesh--getattributetable.md)來取得應用程式的屬性資料表。 如果網格未依屬性排序，此呼叫會傳回0。 應用程式無法設定屬性資料表，因為它是由 **ID3DXMesh：： Optimize** 方法所產生。 屬性排序會區分資料，因此，如果應用程式知道網格的屬性已排序，它仍然需要呼叫 **ID3DXMesh：： Optimize** 來產生屬性資料表。

下列主題描述網格的不同屬性。

### <a name="attribute-id"></a>屬性識別碼

屬性識別碼是一個值，可將臉部群組與屬性群組產生關聯。 此識別碼描述 ID3DXBaseMesh 應繪製哪些臉部子集 [**：:D rawsubset**](id3dxbasemesh--drawsubset.md) 。 屬性緩衝區中的臉部會指定屬性識別碼。 屬性識別碼的實際值可以是任何符合32位的元素，但通常會使用0到 n，其中 n 是屬性的數目。

### <a name="attribute-buffer"></a>屬性緩衝區

屬性緩衝區是一個 Dword 陣列 (每個臉部) 一個，指定每個臉部所屬的屬性群組。 在建立網格時，此緩衝區會初始化為零，但會由載入常式填滿，如果需要多個識別符為0的屬性，則必須由使用者填入。 此緩衝區包含用來根據 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md)中的屬性來排序網格的資訊。 如果沒有屬性工作表存在， [**ID3DXBaseMesh：:D rawsubset**](id3dxbasemesh--drawsubset.md) 會掃描這個緩衝區，以選取要繪製之指定屬性的臉部。

### <a name="attribute-table"></a>屬性工作表

屬性工作表是網格所擁有及維護的結構。 唯一要產生的方法，是藉由呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) with 屬性排序或增強的優化功能。 屬性工作表用來快速起始對 [**ID3DXBaseMesh：:D rawsubset**](id3dxbasemesh--drawsubset.md)的單一繪製基本呼叫。 唯一的用法是，執行中的網格也會維持此結構，因此您可以在目前的詳細資料層級查看有哪些臉部和頂點處於作用中。

## <a name="z-buffer-performance"></a>Z 緩衝區效能

使用 z 緩衝和紋理處理時，應用程式可提高效能，藉由確保場景從前到後轉譯。 有紋理的 z 緩衝基本類型會針對 z 緩衝區預先測試，以掃描列為基礎。 如果掃描列被掀錢轉譯的多邊形隱藏，系統會快速且有效率地拒絕它。 Z 緩衝可以提升效能，但此技術在場景多次繪製相同像素時最實用。 這很難精確計算，但是您通常可以算出近似值。 如果相同像素繪製少於兩次，將 z 緩衝關閉並從後到前轉譯場景，將可達到最佳效能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計提示](programming-tips.md)
</dt> </dl>

 

 
