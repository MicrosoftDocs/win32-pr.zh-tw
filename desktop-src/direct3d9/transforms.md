---
description: 在 Direct3D 中，轉換引擎負責將幾何推入固定函式幾何管線。
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: '轉換 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385835"
---
# <a name="transforms-direct3d-9"></a><span data-ttu-id="2980f-103">轉換 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="2980f-103">Transforms (Direct3D 9)</span></span>

<span data-ttu-id="2980f-104">在 Direct3D 中，轉換引擎負責將幾何推入固定函式幾何管線。</span><span class="sxs-lookup"><span data-stu-id="2980f-104">The part of Direct3D that pushes geometry through the fixed function geometry pipeline is the transform engine.</span></span> <span data-ttu-id="2980f-105">它在世界中尋找模型和檢視器，將頂點投影在螢幕上顯示，並將頂點裁剪至檢視區。</span><span class="sxs-lookup"><span data-stu-id="2980f-105">It locates the model and viewer in the world, projects vertices for display on the screen, and clips vertices to the viewport.</span></span> <span data-ttu-id="2980f-106">轉換引擎也會執行光線計算，以判斷每個頂點上的擴散和反射元件。</span><span class="sxs-lookup"><span data-stu-id="2980f-106">The transform engine also performs lighting computations to determine diffuse and specular components at each vertex.</span></span>

<span data-ttu-id="2980f-107">幾何管線使用頂點做為輸入。</span><span class="sxs-lookup"><span data-stu-id="2980f-107">The geometry pipeline takes vertices as input.</span></span> <span data-ttu-id="2980f-108">轉換引擎將世界、檢視和影轉換套用至頂點，剪輯結果，然後將所有項目傳遞至轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2980f-108">The transform engine applies the world, view, and projection transforms to the vertices, clips the result, and passes everything to the rasterizer.</span></span>

<span data-ttu-id="2980f-109">在管線的開頭，模型頂點的宣告是相對於區域座標系統。</span><span class="sxs-lookup"><span data-stu-id="2980f-109">At the head of the pipeline, a model's vertices are declared relative to a local coordinate system.</span></span> <span data-ttu-id="2980f-110">這是區域原點和方向。</span><span class="sxs-lookup"><span data-stu-id="2980f-110">This is a local origin and an orientation.</span></span> <span data-ttu-id="2980f-111">這種座標方向通常稱為模型空間，而個別座標稱為模型座標。</span><span class="sxs-lookup"><span data-stu-id="2980f-111">This orientation of coordinates is often referred to as model space, and individual coordinates are called model coordinates.</span></span>

<span data-ttu-id="2980f-112">幾何管線的第一階段會將模型的頂點從其區域座標系統轉換成場景中所有物件所使用的座標系統。</span><span class="sxs-lookup"><span data-stu-id="2980f-112">The first stage of the geometry pipeline transforms a model's vertices from their local coordinate system to a coordinate system that is used by all the objects in a scene.</span></span> <span data-ttu-id="2980f-113">Reorienting 頂點的程式稱為「世界」轉換。</span><span class="sxs-lookup"><span data-stu-id="2980f-113">The process of reorienting the vertices is called the world transform.</span></span> <span data-ttu-id="2980f-114">這個新的方向通常稱為「世界空間」，而世界空間中的每個頂點都會使用全局座標來宣告。</span><span class="sxs-lookup"><span data-stu-id="2980f-114">This new orientation is commonly referred to as world space, and each vertex in world space is declared using world coordinates.</span></span>

<span data-ttu-id="2980f-115">在下一個階段，描述您 3D 世界的頂點是相對於相機定向的。</span><span class="sxs-lookup"><span data-stu-id="2980f-115">In the next stage, the vertices that describe your 3D world are oriented with respect to a camera.</span></span> <span data-ttu-id="2980f-116">也就是說，您的應用程式會選擇場景的觀點，而世界空間座標會重新置放並圍繞相機的觀賞旋轉，將世界空間變成相機空間。</span><span class="sxs-lookup"><span data-stu-id="2980f-116">That is, your application chooses a point-of-view for the scene, and world space coordinates are relocated and rotated around the camera's view, turning world space into camera space.</span></span> <span data-ttu-id="2980f-117">這是 view 轉換。</span><span class="sxs-lookup"><span data-stu-id="2980f-117">This is the view transform.</span></span>

<span data-ttu-id="2980f-118">下一個階段是投射轉換。</span><span class="sxs-lookup"><span data-stu-id="2980f-118">The next stage is the projection transform.</span></span> <span data-ttu-id="2980f-119">在管線的這個部分中，物件通常會隨著與檢視器之間的距離而調整，以便將深度的幻影提供給場景;關閉的物件會顯示為大於遠處的物件等等。</span><span class="sxs-lookup"><span data-stu-id="2980f-119">In this part of the pipeline, objects are usually scaled with relation to their distance from the viewer in order to give the illusion of depth to a scene; close objects are made to appear larger than distant objects, and so on.</span></span> <span data-ttu-id="2980f-120">為了簡化，本文件將是投影轉換後頂點的存在空間稱為投影空間。</span><span class="sxs-lookup"><span data-stu-id="2980f-120">For simplicity, this documentation refers to the space in which vertices exist after the projection transform as projection space.</span></span> <span data-ttu-id="2980f-121">一些圖形書籍可能將投影空間稱為透視後同質空間。</span><span class="sxs-lookup"><span data-stu-id="2980f-121">Some graphics books might refer to projection space as post-perspective homogeneous space.</span></span> <span data-ttu-id="2980f-122">並非所有投影轉換都會將場景中的物件大小縮放。</span><span class="sxs-lookup"><span data-stu-id="2980f-122">Not all projection transforms scale the size of objects in a scene.</span></span> <span data-ttu-id="2980f-123">這類投影有時稱為仿射或正交投影。</span><span class="sxs-lookup"><span data-stu-id="2980f-123">A projection such as this is sometimes called an affine or orthogonal projection.</span></span>

<span data-ttu-id="2980f-124">在管線的最後一部分，將不會顯示在螢幕上的任何頂點移除，以便轉譯器不會花時間計算永遠不會看到之項目的色彩和陰影。</span><span class="sxs-lookup"><span data-stu-id="2980f-124">In the final part of the pipeline, any vertices that will not be visible on the screen are removed, so that the rasterizer doesn't take the time to calculate the colors and shading for something that will never be seen.</span></span> <span data-ttu-id="2980f-125">此程序稱為裁剪。</span><span class="sxs-lookup"><span data-stu-id="2980f-125">This process is called clipping.</span></span> <span data-ttu-id="2980f-126">裁剪之後，剩餘頂點依據檢視區參數縮放，而且轉換成螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="2980f-126">After clipping, the remaining vertices are scaled according to the viewport parameters and converted into screen coordinates.</span></span> <span data-ttu-id="2980f-127">結果頂點 (當場景點陣化時會顯示在螢幕上) 存在於螢幕空間。</span><span class="sxs-lookup"><span data-stu-id="2980f-127">The resulting vertices, seen on the screen when the scene is rasterized, exist in screen space.</span></span>

<span data-ttu-id="2980f-128">轉換用於將物件幾何從某個座標轉換到另一個座標。</span><span class="sxs-lookup"><span data-stu-id="2980f-128">Transforms are used to convert object geometry from one coordinate space to another.</span></span> <span data-ttu-id="2980f-129">Direct3D 使用矩陣執行 3D 轉換。</span><span class="sxs-lookup"><span data-stu-id="2980f-129">Direct3D uses matrices to perform 3D transforms.</span></span> <span data-ttu-id="2980f-130">本節說明矩陣如何建立3D 轉換、描述一些常用的轉換，並詳細說明如何結合矩陣以產生包含多個轉換的單一矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-130">This section explains how matrices create 3D transforms, describes some common uses for transforms, and details how you can combine matrices to produce a single matrix that encompasses multiple transforms.</span></span>

-   <span data-ttu-id="2980f-131">[ (Direct3D 9 的世界轉換) ](world-transform.md) -從模型空間轉換成世界空間</span><span class="sxs-lookup"><span data-stu-id="2980f-131">[World Transform (Direct3D 9)](world-transform.md) - convert from model space to world space</span></span>
-   <span data-ttu-id="2980f-132">[查看 (Direct3D 9 的轉換) ](view-transform.md) -從世界空間轉換成視野空間</span><span class="sxs-lookup"><span data-stu-id="2980f-132">[View Transform (Direct3D 9)](view-transform.md) - convert from world space to view space</span></span>
-   <span data-ttu-id="2980f-133">[ (Direct3D 9 的投射轉換) ](projection-transform.md) -從 view space 轉換成投射空間</span><span class="sxs-lookup"><span data-stu-id="2980f-133">[Projection Transform (Direct3D 9)](projection-transform.md) - convert from view space to projection space</span></span>

## <a name="matrix-transforms"></a><span data-ttu-id="2980f-134">矩陣轉換</span><span class="sxs-lookup"><span data-stu-id="2980f-134">Matrix Transforms</span></span>

<span data-ttu-id="2980f-135">在與 3D 圖形搭配運作的應用程式，您可以使用幾何轉換，執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="2980f-135">In applications that work with 3D graphics, you can use geometrical transforms to do the following:</span></span>

-   <span data-ttu-id="2980f-136">表示某物件相對於另一個物件的位置。</span><span class="sxs-lookup"><span data-stu-id="2980f-136">Express the location of an object relative to another object.</span></span>
-   <span data-ttu-id="2980f-137">旋轉和調整物件大小。</span><span class="sxs-lookup"><span data-stu-id="2980f-137">Rotate and size objects.</span></span>
-   <span data-ttu-id="2980f-138">變更檢視位置、方向及透視圖。</span><span class="sxs-lookup"><span data-stu-id="2980f-138">Change viewing positions, directions, and perspectives.</span></span>

<span data-ttu-id="2980f-139">使用 4x4 矩陣，您可以將任何點 (x,y,z) 轉換成另一個點 (x', y', z')，如下面方程式中顯示。</span><span class="sxs-lookup"><span data-stu-id="2980f-139">You can transform any point (x,y,z) into another point (x', y', z') by using a 4x4 matrix, as shown in the following equation.</span></span>

![將任何點轉換成另一個點的方程式](images/matmult.png)

<span data-ttu-id="2980f-141">在 (x, y, z) 和矩陣執行下列方程式以產生點 (x', y', z')。</span><span class="sxs-lookup"><span data-stu-id="2980f-141">Perform the following equations on (x, y, z) and the matrix to produce the point (x', y', z').</span></span>

![新點的方程式](images/matexpnd.png)

<span data-ttu-id="2980f-143">最常見的轉換是轉移、旋轉和縮放比例。</span><span class="sxs-lookup"><span data-stu-id="2980f-143">The most common transforms are translation, rotation, and scaling.</span></span> <span data-ttu-id="2980f-144">您可以將產生這些效果的矩陣結合成單一矩陣，一次計算幾個轉換。</span><span class="sxs-lookup"><span data-stu-id="2980f-144">You can combine the matrices that produce these effects into a single matrix to calculate several transforms at once.</span></span> <span data-ttu-id="2980f-145">例如，您可以建立單一矩陣以轉移並旋轉一系列的點。</span><span class="sxs-lookup"><span data-stu-id="2980f-145">For example, you can build a single matrix to translate and rotate a series of points.</span></span>

<span data-ttu-id="2980f-146">矩陣依列-欄順序寫入。</span><span class="sxs-lookup"><span data-stu-id="2980f-146">Matrices are written in row-column order.</span></span> <span data-ttu-id="2980f-147">沿著每個軸稱平均縮放頂點 (稱為統一縮放) 的矩陣，由下列使用數學符號的矩陣表示。</span><span class="sxs-lookup"><span data-stu-id="2980f-147">A matrix that evenly scales vertices along each axis, known as uniform scaling, is represented by the following matrix using mathematical notation.</span></span>

![統一縮放矩陣的方程式](images/matrix.png)

<span data-ttu-id="2980f-149">在 c + + 中，Direct3D 會使用 [**D3DMATRIX**](d3dmatrix.md) 結構，將矩陣宣告為二維陣列。</span><span class="sxs-lookup"><span data-stu-id="2980f-149">In C++, Direct3D declares matrices as a two-dimensional array, using the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="2980f-150">下列範例示範如何初始化 **D3DMATRIX** 結構，以作為統一的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-150">The following example shows how to initialize a **D3DMATRIX** structure to act as a uniform scaling matrix.</span></span>


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a><span data-ttu-id="2980f-151">翻譯</span><span class="sxs-lookup"><span data-stu-id="2980f-151">Translate</span></span>

<span data-ttu-id="2980f-152">下面方程式將點 (x, y, z) 轉移到新點 (x', y', z')。</span><span class="sxs-lookup"><span data-stu-id="2980f-152">The following equation translates the point (x, y, z) to a new point (x', y', z').</span></span>

![新點轉移矩陣的方程式](images/transl8.png)

<span data-ttu-id="2980f-154">您可以在 C++ 中手動建立轉移矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-154">You can manually create a translation matrix in C++.</span></span> <span data-ttu-id="2980f-155">下列範例程式碼示範如何建立矩陣以轉移頂點的功能。</span><span class="sxs-lookup"><span data-stu-id="2980f-155">The following example shows the source code for a function that creates a matrix to translate vertices.</span></span>


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



<span data-ttu-id="2980f-156">為了方便起見，D3DX 公用程式程式庫會提供 [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) 功能。</span><span class="sxs-lookup"><span data-stu-id="2980f-156">For convenience, the D3DX utility library supplies the [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) function.</span></span>

## <a name="scale"></a><span data-ttu-id="2980f-157">調整</span><span class="sxs-lookup"><span data-stu-id="2980f-157">Scale</span></span>

<span data-ttu-id="2980f-158">下面方程式以 x、y 與 z 方向的任意值，將點 (x, y, z) 縮放成新點 (x', y', z')。</span><span class="sxs-lookup"><span data-stu-id="2980f-158">The following equation scales the point (x, y, z) by arbitrary values in the x-, y-, and z-directions to a new point (x', y', z').</span></span>

![新點縮放矩陣的方程式](images/matscale.png)

## <a name="rotate"></a><span data-ttu-id="2980f-160">Rotate</span><span class="sxs-lookup"><span data-stu-id="2980f-160">Rotate</span></span>

<span data-ttu-id="2980f-161">這裡描述的轉換適用於左手座標系統，因此可能不同於您在其他地方看到的轉移矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-161">The transforms described here are for left-handed coordinate systems, and so may be different from transform matrices that you have seen elsewhere.</span></span>

<span data-ttu-id="2980f-162">下面方程式圍繞 x 軸旋轉點 (x, y, z)，產生新點 (x', y', z')。</span><span class="sxs-lookup"><span data-stu-id="2980f-162">The following equation rotates the point (x, y, z) around the x-axis, producing a new point (x', y', z').</span></span>

![新點 x 旋轉矩陣的方程式](images/matxrot.png)

<span data-ttu-id="2980f-164">下面方程式圍繞 y 軸旋轉點。</span><span class="sxs-lookup"><span data-stu-id="2980f-164">The following equation rotates the point around the y-axis.</span></span>

![新點 y 旋轉矩陣的方程式](images/matyrot.png)

<span data-ttu-id="2980f-166">下面方程式圍繞 z 軸旋轉點。</span><span class="sxs-lookup"><span data-stu-id="2980f-166">The following equation rotates the point around the z-axis.</span></span>

![新點 z 旋轉矩陣的方程式](images/matzrot.png)

<span data-ttu-id="2980f-168">在這些範例矩陣，希臘字母 theta 表示旋轉角度 (以弧度為單位)。</span><span class="sxs-lookup"><span data-stu-id="2980f-168">In these example matrices, the Greek letter theta stands for the angle of rotation, in radians.</span></span> <span data-ttu-id="2980f-169">沿著旋轉軸向原點方向看時，角度是順時針方向測量。</span><span class="sxs-lookup"><span data-stu-id="2980f-169">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

<span data-ttu-id="2980f-170">在 c + + 應用程式中，使用 D3DX 公用程式程式庫所提供的 [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)、 [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)和 [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) 函數來建立旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-170">In a C++ application, use the [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md), and [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) functions supplied by the D3DX utility library to create rotation matrices.</span></span> <span data-ttu-id="2980f-171">以下是 **D3DXMatrixRotationX** 函式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="2980f-171">The following is the code for the **D3DXMatrixRotationX** function.</span></span>


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a><span data-ttu-id="2980f-172">串連矩陣</span><span class="sxs-lookup"><span data-stu-id="2980f-172">Concatenating Matrices</span></span>

<span data-ttu-id="2980f-173">使用矩陣的一個優點是，您可以透過將矩陣相乘，組合兩個或更多矩陣的效果。</span><span class="sxs-lookup"><span data-stu-id="2980f-173">One advantage of using matrices is that you can combine the effects of two or more matrices by multiplying them.</span></span> <span data-ttu-id="2980f-174">這表示，若要旋轉模型，然後將它轉移到特定位置，您不需要套用兩個矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-174">This means that, to rotate a model and then translate it to some location, you don't need to apply two matrices.</span></span> <span data-ttu-id="2980f-175">而是，您將旋轉矩陣和轉移矩陣相乘，產生一個包含所有效果的複合矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-175">Instead, you multiply the rotation and translation matrices to produce a composite matrix that contains all their effects.</span></span> <span data-ttu-id="2980f-176">這個程序，稱為矩陣串連，可以使用下面方程式撰寫。</span><span class="sxs-lookup"><span data-stu-id="2980f-176">This process, called matrix concatenation, can be written with the following equation.</span></span>

![矩陣串連的方程式](images/matrxcat.png)

<span data-ttu-id="2980f-178">在這個方程式中，C 是所建立的複合矩陣，而 M₁ 到 Mₙ 是個別矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-178">In this equation, C is the composite matrix being created, and M₁ through Mₙ are the individual matrices.</span></span> <span data-ttu-id="2980f-179">在大部分案例中，只會串連兩個或三個矩陣，但沒有限制。</span><span class="sxs-lookup"><span data-stu-id="2980f-179">In most cases, only two or three matrices are concatenated, but there is no limit.</span></span>

<span data-ttu-id="2980f-180">您可以使用 [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) 函數來執行矩陣乘法。</span><span class="sxs-lookup"><span data-stu-id="2980f-180">Use the [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) function to perform matrix multiplication.</span></span>

<span data-ttu-id="2980f-181">執行矩陣乘法的順序非常重要。</span><span class="sxs-lookup"><span data-stu-id="2980f-181">The order in which the matrix multiplication is performed is crucial.</span></span> <span data-ttu-id="2980f-182">上述公式反映矩陣串連的由左至右規則。</span><span class="sxs-lookup"><span data-stu-id="2980f-182">The preceding formula reflects the left-to-right rule of matrix concatenation.</span></span> <span data-ttu-id="2980f-183">也就是，您用來建立複合矩陣之矩陣的可見效果是依由左至右的順序發生。</span><span class="sxs-lookup"><span data-stu-id="2980f-183">That is, the visible effects of the matrices that you use to create a composite matrix occur in left-to-right order.</span></span> <span data-ttu-id="2980f-184">以下範例顯示一般世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-184">A typical world matrix is shown in the following example.</span></span> <span data-ttu-id="2980f-185">想像您要為定型飛行器建立世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="2980f-185">Imagine that you are creating the world matrix for a stereotypical flying saucer.</span></span> <span data-ttu-id="2980f-186">您可能會想要圍繞飛行器的中心 (模型空間的 y 軸) 來旋轉飛行器，並將它轉移到場景中的其他位置。</span><span class="sxs-lookup"><span data-stu-id="2980f-186">You would probably want to spin the flying saucer around its center - the y-axis of model space - and translate it to some other location in your scene.</span></span> <span data-ttu-id="2980f-187">若要完成此效果，您首先建立旋轉矩陣，再將它乘以轉移矩陣，如下面方程式中顯示。</span><span class="sxs-lookup"><span data-stu-id="2980f-187">To accomplish this effect, you first create a rotation matrix, and then multiply it by a translation matrix, as shown in the following equation.</span></span>

![根據旋轉矩陣和轉移矩陣之旋轉的方程式](images/wrldexpl.png)

<span data-ttu-id="2980f-189">在這個公式中，R<sub>y</sub> 是圍繞 y 軸之旋轉的矩陣，而 T<sub>w</sub> 則是轉移到世界座標中的特定位置。</span><span class="sxs-lookup"><span data-stu-id="2980f-189">In this formula, R<sub>y</sub> is a matrix for rotation about the y-axis, and T<sub>w</sub> is a translation to some position in world coordinates.</span></span>

<span data-ttu-id="2980f-190">矩陣相乘的順序很重要，因為不像兩個純量數值相乘，矩陣乘法不具交換性。</span><span class="sxs-lookup"><span data-stu-id="2980f-190">The order in which you multiply the matrices is important because, unlike multiplying two scalar values, matrix multiplication is not commutative.</span></span> <span data-ttu-id="2980f-191">依相反順序將矩陣相乘，有轉移飛行器到世界空間位置，然後圍繞世界原點旋轉的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="2980f-191">Multiplying the matrices in the opposite order has the visual effect of translating the flying saucer to its world space position, and then rotating it around the world origin.</span></span>

<span data-ttu-id="2980f-192">無論您建立何種矩陣類型，請記住由左至右規則，以確定您達到預期的效果。</span><span class="sxs-lookup"><span data-stu-id="2980f-192">No matter what type of matrix you are creating, remember the left-to-right rule to ensure that you achieve the expected effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2980f-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="2980f-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2980f-194">快速入門</span><span class="sxs-lookup"><span data-stu-id="2980f-194">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



