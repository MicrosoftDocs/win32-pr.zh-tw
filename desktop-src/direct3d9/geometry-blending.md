---
description: Direct3D 可讓應用程式藉由轉譯分割的多邊形物件（特別是字元）來提高其幕後的本質，而這些物件具有順暢的混合接點。
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: " (Direct3D 9) 的幾何混合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71bb449b592c69ae2cf41487aef229718149eb4c1465d90f8b358d30458b69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122156"
---
# <a name="geometry-blending-direct3d-9"></a> (Direct3D 9) 的幾何混合

Direct3D 可讓應用程式藉由轉譯分割的多邊形物件（特別是字元）來提高其幕後的本質，而這些物件具有順暢的混合接點。 這些效果通常稱為「外觀」。 系統會藉由將額外的世界轉換矩陣套用至一組頂點來建立多個結果，然後在結果頂點之間執行線性 blend 來建立單一幾何集合，以達成此效果。 Banana 的下圖顯示此程式。

![將兩個物件與 banana 材質混合的流程圖例](images/geometry-blend.png)

上圖顯示您可能想像幾何混合進程的方式。 在單一轉譯呼叫中，系統會取得 banana 的頂點、將它們轉換兩次（不需要修改），並使用簡單的旋轉並混合結果來建立彎曲的 banana。 系統會混合頂點位置，以及啟用光源時的頂點法線。 應用程式不限於兩個混合路徑;Direct3D 可以 blend 多達四個世界矩陣，包括標準世界矩陣 [**D3DTS \_ 世界**](d3dts-world.md)。

> [!Note]
>
> 啟用光源時，會以對應的反向世界視圖矩陣（以與頂點位置計算相同的方式加權）來轉換頂點法線。 如果 D3DRS \_ NORMALIZENORMALS 轉譯狀態設為 **TRUE**，系統就會將產生的一般向量標準化。

 

如果沒有幾何混合，動態具現化的模型通常會在區段中呈現。 例如，請考慮使用人體 arm 的3D 模型。 在最簡單的觀點中，arm 有兩個部分：連線至內文的上層 arm，以及連線至手的較低 arm。 這兩個連接在肘線，而較低的 arm 會在該點旋轉。 轉譯 arm 的應用程式可能會保留上層和較低 arm 的頂點資料，每個都有不同的世界轉換矩陣。 下列程式碼範例會說明這點。


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



為了轉譯 arm，會進行兩個轉譯呼叫，如下列程式碼所示。


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



下圖是 banana，修改為使用這項技術。

![混合 banana 沒有幾何混合的圖例](images/noblend.png)

混合幾何和 nonblended 幾何之間的差異很明顯。 這個範例有點極端。 在真實世界的應用程式中，分割模型的接點是設計成讓接縫不太明顯。 不過，在某些情況下會顯示接縫，以呈現模型設計師的常數挑戰。

Direct3D 中的幾何混合提供傳統分段模型案例的替代方案。 不過，已改善的分段物件視覺品質會產生轉譯期間的混合計算成本。 為了將這些額外作業的影響降到最低，Direct3D 幾何管線已針對混合幾何進行優化，而且可能會產生最少的額外負荷。 使用 Direct3D 所提供之幾何混合服務的應用程式，可以改善其字元的真實性，同時避免嚴重的效能影響。

## <a name="blending-transform-and-render-states"></a>混合轉換和呈現狀態

[**IDirect3DDevice9：： SetTransform**](/windows/desktop/api)方法可辨識 [**D3DTS \_ WORLD**](d3dts-world.md)和 [**D3DTS \_ WORLDn**](d3dts-worldn.md)宏，這些宏對應到可由 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)巨集定義的值。 這些宏會用來識別將混合幾何的矩陣。

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)列舉型別包含 D3DRS \_ VERTEXBLEND 轉譯狀態，以啟用並控制幾何混合。 此呈現狀態的有效值是由 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 列舉型別所定義。 如果已啟用幾何混色，頂點格式必須包含適當的混色加權數目。

## <a name="blending-weights"></a>混合加權

混合權數（有時稱為測試加權）會控制指定的世界矩陣影響頂點的範圍。 混合權數是從0.0 到1.0 的浮點數，以頂點格式編碼，其中的值為0.0 表示頂點不會與該矩陣混合，而1.0 表示頂點會受到矩陣的完整影響。

幾何混合權數會以頂點格式編碼，並緊接在每個頂點的位置之後，如 [Fixed FUNCTION FVF 程式碼 (Direct3D 9) ](fixed-function-fvf-codes.md)中所述。 您可以藉由在您提供給轉譯方法的頂點描述中包含其中一個 [FVF 常數](d3dfvf.md) ，來傳達頂點格式的混色加權數目。

系統會在 blend 矩陣的加權結果之間執行線性 blend。 下列方程式是完整的混合公式。

![線性混合的方程式，使用世界轉換矩陣](images/vert-blend-formula.png)

在上述的方程式中，vBlend 是輸出頂點，v 元素是套用的世界矩陣所產生的頂點 ([**D3DTS \_ WORLDn**](d3dts-worldn.md)) 。 W 元素是頂點格式內對應的加權值。 在 n 個矩陣之間混合的頂點可以有-1 個混合加權值，每個混色矩陣各有一個，但最後一個除外。 系統會自動產生最後一個世界矩陣的權數，讓所有加權的總和都是1.0，以 sigma 標記法表示。 您可以針對 Direct3D 所支援的每個案例簡化此公式，如下列方程式所示。

![三種混色案例的線性混合方程式](images/vert-blend-formulas-simple.png)

這些是兩個、三個和四個 blend 矩陣案例的完整混合公式的簡化形式。

> [!Note]  
> 雖然 Direct3D 包含 FVF 描述項來定義最多有五個混色加權的頂點，但這一版的 DirectX 只能使用三個。

 

下列主題包含其他資訊。

-   [使用 (Direct3D 9) 的幾何混合 ](using-geometry-blending.md)
-   [ (Direct3D 9) 的索引頂點混合 ](indexed-vertex-blending.md)
-   [ (Direct3D 9) 的頂點補間 ](vertex-tweening.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點管線](vertex-pipeline.md)
</dt> </dl>

 

 
