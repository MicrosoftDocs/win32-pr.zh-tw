---
title: 使用進展來表示填補和記憶體版面配置
description: DirectML 張量是由稱為 *大小* 的屬性和 *tensor 的進展* 所描述。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b944b1a2600febe27f209bffcc0e355c6a9fc7db
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548392"
---
# <a name="using-strides-to-express-padding-and-memory-layout"></a><span data-ttu-id="8ae6b-103">使用進展來表示填補和記憶體版面配置</span><span class="sxs-lookup"><span data-stu-id="8ae6b-103">Using strides to express padding and memory layout</span></span>

<span data-ttu-id="8ae6b-104">DirectML 張量是由 &mdash; Direct3D 12 緩衝區所支援，其 &mdash; 由稱為 *大小* 和 tensor *進展的* 屬性來描述。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-104">DirectML tensors&mdash;which are are backed by Direct3D 12 buffers&mdash;are described by properties known as the *sizes* and the *strides* of the tensor.</span></span> <span data-ttu-id="8ae6b-105">Tensor 的 *大小* 會描述 tensor 的邏輯維度。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-105">The tensor's *sizes* describe the logical dimensions of the tensor.</span></span> <span data-ttu-id="8ae6b-106">例如，2D tensor 的高度可能是2，而寬度為3。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-106">For example, a 2D tensor might have a height of 2 and a width of 3.</span></span> <span data-ttu-id="8ae6b-107">邏輯上來說，tensor 具有6個相異的元素，但大小並不會指定這些元素如何儲存在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-107">Logically, the tensor has 6 distinct elements, although the sizes don't specify how those elements are stored in memory.</span></span> <span data-ttu-id="8ae6b-108">Tensor 的進展 *會描述 tensor* 元素的實體記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-108">The tensor's *strides* describe the physical memory layout of the tensor's elements.</span></span>

## <a name="two-dimensional-2d-arrays"></a><span data-ttu-id="8ae6b-109">二維 (2D) 陣列</span><span class="sxs-lookup"><span data-stu-id="8ae6b-109">Two-dimensional (2D) arrays</span></span>

<span data-ttu-id="8ae6b-110">請考慮高度為2且寬度為3的 2D tensor;資料是由文字字元所組成。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-110">Consider a 2D tensor that has a height of 2 and a width of 3; the data comprises textual characters.</span></span> <span data-ttu-id="8ae6b-111">在 C/c + + 中，這可能會使用多維度陣列來表示。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-111">In C/C++, this might be expressed using a multi-dimensional array.</span></span>

```cpp
constexpr int rows = 2;
constexpr int columns = 3;
char tensor[rows][columns];
tensor[0][0] = 'A';
tensor[0][1] = 'B';
tensor[0][2] = 'C';
tensor[1][0] = 'D';
tensor[1][1] = 'E';
tensor[1][2] = 'F';
```

<span data-ttu-id="8ae6b-112">上述 tensor 的邏輯視圖如下所示。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-112">The logical view of the above tensor is visualized below.</span></span>

```console
A B C
D E F
```

<span data-ttu-id="8ae6b-113">在 C/c + + 中，多維度陣列是以資料列主要順序儲存。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-113">In C/C++, a multi-dimensional array is stored in row-major order.</span></span> <span data-ttu-id="8ae6b-114">換句話說，沿著寬度維度的連續元素會連續儲存線上性記憶體空間中。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-114">In other words, the consecutive elements along the width dimension are stored contiguously in linear memory space.</span></span>

<span data-ttu-id="8ae6b-115">位移：</span><span class="sxs-lookup"><span data-stu-id="8ae6b-115">Offset:</span></span>|<span data-ttu-id="8ae6b-116">0</span><span class="sxs-lookup"><span data-stu-id="8ae6b-116">0</span></span>|<span data-ttu-id="8ae6b-117">1</span><span class="sxs-lookup"><span data-stu-id="8ae6b-117">1</span></span>|<span data-ttu-id="8ae6b-118">2</span><span class="sxs-lookup"><span data-stu-id="8ae6b-118">2</span></span>|<span data-ttu-id="8ae6b-119">3</span><span class="sxs-lookup"><span data-stu-id="8ae6b-119">3</span></span>|<span data-ttu-id="8ae6b-120">4</span><span class="sxs-lookup"><span data-stu-id="8ae6b-120">4</span></span>|<span data-ttu-id="8ae6b-121">5</span><span class="sxs-lookup"><span data-stu-id="8ae6b-121">5</span></span>
-|-|-|-|-|-|-
<span data-ttu-id="8ae6b-122">值：</span><span class="sxs-lookup"><span data-stu-id="8ae6b-122">Value:</span></span>|<span data-ttu-id="8ae6b-123">A</span><span class="sxs-lookup"><span data-stu-id="8ae6b-123">A</span></span>|<span data-ttu-id="8ae6b-124">B</span><span class="sxs-lookup"><span data-stu-id="8ae6b-124">B</span></span>|<span data-ttu-id="8ae6b-125">C</span><span class="sxs-lookup"><span data-stu-id="8ae6b-125">C</span></span>|<span data-ttu-id="8ae6b-126">D</span><span class="sxs-lookup"><span data-stu-id="8ae6b-126">D</span></span>|<span data-ttu-id="8ae6b-127">E</span><span class="sxs-lookup"><span data-stu-id="8ae6b-127">E</span></span>|<span data-ttu-id="8ae6b-128">F</span><span class="sxs-lookup"><span data-stu-id="8ae6b-128">F</span></span>

<span data-ttu-id="8ae6b-129">維度的 *跨距* 是要跳過的專案數，以便存取該維度中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-129">The *stride* of a dimension is the number of elements to skip in order to access the next element in that dimension.</span></span> <span data-ttu-id="8ae6b-130">努力表達記憶體中 tensor 的版面配置。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-130">Strides express the layout of the tensor in memory.</span></span> <span data-ttu-id="8ae6b-131">以資料列為主的順序而言，寬度維度的跨距一律為1，因為沿著維度的相鄰元素會連續儲存。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-131">With a row-major order, the stride of the width dimension is always 1, since adjacent elements along the dimension are stored contiguously.</span></span> <span data-ttu-id="8ae6b-132">高度維度的 stride 取決於寬度維度的大小;在上述範例中，沿著高度維度的連續元素之間的距離 (例如，A 到 D) 等於 tensor (的寬度，在此範例) 中為3。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-132">The stride of the height dimension depends on the size of the width dimension; in the above example, the distance between consecutive elements along the height dimension (for example, A to D) is equal to the width of the tensor (which is 3 in this example).</span></span>

<span data-ttu-id="8ae6b-133">若要說明不同的版面配置，請考慮使用資料行主要順序。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-133">To illustrate a different layout, consider column-major order.</span></span> <span data-ttu-id="8ae6b-134">換句話說，沿著高度維度的連續元素會連續儲存線上性記憶體空間中。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-134">In other words, the consecutive elements along the height dimension are stored contiguously in linear memory space.</span></span> <span data-ttu-id="8ae6b-135">在此情況下，高度跨距一律為1，而寬度跨距為 2 (高度維度) 的大小。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-135">In this case, the height-stride is always 1, and the width-stride is 2 (the size of the height dimension).</span></span>

<span data-ttu-id="8ae6b-136">位移：</span><span class="sxs-lookup"><span data-stu-id="8ae6b-136">Offset:</span></span>|<span data-ttu-id="8ae6b-137">0</span><span class="sxs-lookup"><span data-stu-id="8ae6b-137">0</span></span>|<span data-ttu-id="8ae6b-138">1</span><span class="sxs-lookup"><span data-stu-id="8ae6b-138">1</span></span>|<span data-ttu-id="8ae6b-139">2</span><span class="sxs-lookup"><span data-stu-id="8ae6b-139">2</span></span>|<span data-ttu-id="8ae6b-140">3</span><span class="sxs-lookup"><span data-stu-id="8ae6b-140">3</span></span>|<span data-ttu-id="8ae6b-141">4</span><span class="sxs-lookup"><span data-stu-id="8ae6b-141">4</span></span>|<span data-ttu-id="8ae6b-142">5</span><span class="sxs-lookup"><span data-stu-id="8ae6b-142">5</span></span>
-|-|-|-|-|-|-
<span data-ttu-id="8ae6b-143">值：</span><span class="sxs-lookup"><span data-stu-id="8ae6b-143">Value:</span></span>|<span data-ttu-id="8ae6b-144">A</span><span class="sxs-lookup"><span data-stu-id="8ae6b-144">A</span></span>|<span data-ttu-id="8ae6b-145">D</span><span class="sxs-lookup"><span data-stu-id="8ae6b-145">D</span></span>|<span data-ttu-id="8ae6b-146">B</span><span class="sxs-lookup"><span data-stu-id="8ae6b-146">B</span></span>|<span data-ttu-id="8ae6b-147">E</span><span class="sxs-lookup"><span data-stu-id="8ae6b-147">E</span></span>|<span data-ttu-id="8ae6b-148">C</span><span class="sxs-lookup"><span data-stu-id="8ae6b-148">C</span></span>|<span data-ttu-id="8ae6b-149">F</span><span class="sxs-lookup"><span data-stu-id="8ae6b-149">F</span></span>

## <a name="higher-dimensions"></a><span data-ttu-id="8ae6b-150">較高的維度</span><span class="sxs-lookup"><span data-stu-id="8ae6b-150">Higher dimensions</span></span>

<span data-ttu-id="8ae6b-151">當超過兩個維度時，將配置參考為數據列或資料行的版面配置就變得很困難。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-151">When it comes to greater than two dimensions, it's unwieldy to refer to a layout as either row-major or column-major.</span></span> <span data-ttu-id="8ae6b-152">因此，本主題的其餘部分會使用這些詞彙和標籤。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-152">So, the rest of this topic uses terms and labels such as these.</span></span>

- <span data-ttu-id="8ae6b-153">2D：「HW」 &mdash; 高度是 (資料列主要) 的最高序位維度。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-153">2D: "HW"&mdash;height is the highest-order dimension (row-major).</span></span>
- <span data-ttu-id="8ae6b-154">2D：「WH」 &mdash; 寬度是 (資料行主要) 的最高序位維度。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-154">2D: "WH"&mdash;width is the highest-order dimension (column-major).</span></span>
- <span data-ttu-id="8ae6b-155">3D：「DHW」 &mdash; 深度是最高順序的維度，後面接著 height，然後是 width。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-155">3D: "DHW"&mdash;depth is the highest-order dimension, followed by height, and then width.</span></span>
- <span data-ttu-id="8ae6b-156">3D：「WHD」 &mdash; 寬度是最高順序的維度，後面接著高度，然後是深度。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-156">3D: "WHD"&mdash;width is the highest-order dimension, followed by height, and then depth.</span></span>
- <span data-ttu-id="8ae6b-157">4D： "NCHW" &mdash; (批次大小) 的影像數目，然後是通道的數目，再接著高度，然後是寬度。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-157">4D: "NCHW"&mdash;the number of images (batch size), then the number of channels, then height, then width.</span></span>

<span data-ttu-id="8ae6b-158">一般而言，維度的 *封裝* 跨距等於低序位維度之大小的乘積。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-158">In general, the *packed* stride of a dimension is equal to the product of the sizes of the lower-order dimensions.</span></span> <span data-ttu-id="8ae6b-159">例如，使用 "DHW" 配置，D stride 等於 H \* W;H stride 等於 W;而 W stride 等於1。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-159">For example, with a "DHW" layout, the D-stride is equal to H \* W; the H-stride is equal to W; and the W-stride is equal to 1.</span></span> <span data-ttu-id="8ae6b-160">當 tensor 的總實體大小等於 tensor 的總邏輯大小時，就會將進展視為已 *封裝* ;換句話說，沒有額外的空格或重迭的元素。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-160">Strides are said to be *packed* when the total physical size of the tensor is equal to the total logical size of the tensor; in other words, there's no extra space nor overlapping elements.</span></span>

<span data-ttu-id="8ae6b-161">讓我們將2D 範例延伸至三個維度，讓我們有深度2、高度2和寬度 3 (的 tensor，共12個邏輯元素) 。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-161">Let's extend the 2D example to three dimensions, so that we have a tensor with depth 2, height 2, and width 3 (for a total of 12 logical elements).</span></span>

```console
A B C
D E F

G H I
J K L
```

<span data-ttu-id="8ae6b-162">使用 "DHW" 配置時，此 tensor 會以下列格式儲存。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-162">With a "DHW" layout, this tensor is stored as follows.</span></span>

<span data-ttu-id="8ae6b-163">位移：</span><span class="sxs-lookup"><span data-stu-id="8ae6b-163">Offset:</span></span>|<span data-ttu-id="8ae6b-164">0</span><span class="sxs-lookup"><span data-stu-id="8ae6b-164">0</span></span>|<span data-ttu-id="8ae6b-165">1</span><span class="sxs-lookup"><span data-stu-id="8ae6b-165">1</span></span>|<span data-ttu-id="8ae6b-166">2</span><span class="sxs-lookup"><span data-stu-id="8ae6b-166">2</span></span>|<span data-ttu-id="8ae6b-167">3</span><span class="sxs-lookup"><span data-stu-id="8ae6b-167">3</span></span>|<span data-ttu-id="8ae6b-168">4</span><span class="sxs-lookup"><span data-stu-id="8ae6b-168">4</span></span>|<span data-ttu-id="8ae6b-169">5</span><span class="sxs-lookup"><span data-stu-id="8ae6b-169">5</span></span>|<span data-ttu-id="8ae6b-170">6</span><span class="sxs-lookup"><span data-stu-id="8ae6b-170">6</span></span>|<span data-ttu-id="8ae6b-171">7</span><span class="sxs-lookup"><span data-stu-id="8ae6b-171">7</span></span>|<span data-ttu-id="8ae6b-172">8</span><span class="sxs-lookup"><span data-stu-id="8ae6b-172">8</span></span>|<span data-ttu-id="8ae6b-173">9</span><span class="sxs-lookup"><span data-stu-id="8ae6b-173">9</span></span>|<span data-ttu-id="8ae6b-174">10</span><span class="sxs-lookup"><span data-stu-id="8ae6b-174">10</span></span>|<span data-ttu-id="8ae6b-175">11</span><span class="sxs-lookup"><span data-stu-id="8ae6b-175">11</span></span>|
-|-|-|-|-|-|-|-|-|-|-|-|-|
<span data-ttu-id="8ae6b-176">值：</span><span class="sxs-lookup"><span data-stu-id="8ae6b-176">Value:</span></span>|<span data-ttu-id="8ae6b-177">A</span><span class="sxs-lookup"><span data-stu-id="8ae6b-177">A</span></span>|<span data-ttu-id="8ae6b-178">B</span><span class="sxs-lookup"><span data-stu-id="8ae6b-178">B</span></span>|<span data-ttu-id="8ae6b-179">C</span><span class="sxs-lookup"><span data-stu-id="8ae6b-179">C</span></span>|<span data-ttu-id="8ae6b-180">D</span><span class="sxs-lookup"><span data-stu-id="8ae6b-180">D</span></span>|<span data-ttu-id="8ae6b-181">E</span><span class="sxs-lookup"><span data-stu-id="8ae6b-181">E</span></span>|<span data-ttu-id="8ae6b-182">F</span><span class="sxs-lookup"><span data-stu-id="8ae6b-182">F</span></span>|<span data-ttu-id="8ae6b-183">G</span><span class="sxs-lookup"><span data-stu-id="8ae6b-183">G</span></span>|<span data-ttu-id="8ae6b-184">H</span><span class="sxs-lookup"><span data-stu-id="8ae6b-184">H</span></span>|<span data-ttu-id="8ae6b-185">I</span><span class="sxs-lookup"><span data-stu-id="8ae6b-185">I</span></span>|<span data-ttu-id="8ae6b-186">J</span><span class="sxs-lookup"><span data-stu-id="8ae6b-186">J</span></span>|<span data-ttu-id="8ae6b-187">K</span><span class="sxs-lookup"><span data-stu-id="8ae6b-187">K</span></span>|<span data-ttu-id="8ae6b-188">L</span><span class="sxs-lookup"><span data-stu-id="8ae6b-188">L</span></span>|

- <span data-ttu-id="8ae6b-189">D-stride = height (2) \* width (3) = 6 (例如，' A ' 和 ' G ' ) 之間的距離。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-189">D-stride = height (2) \* width (3) = 6 (for example, the distance between 'A' and 'G').</span></span>
- <span data-ttu-id="8ae6b-190">H-stride = width (3) = 3 (例如，' A ' 和 ' d ' ) 之間的距離。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-190">H-stride = width (3) = 3 (for example, the distance between 'A' and 'D').</span></span>
- <span data-ttu-id="8ae6b-191">W-stride = 1 (例如，' A ' 和 ' B ' ) 之間的距離。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-191">W-stride = 1 (for example, the distance between 'A' and 'B').</span></span>

<span data-ttu-id="8ae6b-192">專案的索引/座標的點乘積和進展會提供緩衝區中該元素的位移。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-192">The dot product of the indices/coordinates of an element and the strides provides the offset to that element in the buffer.</span></span> <span data-ttu-id="8ae6b-193">例如，H 元素的位移 (d = 1，h = 0，w = 1) 為7。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-193">For example, the offset of the H element (d=1, h=0, w=1) is 7.</span></span>

<span data-ttu-id="8ae6b-194">{1，0，1} ⋅ {6，3，1} = 1 \* 6 + 0 \* 3 + 1 \* 1 = 7</span><span class="sxs-lookup"><span data-stu-id="8ae6b-194">{1, 0, 1} ⋅ {6, 3, 1} = 1 \* 6 + 0 \* 3 + 1 \* 1 = 7</span></span>

## <a name="packed-tensors"></a><span data-ttu-id="8ae6b-195">封裝張量</span><span class="sxs-lookup"><span data-stu-id="8ae6b-195">Packed tensors</span></span>

<span data-ttu-id="8ae6b-196">上述範例說明 *封裝* 的張量。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-196">The examples above illustrate *packed* tensors.</span></span> <span data-ttu-id="8ae6b-197">當) 元素中 tensor (的邏輯大小等於) 專案中緩衝區 (的實際大小，且每個專案都有唯一的位址/位移時，即會將 tensor 視為可 *壓縮* 。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-197">A tensor is said to be *packed* when the logical size of the tensor (in elements) is equal to the physical size of the buffer (in elements), and each element has a unique address/offset.</span></span> <span data-ttu-id="8ae6b-198">例如，如果緩衝區的長度為12個元素，則會封裝 2x2x3 tensor，而且不會對任何一組元素共用緩衝區中的相同位移。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-198">For example, a 2x2x3 tensor is packed if the buffer is 12 elements in length and no pair of elements share the same offset in the buffer.</span></span> <span data-ttu-id="8ae6b-199">封裝的張量是最常見的情況;但是，進展可以更複雜的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-199">Packed tensors are the most common case; but strides allow more complex memory layouts.</span></span>

## <a name="broadcasting-with-strides"></a><span data-ttu-id="8ae6b-200">具有進展的廣播</span><span class="sxs-lookup"><span data-stu-id="8ae6b-200">Broadcasting with strides</span></span>

<span data-ttu-id="8ae6b-201">如果 tensor 的 () 專案中的緩衝區大小小於其邏輯維度的乘積，則會遵循專案中必須有一些重迭的元素。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-201">If a tensor's buffer size (in elements) is smaller than the product of its logical dimensions, then it follows that there must be some overlapping of elements.</span></span> <span data-ttu-id="8ae6b-202">這種情況的一般情況稱為 *廣播*;維度的元素是另一個維度的複本。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-202">The usual case for this is known as *broadcasting*; where the elements of a dimension are a duplicate of another dimension.</span></span> <span data-ttu-id="8ae6b-203">例如，讓我們重新審視2D 範例。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-203">For example, let's revisit the 2D example.</span></span> <span data-ttu-id="8ae6b-204">假設我們想要以邏輯方式2x3 的 tensor，但第二個數據列與第一個資料列相同。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-204">Let's say that we want a tensor that is logically 2x3, but the second row is identical to the first row.</span></span> <span data-ttu-id="8ae6b-205">如下所示。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-205">Here's how that looks.</span></span>

```console
A B C
A B C
```

<span data-ttu-id="8ae6b-206">這可能會儲存為壓縮的 HW/資料列主要 tensor。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-206">This could be stored as a packed HW/row-major tensor.</span></span> <span data-ttu-id="8ae6b-207">但是更精簡的儲存體只會包含3個元素 (A、B 和 C) ，並使用0的高度跨距，而不是3。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-207">But a more compact storage would contain only 3 elements (A, B, and C) and use a height-stride of 0 instead of 3.</span></span> <span data-ttu-id="8ae6b-208">在此情況下，tensor 的實體大小為3個元素，但邏輯大小為6個元素。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-208">In this case, the physical size of the tensor is 3 elements, but the logical size is 6 elements.</span></span>

<span data-ttu-id="8ae6b-209">一般情況下，如果維度的 stride 為0，則低序位維度中的所有元素都會沿著廣播維度重複;例如，如果 tensor 是 NCHW，而 C stride 是0，則每個通道的值會與 H 和 W 相同。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-209">In general, if the stride of a dimension is 0, then all elements in the lower-order dimensions are repeated along the broadcasted dimension; for example, if the tensor is NCHW and the C-stride is 0, then each channel has the same values along H and W.</span></span>

## <a name="padding-with-strides"></a><span data-ttu-id="8ae6b-210">具有進步的填補</span><span class="sxs-lookup"><span data-stu-id="8ae6b-210">Padding with strides</span></span>

<span data-ttu-id="8ae6b-211">如果 tensor 的實體大小大於符合其元素所需的大小下限時，就會被稱為 *填補* 。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-211">A tensor is said to be *padded* if its physical size is larger than the minimum size needed to fit its elements.</span></span> <span data-ttu-id="8ae6b-212">如果沒有廣播或重迭的元素，則 [專案]) 中 tensor (的最小大小就只是其維度的乘積。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-212">When there is no broadcasting nor overlapping elements, the minimum size of the tensor (in elements) is simply the product of its dimensions.</span></span> <span data-ttu-id="8ae6b-213">您可以使用 helper 函式 `DMLCalcBufferTensorSize` (參閱 [DirectML helper](dml-helper-functions.md) 函式，以取得該函式的清單) 計算 DirectML 張量的 *最小* 緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-213">You can use the helper function `DMLCalcBufferTensorSize` (see [DirectML helper functions](dml-helper-functions.md) for a listing of that function) to calculate the *minimum* buffer size for your DirectML tensors.</span></span>

<span data-ttu-id="8ae6b-214">假設緩衝區包含下列值 (' x ' 元素表示填補值) 。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-214">Let's say that a buffer contains the following values (the 'x' elements indicate padding values).</span></span>

<span data-ttu-id="8ae6b-215">0</span><span class="sxs-lookup"><span data-stu-id="8ae6b-215">0</span></span>|<span data-ttu-id="8ae6b-216">1</span><span class="sxs-lookup"><span data-stu-id="8ae6b-216">1</span></span>|<span data-ttu-id="8ae6b-217">2</span><span class="sxs-lookup"><span data-stu-id="8ae6b-217">2</span></span>|<span data-ttu-id="8ae6b-218">3</span><span class="sxs-lookup"><span data-stu-id="8ae6b-218">3</span></span>|<span data-ttu-id="8ae6b-219">4</span><span class="sxs-lookup"><span data-stu-id="8ae6b-219">4</span></span>|<span data-ttu-id="8ae6b-220">5</span><span class="sxs-lookup"><span data-stu-id="8ae6b-220">5</span></span>|<span data-ttu-id="8ae6b-221">6</span><span class="sxs-lookup"><span data-stu-id="8ae6b-221">6</span></span>|<span data-ttu-id="8ae6b-222">7</span><span class="sxs-lookup"><span data-stu-id="8ae6b-222">7</span></span>|<span data-ttu-id="8ae6b-223">8</span><span class="sxs-lookup"><span data-stu-id="8ae6b-223">8</span></span>|<span data-ttu-id="8ae6b-224">9</span><span class="sxs-lookup"><span data-stu-id="8ae6b-224">9</span></span>|
-|-|-|-|-|-|-|-|-|-|
<span data-ttu-id="8ae6b-225">A</span><span class="sxs-lookup"><span data-stu-id="8ae6b-225">A</span></span>|<span data-ttu-id="8ae6b-226">B</span><span class="sxs-lookup"><span data-stu-id="8ae6b-226">B</span></span>|<span data-ttu-id="8ae6b-227">C</span><span class="sxs-lookup"><span data-stu-id="8ae6b-227">C</span></span>|<span data-ttu-id="8ae6b-228">x</span><span class="sxs-lookup"><span data-stu-id="8ae6b-228">x</span></span>|<span data-ttu-id="8ae6b-229">x</span><span class="sxs-lookup"><span data-stu-id="8ae6b-229">x</span></span>|<span data-ttu-id="8ae6b-230">D</span><span class="sxs-lookup"><span data-stu-id="8ae6b-230">D</span></span>|<span data-ttu-id="8ae6b-231">E</span><span class="sxs-lookup"><span data-stu-id="8ae6b-231">E</span></span>|<span data-ttu-id="8ae6b-232">F</span><span class="sxs-lookup"><span data-stu-id="8ae6b-232">F</span></span>|<span data-ttu-id="8ae6b-233">x</span><span class="sxs-lookup"><span data-stu-id="8ae6b-233">x</span></span>|<span data-ttu-id="8ae6b-234">x</span><span class="sxs-lookup"><span data-stu-id="8ae6b-234">x</span></span>

<span data-ttu-id="8ae6b-235">填補的 tensor 可以使用5的高度 stride 而非3來描述。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-235">The padded tensor can be described by using a height-stride of 5 instead of 3.</span></span> <span data-ttu-id="8ae6b-236">此步驟不會逐步執行3個元素來取得下一個資料列，而是 (3 個 *真正* 元素加上2個填補元素) 。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-236">Instead of stepping by 3 elements to get to the next row, the step is 5 elements (3 *real* elements plus 2 padding elements).</span></span> <span data-ttu-id="8ae6b-237">填補在電腦圖形中很常見，例如，為了確保影像的電源有兩個對齊。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-237">Padding is common in computer graphics, for example, to ensure that an image has a power-of-two alignment.</span></span>

```console
A B C
D E F
```

## <a name="directml-buffer-tensor-descriptions"></a><span data-ttu-id="8ae6b-238">DirectML 緩衝區 tensor 描述</span><span class="sxs-lookup"><span data-stu-id="8ae6b-238">DirectML buffer tensor descriptions</span></span>

<span data-ttu-id="8ae6b-239">DirectML 可以使用各種實體 tensor 配置，因為 [ **DML_BUFFER_TENSOR_DESC** 結構](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)同時具有 `Sizes` 和 `Strides` 成員。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-239">DirectML can work with a variety of physical tensor layouts, since the [**DML_BUFFER_TENSOR_DESC** structure](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) has both `Sizes` and `Strides` members.</span></span> <span data-ttu-id="8ae6b-240">某些運算子實現可能會更有效率地使用特定配置，因此變更儲存 tensor 資料的方式並不常見，以提升效能。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-240">Some operator implementations might be more efficient with a specific layout, so it's not uncommon to change how tensor data is stored for better performance.</span></span>

<span data-ttu-id="8ae6b-241">大部分的 DirectML 運算子都需要4D 或5D 張量，而且大小和進展值的順序是固定的。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-241">Most DirectML operators require either 4D or 5D tensors, and the order of the sizes and strides values is fixed.</span></span> <span data-ttu-id="8ae6b-242">藉由修正 tensor 描述中的大小和 stride 值順序，DirectML 可以推斷不同的實體版面配置。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-242">By fixing the order of the sizes and stride values in a tensor description, it's possible for DirectML to infer different physical layouts.</span></span>

<span data-ttu-id="8ae6b-243">**4D**</span><span class="sxs-lookup"><span data-stu-id="8ae6b-243">**4D**</span></span>
- <span data-ttu-id="8ae6b-244">[**DML_BUFFER_TENSOR_DESC：：**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) size = {N 大小，C-大小，H-大小，W 大小}</span><span class="sxs-lookup"><span data-stu-id="8ae6b-244">[**DML_BUFFER_TENSOR_DESC::Sizes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = { N-size, C-size, H-size, W-size }</span></span>
- <span data-ttu-id="8ae6b-245">[**DML_BUFFER_TENSOR_DESC：：**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) 進展 = {N 個 Stride，C Stride，H-Stride，W-stride}</span><span class="sxs-lookup"><span data-stu-id="8ae6b-245">[**DML_BUFFER_TENSOR_DESC::Strides**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = { N-stride, C-stride, H-stride, W-stride }</span></span>

<span data-ttu-id="8ae6b-246">**5D**</span><span class="sxs-lookup"><span data-stu-id="8ae6b-246">**5D**</span></span>
- <span data-ttu-id="8ae6b-247">**DML_BUFFER_TENSOR_DESC：：** size = {N 大小，C-大小，D 大小，H-大小，W-大小}</span><span class="sxs-lookup"><span data-stu-id="8ae6b-247">**DML_BUFFER_TENSOR_DESC::Sizes** = { N-size, C-size, D-size, H-size, W-size }</span></span>
- <span data-ttu-id="8ae6b-248">**DML_BUFFER_TENSOR_DESC：：** 進展 = {N 個 Stride，C Stride，D-Stride，H-Stride，W-stride}</span><span class="sxs-lookup"><span data-stu-id="8ae6b-248">**DML_BUFFER_TENSOR_DESC::Strides** = { N-stride, C-stride, D-stride, H-stride, W-stride }</span></span>

<span data-ttu-id="8ae6b-249">如果 DirectML 運算子需要4D 或 5D tensor，但實際資料有較小的等級 (例如，2D) ，則開頭的維度應該以1s 填滿。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-249">If a DirectML operator requires a 4D or a 5D tensor, but the actual data has a smaller rank (for example, 2D), then the leading dimensions should be filled with 1s.</span></span> <span data-ttu-id="8ae6b-250">例如，"HW" tensor 是使用 **DML_BUFFER_TENSOR_DESC：：大小** = {1，1，H，W} 來設定。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-250">For example, an "HW" tensor is set using **DML_BUFFER_TENSOR_DESC::Sizes** = { 1, 1, H, W }.</span></span>

<span data-ttu-id="8ae6b-251">如果 tensor 資料儲存在 NCHW/NCDHW 中，除非您想要廣播或填補，否則不需要設定 **DML_BUFFER_TENSOR_DESC：：進步**。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-251">If tensor data is stored in NCHW/NCDHW, then it's not necessary to set **DML_BUFFER_TENSOR_DESC::Strides**, unless you want broadcasting or padding.</span></span> <span data-ttu-id="8ae6b-252">您可以將 [進展] 欄位設定為 `nullptr` 。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-252">You can set the strides field to `nullptr`.</span></span> <span data-ttu-id="8ae6b-253">但是，如果 tensor 的資料儲存在另一個配置中（例如 NHWC），則您需要進展，才能將 NCHW 的轉換表示為該版面配置。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-253">However, if the tensor data is stored in another layout, such as NHWC, then you need strides in order to express the transformation from NCHW to that layout.</span></span>

<span data-ttu-id="8ae6b-254">如需簡單的範例，請考慮高度為3和寬度為5的 2D tensor 描述。</span><span class="sxs-lookup"><span data-stu-id="8ae6b-254">For a simple example, consider the description of a 2D tensor with height 3 and width 5.</span></span>

<span data-ttu-id="8ae6b-255">**封裝 NCHW (隱含的進展)**</span><span class="sxs-lookup"><span data-stu-id="8ae6b-255">**Packed NCHW (implicit strides)**</span></span>
- <span data-ttu-id="8ae6b-256">**DML_BUFFER_TENSOR_DESC：：大小** = {1，1，3，5}</span><span class="sxs-lookup"><span data-stu-id="8ae6b-256">**DML_BUFFER_TENSOR_DESC::Sizes** = { 1, 1, 3, 5 }</span></span>
- <span data-ttu-id="8ae6b-257">**DML_BUFFER_TENSOR_DESC：：進步** = `nullptr`</span><span class="sxs-lookup"><span data-stu-id="8ae6b-257">**DML_BUFFER_TENSOR_DESC::Strides** = `nullptr`</span></span>

<span data-ttu-id="8ae6b-258">**封裝 NCHW (明確的進展)**</span><span class="sxs-lookup"><span data-stu-id="8ae6b-258">**Packed NCHW (explicit strides)**</span></span>
- <span data-ttu-id="8ae6b-259">N-stride = C-size \* H-size \* W-size = 1 \* 3 \* 5 = 15</span><span class="sxs-lookup"><span data-stu-id="8ae6b-259">N-stride = C-size \* H-size \* W-size = 1 \* 3 \* 5 = 15</span></span>
- <span data-ttu-id="8ae6b-260">C-stride = H-size \* W-size = 3 \* 5 = 15</span><span class="sxs-lookup"><span data-stu-id="8ae6b-260">C-stride = H-size \* W-size = 3 \* 5 = 15</span></span>
- <span data-ttu-id="8ae6b-261">H-stride = W-size = 5</span><span class="sxs-lookup"><span data-stu-id="8ae6b-261">H-stride = W-size = 5</span></span>
- <span data-ttu-id="8ae6b-262">W-stride = 1</span><span class="sxs-lookup"><span data-stu-id="8ae6b-262">W-stride = 1</span></span>
- <span data-ttu-id="8ae6b-263">**DML_BUFFER_TENSOR_DESC：：大小** = {1，1，3，5}</span><span class="sxs-lookup"><span data-stu-id="8ae6b-263">**DML_BUFFER_TENSOR_DESC::Sizes** = { 1, 1, 3, 5 }</span></span>
- <span data-ttu-id="8ae6b-264">**DML_BUFFER_TENSOR_DESC：：進步** = {15，15，5，1}</span><span class="sxs-lookup"><span data-stu-id="8ae6b-264">**DML_BUFFER_TENSOR_DESC::Strides** = { 15, 15, 5, 1 }</span></span>

<span data-ttu-id="8ae6b-265">**封裝 NHWC**</span><span class="sxs-lookup"><span data-stu-id="8ae6b-265">**Packed NHWC**</span></span>
- <span data-ttu-id="8ae6b-266">N 個 stride = H-size \* W-size \* C-size = 3 \* 5 \* 1 = 15</span><span class="sxs-lookup"><span data-stu-id="8ae6b-266">N-stride = H-size \* W-size \* C-size = 3 \* 5 \* 1 = 15</span></span>
- <span data-ttu-id="8ae6b-267">H-stride = W-size \* C-size = 5 \* 1 = 5</span><span class="sxs-lookup"><span data-stu-id="8ae6b-267">H-stride = W-size \* C-size = 5 \* 1 = 5</span></span>
- <span data-ttu-id="8ae6b-268">W-stride = C-大小 = 1</span><span class="sxs-lookup"><span data-stu-id="8ae6b-268">W-stride = C-size = 1</span></span>
- <span data-ttu-id="8ae6b-269">C-stride = 1</span><span class="sxs-lookup"><span data-stu-id="8ae6b-269">C-stride = 1</span></span>
- <span data-ttu-id="8ae6b-270">**DML_BUFFER_TENSOR_DESC：：大小** = {1，1，3，5}</span><span class="sxs-lookup"><span data-stu-id="8ae6b-270">**DML_BUFFER_TENSOR_DESC::Sizes** = { 1, 1, 3, 5 }</span></span>
- <span data-ttu-id="8ae6b-271">**DML_BUFFER_TENSOR_DESC：：進步** = {15，1，5，1}</span><span class="sxs-lookup"><span data-stu-id="8ae6b-271">**DML_BUFFER_TENSOR_DESC::Strides** = { 15, 1, 5, 1 }</span></span>

## <a name="see-also"></a><span data-ttu-id="8ae6b-272">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ae6b-272">See also</span></span>

* [<span data-ttu-id="8ae6b-273">DirectML helper 函式</span><span class="sxs-lookup"><span data-stu-id="8ae6b-273">DirectML helper functions</span></span>](dml-helper-functions.md)
* [<span data-ttu-id="8ae6b-274">DML_BUFFER_TENSOR_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="8ae6b-274">DML_BUFFER_TENSOR_DESC structure</span></span>](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)
