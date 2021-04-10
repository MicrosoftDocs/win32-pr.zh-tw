---
description: D3DX 公用程式程式庫會提供 ID3DXMATRIXStack 介面。
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: " (Direct3D 9) 的矩陣堆疊"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d535307fb99d8743b910f2f3f8c6d55e197748e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846420"
---
# <a name="matrix-stacks-direct3d-9"></a> (Direct3D 9) 的矩陣堆疊

D3DX 公用程式程式庫會提供 [**ID3DXMATRIXStack**](id3dxmatrixstack.md) 介面。 它會提供一種機制，讓矩陣可推送至矩陣堆疊並將其向外快顯。 在遍歷轉換階層時，執行矩陣堆疊是追蹤矩陣的有效方式。

D3DX 公用程式程式庫會使用矩陣堆疊來將轉換儲存為矩陣。 [**ID3DXMATRIXStack**](id3dxmatrixstack.md)介面的各種方法會處理目前的矩陣，或位於堆疊頂端的矩陣。 您可以使用 [**ID3DXMATRIXStack：： LoadIdentity**](id3dxmatrixstack--loadidentity.md) 方法清除目前的矩陣。 若要明確指定要載入為目前轉換矩陣的特定矩陣，請使用 [**ID3DXMATRIXStack：： LoadMatrix**](id3dxmatrixstack--loadmatrix.md) 方法。 然後您可以呼叫 [**ID3DXMATRIXStack：： MultMatrix**](id3dxmatrixstack--multmatrix.md) 方法或 [**ID3DXMATRIXStack：： MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) 方法，以將目前的矩陣乘以指定的矩陣。

[**ID3DXMATRIXStack：:P op**](id3dxmatrixstack--pop.md)方法可讓您回到上一個轉換矩陣， [**ID3DXMATRIXStack：:P ush**](id3dxmatrixstack--push.md)方法會將轉換矩陣新增至堆疊。

矩陣堆疊上的個別矩陣表示為4x4 個同質矩陣，由 D3DX 公用程式程式庫 [**D3DXMATRIX**](d3dxmatrix.md) 結構定義。

D3DX 公用程式程式庫會透過元件物件模型 (COM) 物件來提供矩陣堆疊。

## <a name="implementing-a-scene-hierarchy"></a>執行場景階層

矩陣堆疊可簡化階層式模型的結構，其中複雜的物件是由一系列簡單的物件所構成。

場景或轉換通常是由樹狀結構資料結構來表示。 樹狀結構資料結構中的每個節點都包含一個矩陣。 特定矩陣表示從節點的父節點到節點的座標系統變更。 例如，如果您正在建立人工 arm 模型，您可以執行下圖所示的階層。

![人類 arm 階層的圖表](images/stack1.png)

在此階層中，內文矩陣會將主體放在世界各地。 UpperArm 矩陣包含了肩的旋轉、LowerArm 矩陣包含肘的旋轉，而手矩陣則包含手腕的旋轉。 若要判斷手上相對於世界的地方，您可以將所有的矩陣從內文中將所有矩陣相乘。

先前的階層過於簡化，因為每個節點只有一個子系。 如果您開始更詳細地建立模型的模型，您可能會加入手指和 thumb。 您可以將每個數位新增至階層作為手形的子系，如下圖所示。

![人工階層的圖表](images/stack2.png)

如果您在移至下一個路徑之前，先將 arm 的完整圖形以深度優先順序往返至最低的路徑，請執行一連串的分段轉譯。 例如，若要呈現手邊和手指，請執行下列模式。

1.  將手矩陣推送至矩陣堆疊。
2.  畫手。
3.  將 Thumb 矩陣推送至矩陣堆疊。
4.  繪製 thumb。
5.  將 Thumb 矩陣從堆疊中取出。
6.  將手指1矩陣推送至矩陣堆疊。
7.  繪製第一個手指。
8.  將指標1矩陣從堆疊中取出。
9.  將手指2矩陣推送至矩陣堆疊。 您可以用這種方式繼續進行，直到轉譯所有手指和 thumb 為止。

在您完成手指的呈現之後，您會將該牌從堆疊中取出。

您可以使用下列範例，在程式碼中執行這個基本程式。 當您在樹狀結構資料結構的深度優先搜尋期間遇到節點時，請將矩陣推送至矩陣堆疊的頂端。


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



當您完成節點時，請將矩陣從矩陣堆疊的頂端取出。


```
MatrixStack->Pop();
```



如此一來，堆疊頂端的矩陣一律代表目前節點的世界轉換。 因此，在繪製每個節點之前，您應該先設定 Direct3D 矩陣。


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



如需有關您可以在 D3DX 矩陣堆疊上執行之特定方法的詳細資訊，請參閱 [**ID3DXMATRIXStack**](id3dxmatrixstack.md) 參考主題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點管線](vertex-pipeline.md)
</dt> </dl>

 

 



