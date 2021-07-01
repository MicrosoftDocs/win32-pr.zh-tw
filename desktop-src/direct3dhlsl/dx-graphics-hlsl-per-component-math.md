---
title: Per-Component 數學運算
description: 透過 HLSL，您可以在演算法層級編寫著色器。
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c8c9eeea1072c53915588ac0099998e76c0452a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119593"
---
# <a name="per-component-math-operations"></a><span data-ttu-id="dabf9-103">Per-Component 數學運算</span><span class="sxs-lookup"><span data-stu-id="dabf9-103">Per-Component Math Operations</span></span>

<span data-ttu-id="dabf9-104">透過 HLSL，您可以在演算法層級編寫著色器。</span><span class="sxs-lookup"><span data-stu-id="dabf9-104">With HLSL, you can program shaders at an algorithm level.</span></span> <span data-ttu-id="dabf9-105">若要瞭解語言，您必須知道如何宣告變數和函式、使用內建函式、定義自訂資料類型，以及使用語義將著色器引數連接至其他著色器和管線。</span><span class="sxs-lookup"><span data-stu-id="dabf9-105">To understand the language, you will need to know how to declare variables and functions, use intrinsic functions, define custom data types and use semantics to connect shader arguments to other shaders and to the pipeline.</span></span>

<span data-ttu-id="dabf9-106">一旦您瞭解如何在 HLSL 中撰寫著色器，您將需要瞭解 API 呼叫，以便您可以：編譯特定硬體的著色器、初始化著色器常數，以及視需要初始化其他管線狀態。</span><span class="sxs-lookup"><span data-stu-id="dabf9-106">Once you learn how to author shaders in HLSL, you will need to learn about API calls so that you can: compile a shader for particular hardware, initialize shader constants, and initialize other pipeline state if necessary.</span></span>

-   [<span data-ttu-id="dabf9-107">向量類型</span><span class="sxs-lookup"><span data-stu-id="dabf9-107">The Vector Type</span></span>](#the-vector-type)
-   [<span data-ttu-id="dabf9-108">矩陣類型</span><span class="sxs-lookup"><span data-stu-id="dabf9-108">The Matrix Type</span></span>](#the-matrix-type)
    -   [<span data-ttu-id="dabf9-109">矩陣順序</span><span class="sxs-lookup"><span data-stu-id="dabf9-109">Matrix Ordering</span></span>](#matrix-ordering)
-   [<span data-ttu-id="dabf9-110">範例</span><span class="sxs-lookup"><span data-stu-id="dabf9-110">Examples</span></span>](#examples)
-   [<span data-ttu-id="dabf9-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="dabf9-111">Related topics</span></span>](#related-topics)

## <a name="the-vector-type"></a><span data-ttu-id="dabf9-112">向量類型</span><span class="sxs-lookup"><span data-stu-id="dabf9-112">The Vector Type</span></span>

<span data-ttu-id="dabf9-113">Vector 是包含一到四個元件的資料結構。</span><span class="sxs-lookup"><span data-stu-id="dabf9-113">A vector is a data structure that contains between one and four components.</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



<span data-ttu-id="dabf9-114">緊接在資料類型後面的整數是向量上的元件數目。</span><span class="sxs-lookup"><span data-stu-id="dabf9-114">The integer immediately following the data type is the number of components on the vector.</span></span>

<span data-ttu-id="dabf9-115">初始化運算式也可以包含在宣告中。</span><span class="sxs-lookup"><span data-stu-id="dabf9-115">Initializers can also be included in the declarations.</span></span>


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="dabf9-116">或者，向量類型可以用來建立相同的宣告：</span><span class="sxs-lookup"><span data-stu-id="dabf9-116">Alternatively, the vector type can be used to make the same declarations:</span></span>


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="dabf9-117">向量類型會使用角括弧來指定元件的類型和數目。</span><span class="sxs-lookup"><span data-stu-id="dabf9-117">The vector type uses angle brackets to specify the type and number of components.</span></span>

<span data-ttu-id="dabf9-118">向量最多包含四個元件，每個元件都可以使用兩個命名集的其中一個來存取：</span><span class="sxs-lookup"><span data-stu-id="dabf9-118">Vectors contain up to four components, each of which can be accessed using one of two naming sets:</span></span>

-   <span data-ttu-id="dabf9-119">設定的位置： x、y、z、w</span><span class="sxs-lookup"><span data-stu-id="dabf9-119">The position set: x,y,z,w</span></span>
-   <span data-ttu-id="dabf9-120">色彩設定： r、g、b、a</span><span class="sxs-lookup"><span data-stu-id="dabf9-120">The color set: r,g,b,a</span></span>

<span data-ttu-id="dabf9-121">這些語句都會傳回第三個元件的值。</span><span class="sxs-lookup"><span data-stu-id="dabf9-121">These statements both return the value in the third component.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



<span data-ttu-id="dabf9-122">命名集可以使用一或多個元件，但不能混用。</span><span class="sxs-lookup"><span data-stu-id="dabf9-122">Naming sets can use one or more components, but they cannot be mixed.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



<span data-ttu-id="dabf9-123">在讀取元件時指定一或多個向量元件，稱為 swizzling。</span><span class="sxs-lookup"><span data-stu-id="dabf9-123">Specifying one or more vector components when reading components is called swizzling.</span></span> <span data-ttu-id="dabf9-124">例如：</span><span class="sxs-lookup"><span data-stu-id="dabf9-124">For example:</span></span>


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



<span data-ttu-id="dabf9-125">遮罩會控制寫入的元件數目。</span><span class="sxs-lookup"><span data-stu-id="dabf9-125">Masking controls how many components are written.</span></span>


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



<span data-ttu-id="dabf9-126">無法將指派寫入相同的元件一次以上。</span><span class="sxs-lookup"><span data-stu-id="dabf9-126">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="dabf9-127">因此，此語句的左邊無效：</span><span class="sxs-lookup"><span data-stu-id="dabf9-127">So the left side of this statement is invalid:</span></span>


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



<span data-ttu-id="dabf9-128">此外，元件命名空間也不能混用。</span><span class="sxs-lookup"><span data-stu-id="dabf9-128">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="dabf9-129">這是不正確元件寫入：</span><span class="sxs-lookup"><span data-stu-id="dabf9-129">This is an invalid component write:</span></span>


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



<span data-ttu-id="dabf9-130">將向量當作純量存取會存取向量的第一個元件。</span><span class="sxs-lookup"><span data-stu-id="dabf9-130">Accessing a vector as a scalar will access the first component of the vector.</span></span> <span data-ttu-id="dabf9-131">下列兩個語句是相等的。</span><span class="sxs-lookup"><span data-stu-id="dabf9-131">The following two statements are equivalent.</span></span>


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a><span data-ttu-id="dabf9-132">矩陣類型</span><span class="sxs-lookup"><span data-stu-id="dabf9-132">The Matrix Type</span></span>

<span data-ttu-id="dabf9-133">矩陣是包含資料列和資料行的資料結構。</span><span class="sxs-lookup"><span data-stu-id="dabf9-133">A matrix is a data structure that contains rows and columns of data.</span></span> <span data-ttu-id="dabf9-134">資料可以是任何純量資料類型，不過，矩陣的每個元素都是相同的資料類型。</span><span class="sxs-lookup"><span data-stu-id="dabf9-134">The data can be any of the scalar data types, however, every element of a matrix is the same data type.</span></span> <span data-ttu-id="dabf9-135">資料列和資料行的數目是使用附加至資料類型的逐資料行字串來指定。</span><span class="sxs-lookup"><span data-stu-id="dabf9-135">The number of rows and columns is specified with the row-by-column string that is appended to the data type.</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



<span data-ttu-id="dabf9-136">資料列或資料行的最大數目為 4;最小值為1。</span><span class="sxs-lookup"><span data-stu-id="dabf9-136">The maximum number of rows or columns is 4; the minimum number is 1.</span></span>

<span data-ttu-id="dabf9-137">在宣告矩陣時，可以將它初始化：</span><span class="sxs-lookup"><span data-stu-id="dabf9-137">A matrix can be initialized when it is declared:</span></span>


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="dabf9-138">或者，矩陣類型可以用來建立相同的宣告：</span><span class="sxs-lookup"><span data-stu-id="dabf9-138">Or, the matrix type can be used to make the same declarations:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



<span data-ttu-id="dabf9-139">矩陣類型會使用角括弧來指定類型、資料列數目和資料行數目。</span><span class="sxs-lookup"><span data-stu-id="dabf9-139">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="dabf9-140">這個範例會建立具有兩個數據列和兩個數據行的浮點數矩陣。</span><span class="sxs-lookup"><span data-stu-id="dabf9-140">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="dabf9-141">您可以使用任何純量資料類型。</span><span class="sxs-lookup"><span data-stu-id="dabf9-141">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="dabf9-142">這個宣告會定義浮點數的矩陣 (32 位浮點數) 有兩個數據列和三個數據行：</span><span class="sxs-lookup"><span data-stu-id="dabf9-142">This declaration defines a matrix of float values (32-bit floating-point numbers) with two rows and three columns:</span></span>


```
matrix <float, 2, 3> fFloatMatrix;
```



<span data-ttu-id="dabf9-143">矩陣包含以資料列和資料行組織的值，可使用結構運算子 "." 來存取，後面接著兩個命名集的其中一個：</span><span class="sxs-lookup"><span data-stu-id="dabf9-143">A matrix contains values organized in rows and columns, which can be accessed using the structure operator "." followed by one of two naming sets:</span></span>

-   <span data-ttu-id="dabf9-144">以零為基礎的資料列資料行位置：</span><span class="sxs-lookup"><span data-stu-id="dabf9-144">The zero-based row-column position:</span></span>
    -   <span data-ttu-id="dabf9-145">\_m00、 \_ m01、 \_ m02、 \_ m03</span><span class="sxs-lookup"><span data-stu-id="dabf9-145">\_m00, \_m01, \_m02, \_m03</span></span>
    -   <span data-ttu-id="dabf9-146">\_m10、 \_ m11、 \_ m12、 \_ m13</span><span class="sxs-lookup"><span data-stu-id="dabf9-146">\_m10, \_m11, \_m12, \_m13</span></span>
    -   <span data-ttu-id="dabf9-147">\_m20、 \_ m21、 \_ m22、 \_ m23</span><span class="sxs-lookup"><span data-stu-id="dabf9-147">\_m20, \_m21, \_m22, \_m23</span></span>
    -   <span data-ttu-id="dabf9-148">\_m30、 \_ m31、 \_ m32、 \_ m33</span><span class="sxs-lookup"><span data-stu-id="dabf9-148">\_m30, \_m31, \_m32, \_m33</span></span>
-   <span data-ttu-id="dabf9-149">以一為基礎的資料列資料行位置：</span><span class="sxs-lookup"><span data-stu-id="dabf9-149">The one-based row-column position:</span></span>
    -   <span data-ttu-id="dabf9-150">\_11、 \_ 12、 \_ 13、 \_ 14</span><span class="sxs-lookup"><span data-stu-id="dabf9-150">\_11, \_12, \_13, \_14</span></span>
    -   <span data-ttu-id="dabf9-151">\_21、 \_ 22、 \_ 23、 \_ 24</span><span class="sxs-lookup"><span data-stu-id="dabf9-151">\_21, \_22, \_23, \_24</span></span>
    -   <span data-ttu-id="dabf9-152">\_31、 \_ 32、 \_ 33、 \_ 34</span><span class="sxs-lookup"><span data-stu-id="dabf9-152">\_31, \_32, \_33, \_34</span></span>
    -   <span data-ttu-id="dabf9-153">\_41、 \_ 42、 \_ 43、 \_ 44</span><span class="sxs-lookup"><span data-stu-id="dabf9-153">\_41, \_42, \_43, \_44</span></span>

<span data-ttu-id="dabf9-154">每個命名集的開頭都是底線，後面接著資料列編號和資料行編號。</span><span class="sxs-lookup"><span data-stu-id="dabf9-154">Each naming set starts with an underscore followed by the row number and the column number.</span></span> <span data-ttu-id="dabf9-155">以零為基底的慣例也會在資料列和資料行編號之前包含字母 "m"。</span><span class="sxs-lookup"><span data-stu-id="dabf9-155">The zero-based convention also includes the letter "m" before the row and column number.</span></span> <span data-ttu-id="dabf9-156">以下是使用兩個命名集來存取矩陣的範例：</span><span class="sxs-lookup"><span data-stu-id="dabf9-156">Here's an example that uses the two naming sets to access a matrix:</span></span>


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



<span data-ttu-id="dabf9-157">就像向量一樣，命名集可以使用命名集的一或多個元件。</span><span class="sxs-lookup"><span data-stu-id="dabf9-157">Just like vectors, naming sets can use one or more components from either naming set.</span></span>


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



<span data-ttu-id="dabf9-158">您也可以使用陣列存取標記法來存取矩陣，這是以零為基礎的索引集合。</span><span class="sxs-lookup"><span data-stu-id="dabf9-158">A matrix can also be accessed using array access notation, which is a zero-based set of indices.</span></span> <span data-ttu-id="dabf9-159">每個索引都在方括弧內。</span><span class="sxs-lookup"><span data-stu-id="dabf9-159">Each index is inside of square brackets.</span></span> <span data-ttu-id="dabf9-160">使用下列索引來存取4x4 矩陣：</span><span class="sxs-lookup"><span data-stu-id="dabf9-160">A 4x4 matrix is accessed with the following indices:</span></span>

-   <span data-ttu-id="dabf9-161">\[0 \] \[ 0 \] 、 \[ 0 \] \[ 1 \] 、 \[ 0 \] \[ 2 \] 、 \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="dabf9-161">\[0\]\[0\], \[0\]\[1\], \[0\]\[2\], \[0\]\[3\]</span></span>
-   <span data-ttu-id="dabf9-162">\[1 \] \[ 0 \] ， \[ 1 \] \[ 1 \] ， \[ 1 \] \[ 2 \] ， \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="dabf9-162">\[1\]\[0\], \[1\]\[1\], \[1\]\[2\], \[1\]\[3\]</span></span>
-   <span data-ttu-id="dabf9-163">\[2 \] \[ 0 \] 、 \[ 2 \] \[ 1 \] 、 \[ 2 \] \[ 2 \] 、 \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="dabf9-163">\[2\]\[0\], \[2\]\[1\], \[2\]\[2\], \[2\]\[3\]</span></span>
-   <span data-ttu-id="dabf9-164">\[3 \] \[ 0 \] 、 \[ 3 \] \[ 1 \] 、 \[ 3 \] \[ 2 \] 、 \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="dabf9-164">\[3\]\[0\], \[3\]\[1\], \[3\]\[2\], \[3\]\[3\]</span></span>

<span data-ttu-id="dabf9-165">以下是存取矩陣的範例：</span><span class="sxs-lookup"><span data-stu-id="dabf9-165">Here is an example of accessing a matrix:</span></span>


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



<span data-ttu-id="dabf9-166">請注意，不會使用結構運算子 "." 來存取陣列。</span><span class="sxs-lookup"><span data-stu-id="dabf9-166">Notice that the structure operator "." is not used to access an array.</span></span> <span data-ttu-id="dabf9-167">陣列存取標記法不能使用 swizzling 來讀取一個以上的元件。</span><span class="sxs-lookup"><span data-stu-id="dabf9-167">Array access notation cannot use swizzling to read more than one component.</span></span>


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



<span data-ttu-id="dabf9-168">不過，陣列存取可以讀取多元件向量。</span><span class="sxs-lookup"><span data-stu-id="dabf9-168">However, array accessing can read a multi-component vector.</span></span>


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



<span data-ttu-id="dabf9-169">如同向量，讀取一個以上的矩陣元件稱為 swizzling。</span><span class="sxs-lookup"><span data-stu-id="dabf9-169">As with vectors, reading more than one matrix component is called swizzling.</span></span> <span data-ttu-id="dabf9-170">只要使用一個命名空間，就可以指派一個以上的元件。</span><span class="sxs-lookup"><span data-stu-id="dabf9-170">More than one component can be assigned, assuming only one name space is used.</span></span> <span data-ttu-id="dabf9-171">這些都是有效的指派：</span><span class="sxs-lookup"><span data-stu-id="dabf9-171">These are all valid assignments:</span></span>


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



<span data-ttu-id="dabf9-172">遮罩會控制寫入的元件數目。</span><span class="sxs-lookup"><span data-stu-id="dabf9-172">Masking controls how many components are written.</span></span>


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="dabf9-173">無法將指派寫入相同的元件一次以上。</span><span class="sxs-lookup"><span data-stu-id="dabf9-173">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="dabf9-174">因此，此語句的左邊無效：</span><span class="sxs-lookup"><span data-stu-id="dabf9-174">So the left side of this statement is invalid:</span></span>


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="dabf9-175">此外，元件命名空間也不能混用。</span><span class="sxs-lookup"><span data-stu-id="dabf9-175">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="dabf9-176">這是不正確元件寫入：</span><span class="sxs-lookup"><span data-stu-id="dabf9-176">This is an invalid component write:</span></span>


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a><span data-ttu-id="dabf9-177">矩陣順序</span><span class="sxs-lookup"><span data-stu-id="dabf9-177">Matrix Ordering</span></span>

<span data-ttu-id="dabf9-178">統一參數的矩陣封裝順序預設會設定為 [資料行主要]。</span><span class="sxs-lookup"><span data-stu-id="dabf9-178">Matrix packing order for uniform parameters is set to column-major by default.</span></span> <span data-ttu-id="dabf9-179">這表示矩陣的每個資料行都會儲存在單一常數暫存器中。</span><span class="sxs-lookup"><span data-stu-id="dabf9-179">This means each column of the matrix is stored in a single constant register.</span></span> <span data-ttu-id="dabf9-180">另一方面，資料列主要矩陣會將矩陣的每個資料列封裝在單一常數暫存器中。</span><span class="sxs-lookup"><span data-stu-id="dabf9-180">On the other hand, a row-major matrix packs each row of the matrix in a single constant register.</span></span> <span data-ttu-id="dabf9-181">您可以使用 **\# pragmapack \_ 矩陣** 指示詞，或使用資料列 **\_ 主要** 關鍵字或資料行 **\_ 主要** 關鍵字來變更矩陣封裝。</span><span class="sxs-lookup"><span data-stu-id="dabf9-181">Matrix packing can be changed with the **\#pragmapack\_matrix** directive, or with the **row\_major** or the **column\_major** keyword.</span></span>

<span data-ttu-id="dabf9-182">在著色器執行之前，矩陣中的資料會載入著色器常數暫存器中。</span><span class="sxs-lookup"><span data-stu-id="dabf9-182">The data in a matrix is loaded into shader constant registers before a shader runs.</span></span> <span data-ttu-id="dabf9-183">如何讀取矩陣資料的選項有兩種：以資料列為主的順序或依資料行的順序。</span><span class="sxs-lookup"><span data-stu-id="dabf9-183">There are two choices for how the matrix data is read: in row-major order or in column-major order.</span></span> <span data-ttu-id="dabf9-184">資料行主要順序表示每個矩陣資料行都會儲存在單一常數暫存器中，而資料列主要順序表示矩陣的每個資料列都會儲存在單一常數暫存器中。</span><span class="sxs-lookup"><span data-stu-id="dabf9-184">Column-major order means that each matrix column will be stored in a single constant register, and row-major order means that each row of the matrix will be stored in a single constant register.</span></span> <span data-ttu-id="dabf9-185">這是用於矩陣的常數暫存器數目的重要考慮。</span><span class="sxs-lookup"><span data-stu-id="dabf9-185">This is an important consideration for how many constant registers are used for a matrix.</span></span>

<span data-ttu-id="dabf9-186">資料列主要矩陣的配置方式如下所示：</span><span class="sxs-lookup"><span data-stu-id="dabf9-186">A row-major matrix is laid out like the following:</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="dabf9-187">11</span><span class="sxs-lookup"><span data-stu-id="dabf9-187">11</span></span><br/>
        <span data-ttu-id="dabf9-188">21</span><span class="sxs-lookup"><span data-stu-id="dabf9-188">21</span></span><br/>
        <span data-ttu-id="dabf9-189">31</span><span class="sxs-lookup"><span data-stu-id="dabf9-189">31</span></span><br/>
        <span data-ttu-id="dabf9-190">41</span><span class="sxs-lookup"><span data-stu-id="dabf9-190">41</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="dabf9-191">12</span><span class="sxs-lookup"><span data-stu-id="dabf9-191">12</span></span><br/>
        <span data-ttu-id="dabf9-192">22</span><span class="sxs-lookup"><span data-stu-id="dabf9-192">22</span></span><br/>
        <span data-ttu-id="dabf9-193">32</span><span class="sxs-lookup"><span data-stu-id="dabf9-193">32</span></span><br/>
        <span data-ttu-id="dabf9-194">42</span><span class="sxs-lookup"><span data-stu-id="dabf9-194">42</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="dabf9-195">13</span><span class="sxs-lookup"><span data-stu-id="dabf9-195">13</span></span><br/>
        <span data-ttu-id="dabf9-196">23</span><span class="sxs-lookup"><span data-stu-id="dabf9-196">23</span></span><br/>
        <span data-ttu-id="dabf9-197">33</span><span class="sxs-lookup"><span data-stu-id="dabf9-197">33</span></span><br/>
        <span data-ttu-id="dabf9-198">43</span><span class="sxs-lookup"><span data-stu-id="dabf9-198">43</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="dabf9-199">14</span><span class="sxs-lookup"><span data-stu-id="dabf9-199">14</span></span><br/>
        <span data-ttu-id="dabf9-200">24</span><span class="sxs-lookup"><span data-stu-id="dabf9-200">24</span></span><br/>
        <span data-ttu-id="dabf9-201">34</span><span class="sxs-lookup"><span data-stu-id="dabf9-201">34</span></span><br/>
        <span data-ttu-id="dabf9-202">44</span><span class="sxs-lookup"><span data-stu-id="dabf9-202">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="dabf9-203">資料行主要矩陣的配置方式如下所示：</span><span class="sxs-lookup"><span data-stu-id="dabf9-203">A column-major matrix is laid out like the following:</span></span>


:::row:::
    :::column:::
        <span data-ttu-id="dabf9-204">11</span><span class="sxs-lookup"><span data-stu-id="dabf9-204">11</span></span><br/>
        <span data-ttu-id="dabf9-205">12</span><span class="sxs-lookup"><span data-stu-id="dabf9-205">12</span></span><br/>
        <span data-ttu-id="dabf9-206">13</span><span class="sxs-lookup"><span data-stu-id="dabf9-206">13</span></span><br/>
        <span data-ttu-id="dabf9-207">14</span><span class="sxs-lookup"><span data-stu-id="dabf9-207">14</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="dabf9-208">21</span><span class="sxs-lookup"><span data-stu-id="dabf9-208">21</span></span><br/>
        <span data-ttu-id="dabf9-209">22</span><span class="sxs-lookup"><span data-stu-id="dabf9-209">22</span></span><br/>
        <span data-ttu-id="dabf9-210">23</span><span class="sxs-lookup"><span data-stu-id="dabf9-210">23</span></span><br/>
        <span data-ttu-id="dabf9-211">24</span><span class="sxs-lookup"><span data-stu-id="dabf9-211">24</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="dabf9-212">31</span><span class="sxs-lookup"><span data-stu-id="dabf9-212">31</span></span><br/>
        <span data-ttu-id="dabf9-213">32</span><span class="sxs-lookup"><span data-stu-id="dabf9-213">32</span></span><br/>
        <span data-ttu-id="dabf9-214">33</span><span class="sxs-lookup"><span data-stu-id="dabf9-214">33</span></span><br/>
        <span data-ttu-id="dabf9-215">34</span><span class="sxs-lookup"><span data-stu-id="dabf9-215">34</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="dabf9-216">14</span><span class="sxs-lookup"><span data-stu-id="dabf9-216">14</span></span><br/>
        <span data-ttu-id="dabf9-217">24</span><span class="sxs-lookup"><span data-stu-id="dabf9-217">24</span></span><br/>
        <span data-ttu-id="dabf9-218">34</span><span class="sxs-lookup"><span data-stu-id="dabf9-218">34</span></span><br/>
        <span data-ttu-id="dabf9-219">44</span><span class="sxs-lookup"><span data-stu-id="dabf9-219">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="dabf9-220">資料列-主要和資料行主要矩陣順序：決定從著色器輸入讀取矩陣元件的順序。</span><span class="sxs-lookup"><span data-stu-id="dabf9-220">Row-major and column-major matrix ordering determine the order the matrix components are read from shader inputs.</span></span> <span data-ttu-id="dabf9-221">一旦資料寫入常數暫存器中，矩陣順序就不會影響資料在著色器程式碼中的使用或存取方式。</span><span class="sxs-lookup"><span data-stu-id="dabf9-221">Once the data is written into constant registers, matrix order has no effect on how the data is used or accessed from within shader code.</span></span> <span data-ttu-id="dabf9-222">此外，在著色器主體中宣告的矩陣不會封裝成常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="dabf9-222">Also, matrices declared in a shader body do not get packed into constant registers.</span></span> <span data-ttu-id="dabf9-223">資料列-主要和資料行主要封裝順序不會影響函式的封裝順序 (其一律遵循資料列主要順序) 。</span><span class="sxs-lookup"><span data-stu-id="dabf9-223">Row-major and column-major packing order has no influence on the packing order of constructors (which always follows row-major ordering).</span></span>

<span data-ttu-id="dabf9-224">矩陣中的資料順序可以在編譯時期宣告，或編譯器會在執行時間為數據排序，以獲得最有效率的使用方式。</span><span class="sxs-lookup"><span data-stu-id="dabf9-224">The order of the data in a matrix can be declared at compile time or the compiler will order the data at runtime for the most efficient use.</span></span>

## <a name="examples"></a><span data-ttu-id="dabf9-225">範例</span><span class="sxs-lookup"><span data-stu-id="dabf9-225">Examples</span></span>

<span data-ttu-id="dabf9-226">HLSL 會使用兩種特殊類型：向量類型和矩陣類型，讓程式設計2D 和3D 圖形變得更容易。</span><span class="sxs-lookup"><span data-stu-id="dabf9-226">HLSL uses two special types, a vector type and a matrix type to make programming 2D and 3D graphics easier.</span></span> <span data-ttu-id="dabf9-227">其中每個類型都包含一個以上的元件;向量最多包含四個元件，而矩陣最多包含16個元件。</span><span class="sxs-lookup"><span data-stu-id="dabf9-227">Each of these types contain more than one component; a vector contains up to four components, and a matrix contains up to 16 components.</span></span> <span data-ttu-id="dabf9-228">當向量和矩陣在標準 HLSL 方程式中使用時，所執行的數學會設計為每個元件的工作。</span><span class="sxs-lookup"><span data-stu-id="dabf9-228">When vectors and matrices are used in standard HLSL equations, the math performed is designed to work per-component.</span></span> <span data-ttu-id="dabf9-229">比方說，HLSL 會執行這個乘法：</span><span class="sxs-lookup"><span data-stu-id="dabf9-229">For instance, HLSL implements this multiply:</span></span>


```
float4 v = a*b;
```



<span data-ttu-id="dabf9-230">四個元件的乘法。</span><span class="sxs-lookup"><span data-stu-id="dabf9-230">as a four-component multiply.</span></span> <span data-ttu-id="dabf9-231">結果為四個純量：</span><span class="sxs-lookup"><span data-stu-id="dabf9-231">The result is four scalars:</span></span>


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



<span data-ttu-id="dabf9-232">這是四個乘法運算，其中每個結果都會儲存在 v 的個別元件中。</span><span class="sxs-lookup"><span data-stu-id="dabf9-232">This is four multiplications where each result is stored in a separate component of v.</span></span> <span data-ttu-id="dabf9-233">這稱為四個元件的乘法。</span><span class="sxs-lookup"><span data-stu-id="dabf9-233">This is called a four-component multiply.</span></span> <span data-ttu-id="dabf9-234">HLSL 會使用元件數學，讓寫入著色器非常有效率。</span><span class="sxs-lookup"><span data-stu-id="dabf9-234">HLSL uses component math which makes writing shaders very efficient.</span></span>

<span data-ttu-id="dabf9-235">這與通常實作為點乘積的乘法（會產生單一純量）非常不同：</span><span class="sxs-lookup"><span data-stu-id="dabf9-235">This is very different from a multiply which is typically implemented as a dot product which generates a single scalar:</span></span>


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



<span data-ttu-id="dabf9-236">矩陣也會使用 HLSL 中的每個元件作業：</span><span class="sxs-lookup"><span data-stu-id="dabf9-236">A matrix also uses per-component operations in HLSL:</span></span>


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



<span data-ttu-id="dabf9-237">結果會是兩個矩陣 (的每個元件乘，而不是標準3x3 矩陣乘以) 。</span><span class="sxs-lookup"><span data-stu-id="dabf9-237">The result is a per-component multiply of the two matrices (as opposed to a standard 3x3 matrix multiply).</span></span> <span data-ttu-id="dabf9-238">每個元件矩陣乘法會產生第一個詞彙：</span><span class="sxs-lookup"><span data-stu-id="dabf9-238">A per component matrix multiply yields this first term:</span></span>


```
mat3.m00 = mat1.m00 * mat2._m00;
```



<span data-ttu-id="dabf9-239">這與會產生第一個詞彙的3x3 矩陣相乘不同：</span><span class="sxs-lookup"><span data-stu-id="dabf9-239">This is different from a 3x3 matrix multiply which would yield this first term:</span></span>


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



<span data-ttu-id="dabf9-240">相乘內建函式的多載版本，其中一個運算元是向量，另一個運算元是矩陣。</span><span class="sxs-lookup"><span data-stu-id="dabf9-240">Overloaded versions of the multiply intrinsic function handle cases where one operand is a vector and the other operand is a matrix.</span></span> <span data-ttu-id="dabf9-241">例如：向量 \* 向量、向量 \* 矩陣、矩陣 \* 向量和矩陣 \* 矩陣。</span><span class="sxs-lookup"><span data-stu-id="dabf9-241">Such as: vector \* vector, vector \* matrix, matrix \* vector, and matrix \* matrix.</span></span> <span data-ttu-id="dabf9-242">例如：</span><span class="sxs-lookup"><span data-stu-id="dabf9-242">For instance:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="dabf9-243">產生相同的結果，如下所示：</span><span class="sxs-lookup"><span data-stu-id="dabf9-243">produces the same result as:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="dabf9-244">此範例會使用 (float1x4) 轉換，將 pos 向量轉換成資料行向量。</span><span class="sxs-lookup"><span data-stu-id="dabf9-244">This example casts the pos vector to a column vector using the (float1x4) cast.</span></span> <span data-ttu-id="dabf9-245">藉由轉型來變更向量，或將提供給乘法的引數的順序交換，相當於將矩陣轉置。</span><span class="sxs-lookup"><span data-stu-id="dabf9-245">Changing a vector by casting, or swapping the order of the arguments supplied to multiply is equivalent to transposing the matrix.</span></span>

<span data-ttu-id="dabf9-246">自動轉換轉換會導致乘法和 dot 內建函式傳回與此處所用相同的結果：</span><span class="sxs-lookup"><span data-stu-id="dabf9-246">Automatic cast conversion causes the multiply and dot intrinsic functions to return the same results as used here:</span></span>


```
{
  float4 val;
  return mul(val,val);
}
```



<span data-ttu-id="dabf9-247">相乘的結果是 \* 4x1 = 1x1 向量。</span><span class="sxs-lookup"><span data-stu-id="dabf9-247">This result of the multiply is a 1x4 \* 4x1 = 1x1 vector.</span></span> <span data-ttu-id="dabf9-248">這相當於點乘積：</span><span class="sxs-lookup"><span data-stu-id="dabf9-248">This is equivalent to a dot product:</span></span>


```
{
  float4 val;
  return dot(val,val);
}
```



<span data-ttu-id="dabf9-249">傳回單一純量值的。</span><span class="sxs-lookup"><span data-stu-id="dabf9-249">which returns a single scalar value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dabf9-250">相關主題</span><span class="sxs-lookup"><span data-stu-id="dabf9-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dabf9-251"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="dabf9-251">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




