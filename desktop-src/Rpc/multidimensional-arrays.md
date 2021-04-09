---
title: 多維陣列
description: 陣列屬性也可以搭配多維度陣列使用。
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933457"
---
# <a name="multidimensional-arrays"></a><span data-ttu-id="24937-103">多維陣列</span><span class="sxs-lookup"><span data-stu-id="24937-103">Multidimensional Arrays</span></span>

<span data-ttu-id="24937-104">陣列屬性也可以搭配多維度陣列使用。</span><span class="sxs-lookup"><span data-stu-id="24937-104">Array attributes can also be used with multidimensional arrays.</span></span> <span data-ttu-id="24937-105">不過，請小心確保陣列的每個維度都有對應的屬性。</span><span class="sxs-lookup"><span data-stu-id="24937-105">However, be careful to ensure that every dimension of the array has a corresponding attribute.</span></span> <span data-ttu-id="24937-106">例如：</span><span class="sxs-lookup"><span data-stu-id="24937-106">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

<span data-ttu-id="24937-107">上述陣列是符合標準的陣列 (，其大小為30個元素陣列的大小 d1size )  (具有針對每個) 隨附的 d2len 元素。</span><span class="sxs-lookup"><span data-stu-id="24937-107">The preceding array is a conformant array (of size d1size ) of 30 element arrays (with d2len elements shipped for each).</span></span> <span data-ttu-id="24937-108">Size 的括弧中的逗號 \[ [**\_ 是**](/windows/desktop/Midl/size-is) \] attribute，指定 d1size 中的值會套用至陣列的第一個維度。</span><span class="sxs-lookup"><span data-stu-id="24937-108">The comma in the parentheses of the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute specifies that value in d1size is applied to the first dimension of the array.</span></span> <span data-ttu-id="24937-109">同樣地，length 的括弧中的命令 \[ [**\_ 是**](/windows/desktop/Midl/length-is) \] 屬性，表示 d2len 中的值會套用至陣列的第二個維度。</span><span class="sxs-lookup"><span data-stu-id="24937-109">Likewise, the command in the parentheses of the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute indicates that the value in d2len is applied to the second dimension of the array.</span></span>

<span data-ttu-id="24937-110">MIDL 2.0 編譯器提供兩種方法來封送處理參數：混合模式 (/**Os**) 和完全解讀的 (/**Oif** 或/**Oicf**) 。</span><span class="sxs-lookup"><span data-stu-id="24937-110">The MIDL 2.0 compiler provides two methods for marshaling parameters: mixed-mode (/**Os**) and fully-interpreted (/**Oif** or /**Oicf**).</span></span> <span data-ttu-id="24937-111">根據預設，MIDL 編譯器會在混合模式中編譯介面。</span><span class="sxs-lookup"><span data-stu-id="24937-111">By default, the MIDL compiler compiles interfaces in mixed mode.</span></span> <span data-ttu-id="24937-112">您不需要明確指定 [**/os**](/windows/desktop/Midl/-os) 參數來取得混合模式封送處理。</span><span class="sxs-lookup"><span data-stu-id="24937-112">You do not need to explicitly specify the [**/Os**](/windows/desktop/Midl/-os) switch to get mixed-mode marshaling.</span></span>

<span data-ttu-id="24937-113">完全解讀的方法會完全離線地封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="24937-113">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="24937-114">這會大幅減少存根程式碼的大小，但它也會導致效能降低。</span><span class="sxs-lookup"><span data-stu-id="24937-114">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span> <span data-ttu-id="24937-115">在混合模式封送處理中，存根會將某些參數離線封送處理。</span><span class="sxs-lookup"><span data-stu-id="24937-115">In mixed-mode marshaling, the stubs marshals some parameters online.</span></span> <span data-ttu-id="24937-116">雖然這會產生較大的存根大小，但它也可提供更高的效能。</span><span class="sxs-lookup"><span data-stu-id="24937-116">While this results in a larger stub size, it also offers increased performance.</span></span>

> [!Caution]  
> <span data-ttu-id="24937-117">在此模式中編譯 IDL 檔案時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="24937-117">Exercise caution when compiling IDL files in this mode.</span></span> <span data-ttu-id="24937-118">在混合模式中使用多維陣列可能會導致未正確封送處理的參數。</span><span class="sxs-lookup"><span data-stu-id="24937-118">Using multidimensional arrays in mixed mode can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="24937-119">當您的介面定義屬於多維陣列的參數時，建議使用 [**/Oicf**](/windows/desktop/Midl/-oi) 命令列參數。</span><span class="sxs-lookup"><span data-stu-id="24937-119">The [**/Oicf**](/windows/desktop/Midl/-oi) command line switch is recommended when your interface defines parameters that are multidimensional arrays.</span></span>

 

<span data-ttu-id="24937-120">\[[**字串**](/windows/desktop/Midl/string) \] 屬性也可以搭配多維度陣列使用。</span><span class="sxs-lookup"><span data-stu-id="24937-120">The \[[**string**](/windows/desktop/Midl/string)\] attribute can also be used with multidimensional arrays.</span></span> <span data-ttu-id="24937-121">屬性會套用至最不重要的維度，例如符合標準的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="24937-121">The attribute applies to the least significant dimension, such as a conformant array of strings.</span></span> <span data-ttu-id="24937-122">您也可以使用多維度指標屬性。</span><span class="sxs-lookup"><span data-stu-id="24937-122">You can also use multidimensional pointer attributes.</span></span> <span data-ttu-id="24937-123">例如：</span><span class="sxs-lookup"><span data-stu-id="24937-123">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

<span data-ttu-id="24937-124">在上述範例中，變數 ptr2d 是指標，指向 d1len 大小的指標區塊，其中每個指標都會指向 **long** 的 d2len 指標。</span><span class="sxs-lookup"><span data-stu-id="24937-124">In the preceding example, the variable ptr2d is a pointer to a d1len-sized block of pointers, each of which points to d2len pointers to **long**.</span></span>

<span data-ttu-id="24937-125">多維陣列與指標陣列不相等。</span><span class="sxs-lookup"><span data-stu-id="24937-125">Multidimensional arrays are not equivalent to arrays of pointers.</span></span> <span data-ttu-id="24937-126">多維陣列是記憶體中的單一大型資料區塊。</span><span class="sxs-lookup"><span data-stu-id="24937-126">A multidimensional array is a single, large block of data in memory.</span></span> <span data-ttu-id="24937-127">指標的陣列只包含陣列中指標的區塊。</span><span class="sxs-lookup"><span data-stu-id="24937-127">An array of pointers only contains a block of pointers in the array.</span></span> <span data-ttu-id="24937-128">指標指向的資料可以是記憶體中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="24937-128">The data that the pointers point to can be anywhere in memory.</span></span> <span data-ttu-id="24937-129">此外，ANSI C 語法只允許在多維度陣列中未指定最大 (最左邊的) 陣列維度。</span><span class="sxs-lookup"><span data-stu-id="24937-129">Also, ANSI C syntax allows only the most significant (leftmost) array dimension to be unspecified in a multidimensional array.</span></span> <span data-ttu-id="24937-130">因此，下列是有效的語句：</span><span class="sxs-lookup"><span data-stu-id="24937-130">Therefore, the following is a valid statement:</span></span>

`long a1[] [20]`

<span data-ttu-id="24937-131">將此語句與下列不正確語句進行比較：</span><span class="sxs-lookup"><span data-stu-id="24937-131">Compare this to the following invalid statement:</span></span>

`long a1[20] []`

 

 