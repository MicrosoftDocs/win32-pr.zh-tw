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
# <a name="matrix-stacks-direct3d-9"></a><span data-ttu-id="3e67b-103"> (Direct3D 9) 的矩陣堆疊</span><span class="sxs-lookup"><span data-stu-id="3e67b-103">Matrix Stacks (Direct3D 9)</span></span>

<span data-ttu-id="3e67b-104">D3DX 公用程式程式庫會提供 [**ID3DXMATRIXStack**](id3dxmatrixstack.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="3e67b-104">The D3DX utility library provides the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span> <span data-ttu-id="3e67b-105">它會提供一種機制，讓矩陣可推送至矩陣堆疊並將其向外快顯。</span><span class="sxs-lookup"><span data-stu-id="3e67b-105">It supplies a mechanism to enable matrices to be pushed onto and popped off of a matrix stack.</span></span> <span data-ttu-id="3e67b-106">在遍歷轉換階層時，執行矩陣堆疊是追蹤矩陣的有效方式。</span><span class="sxs-lookup"><span data-stu-id="3e67b-106">Implementing a matrix stack is an efficient way to track matrices while traversing a transform hierarchy.</span></span>

<span data-ttu-id="3e67b-107">D3DX 公用程式程式庫會使用矩陣堆疊來將轉換儲存為矩陣。</span><span class="sxs-lookup"><span data-stu-id="3e67b-107">The D3DX utility library uses a matrix stack to store transformations as matrices.</span></span> <span data-ttu-id="3e67b-108">[**ID3DXMATRIXStack**](id3dxmatrixstack.md)介面的各種方法會處理目前的矩陣，或位於堆疊頂端的矩陣。</span><span class="sxs-lookup"><span data-stu-id="3e67b-108">The various methods of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface deal with the current matrix, or the matrix located on top of the stack.</span></span> <span data-ttu-id="3e67b-109">您可以使用 [**ID3DXMATRIXStack：： LoadIdentity**](id3dxmatrixstack--loadidentity.md) 方法清除目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="3e67b-109">You can clear the current matrix with the [**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md) method.</span></span> <span data-ttu-id="3e67b-110">若要明確指定要載入為目前轉換矩陣的特定矩陣，請使用 [**ID3DXMATRIXStack：： LoadMatrix**](id3dxmatrixstack--loadmatrix.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3e67b-110">To explicitly specify a certain matrix to load as the current transformation matrix, use the [**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md) method.</span></span> <span data-ttu-id="3e67b-111">然後您可以呼叫 [**ID3DXMATRIXStack：： MultMatrix**](id3dxmatrixstack--multmatrix.md) 方法或 [**ID3DXMATRIXStack：： MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) 方法，以將目前的矩陣乘以指定的矩陣。</span><span class="sxs-lookup"><span data-stu-id="3e67b-111">Then you can call either the [**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md) method or the [**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) method to multiply the current matrix by the specified matrix.</span></span>

<span data-ttu-id="3e67b-112">[**ID3DXMATRIXStack：:P op**](id3dxmatrixstack--pop.md)方法可讓您回到上一個轉換矩陣， [**ID3DXMATRIXStack：:P ush**](id3dxmatrixstack--push.md)方法會將轉換矩陣新增至堆疊。</span><span class="sxs-lookup"><span data-stu-id="3e67b-112">The [**ID3DXMATRIXStack::Pop**](id3dxmatrixstack--pop.md) method enables you to return to the previous transformation matrix and the [**ID3DXMATRIXStack::Push**](id3dxmatrixstack--push.md) method adds a transformation matrix to the stack.</span></span>

<span data-ttu-id="3e67b-113">矩陣堆疊上的個別矩陣表示為4x4 個同質矩陣，由 D3DX 公用程式程式庫 [**D3DXMATRIX**](d3dxmatrix.md) 結構定義。</span><span class="sxs-lookup"><span data-stu-id="3e67b-113">The individual matrices on the matrix stack are represented as 4x4 homogeneous matrices, defined by the D3DX utility library [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

<span data-ttu-id="3e67b-114">D3DX 公用程式程式庫會透過元件物件模型 (COM) 物件來提供矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="3e67b-114">The D3DX utility library provides a matrix stack through a component object model (COM) object.</span></span>

## <a name="implementing-a-scene-hierarchy"></a><span data-ttu-id="3e67b-115">執行場景階層</span><span class="sxs-lookup"><span data-stu-id="3e67b-115">Implementing a Scene Hierarchy</span></span>

<span data-ttu-id="3e67b-116">矩陣堆疊可簡化階層式模型的結構，其中複雜的物件是由一系列簡單的物件所構成。</span><span class="sxs-lookup"><span data-stu-id="3e67b-116">A matrix stack simplifies the construction of hierarchical models, in which complicated objects are constructed from a series of simpler objects.</span></span>

<span data-ttu-id="3e67b-117">場景或轉換通常是由樹狀結構資料結構來表示。</span><span class="sxs-lookup"><span data-stu-id="3e67b-117">A scene, or transform, hierarchy is usually represented by a tree data structure.</span></span> <span data-ttu-id="3e67b-118">樹狀結構資料結構中的每個節點都包含一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="3e67b-118">Each node in the tree data structure contains a matrix.</span></span> <span data-ttu-id="3e67b-119">特定矩陣表示從節點的父節點到節點的座標系統變更。</span><span class="sxs-lookup"><span data-stu-id="3e67b-119">A particular matrix represents the change in coordinate systems from the node's parent to the node.</span></span> <span data-ttu-id="3e67b-120">例如，如果您正在建立人工 arm 模型，您可以執行下圖所示的階層。</span><span class="sxs-lookup"><span data-stu-id="3e67b-120">For example, if you are modeling a human arm, you might implement the hierarchy that is shown in the following diagram.</span></span>

![人類 arm 階層的圖表](images/stack1.png)

<span data-ttu-id="3e67b-122">在此階層中，內文矩陣會將主體放在世界各地。</span><span class="sxs-lookup"><span data-stu-id="3e67b-122">In this hierarchy, the Body matrix places the body in the world.</span></span> <span data-ttu-id="3e67b-123">UpperArm 矩陣包含了肩的旋轉、LowerArm 矩陣包含肘的旋轉，而手矩陣則包含手腕的旋轉。</span><span class="sxs-lookup"><span data-stu-id="3e67b-123">The UpperArm matrix contains the rotation of the shoulder, the LowerArm matrix contains the rotation of the elbow, and the Hand matrix contains the rotation of the wrist.</span></span> <span data-ttu-id="3e67b-124">若要判斷手上相對於世界的地方，您可以將所有的矩陣從內文中將所有矩陣相乘。</span><span class="sxs-lookup"><span data-stu-id="3e67b-124">To determine where the hand is relative to the world, you multiply all the matrices from Body down through Hand together.</span></span>

<span data-ttu-id="3e67b-125">先前的階層過於簡化，因為每個節點只有一個子系。</span><span class="sxs-lookup"><span data-stu-id="3e67b-125">The previous hierarchy is overly simplistic, because each node has only one child.</span></span> <span data-ttu-id="3e67b-126">如果您開始更詳細地建立模型的模型，您可能會加入手指和 thumb。</span><span class="sxs-lookup"><span data-stu-id="3e67b-126">If you begin to model the hand in more detail, you will probably add fingers and a thumb.</span></span> <span data-ttu-id="3e67b-127">您可以將每個數位新增至階層作為手形的子系，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="3e67b-127">Each digit can be added to the hierarchy as children of Hand, as shown in the following diagram.</span></span>

![人工階層的圖表](images/stack2.png)

<span data-ttu-id="3e67b-129">如果您在移至下一個路徑之前，先將 arm 的完整圖形以深度優先順序往返至最低的路徑，請執行一連串的分段轉譯。</span><span class="sxs-lookup"><span data-stu-id="3e67b-129">If you traverse the complete graph of the arm in depth-first order - traversing as far down one path as possible before moving on to the next path - to draw the scene, you perform a sequence of segmented rendering.</span></span> <span data-ttu-id="3e67b-130">例如，若要呈現手邊和手指，請執行下列模式。</span><span class="sxs-lookup"><span data-stu-id="3e67b-130">For example, to render the hand and fingers, you implement the following pattern.</span></span>

1.  <span data-ttu-id="3e67b-131">將手矩陣推送至矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="3e67b-131">Push the Hand matrix onto the matrix stack.</span></span>
2.  <span data-ttu-id="3e67b-132">畫手。</span><span class="sxs-lookup"><span data-stu-id="3e67b-132">Draw the hand.</span></span>
3.  <span data-ttu-id="3e67b-133">將 Thumb 矩陣推送至矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="3e67b-133">Push the Thumb matrix onto the matrix stack.</span></span>
4.  <span data-ttu-id="3e67b-134">繪製 thumb。</span><span class="sxs-lookup"><span data-stu-id="3e67b-134">Draw the thumb.</span></span>
5.  <span data-ttu-id="3e67b-135">將 Thumb 矩陣從堆疊中取出。</span><span class="sxs-lookup"><span data-stu-id="3e67b-135">Pop the Thumb matrix off the stack.</span></span>
6.  <span data-ttu-id="3e67b-136">將手指1矩陣推送至矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="3e67b-136">Push the Finger 1 matrix onto the matrix stack.</span></span>
7.  <span data-ttu-id="3e67b-137">繪製第一個手指。</span><span class="sxs-lookup"><span data-stu-id="3e67b-137">Draw the first finger.</span></span>
8.  <span data-ttu-id="3e67b-138">將指標1矩陣從堆疊中取出。</span><span class="sxs-lookup"><span data-stu-id="3e67b-138">Pop the Finger 1 matrix off the stack.</span></span>
9.  <span data-ttu-id="3e67b-139">將手指2矩陣推送至矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="3e67b-139">Push the Finger 2 matrix onto the matrix stack.</span></span> <span data-ttu-id="3e67b-140">您可以用這種方式繼續進行，直到轉譯所有手指和 thumb 為止。</span><span class="sxs-lookup"><span data-stu-id="3e67b-140">You continue in this manner until all the fingers and thumb are rendered.</span></span>

<span data-ttu-id="3e67b-141">在您完成手指的呈現之後，您會將該牌從堆疊中取出。</span><span class="sxs-lookup"><span data-stu-id="3e67b-141">After you have completed rendering the fingers, you would pop the Hand matrix off the stack.</span></span>

<span data-ttu-id="3e67b-142">您可以使用下列範例，在程式碼中執行這個基本程式。</span><span class="sxs-lookup"><span data-stu-id="3e67b-142">You can follow this basic process in code with the following examples.</span></span> <span data-ttu-id="3e67b-143">當您在樹狀結構資料結構的深度優先搜尋期間遇到節點時，請將矩陣推送至矩陣堆疊的頂端。</span><span class="sxs-lookup"><span data-stu-id="3e67b-143">When you encounter a node during the depth-first search of the tree data structure, push the matrix onto the top of the matrix stack.</span></span>


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



<span data-ttu-id="3e67b-144">當您完成節點時，請將矩陣從矩陣堆疊的頂端取出。</span><span class="sxs-lookup"><span data-stu-id="3e67b-144">When you are finished with a node, pop the matrix off the top of the matrix stack.</span></span>


```
MatrixStack->Pop();
```



<span data-ttu-id="3e67b-145">如此一來，堆疊頂端的矩陣一律代表目前節點的世界轉換。</span><span class="sxs-lookup"><span data-stu-id="3e67b-145">In this way, the matrix on the top of the stack always represents the world-transform of the current node.</span></span> <span data-ttu-id="3e67b-146">因此，在繪製每個節點之前，您應該先設定 Direct3D 矩陣。</span><span class="sxs-lookup"><span data-stu-id="3e67b-146">Therefore, before drawing each node, you should set the Direct3D matrix.</span></span>


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



<span data-ttu-id="3e67b-147">如需有關您可以在 D3DX 矩陣堆疊上執行之特定方法的詳細資訊，請參閱 [**ID3DXMATRIXStack**](id3dxmatrixstack.md) 參考主題。</span><span class="sxs-lookup"><span data-stu-id="3e67b-147">For more information about the specific methods that you can perform on a D3DX matrix stack, see the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) reference topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e67b-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e67b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e67b-149">頂點管線</span><span class="sxs-lookup"><span data-stu-id="3e67b-149">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 



