---
title: MIDL 陣列
description: MIDL 陣列。
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- 資料類型 MIDL、陣列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023421"
---
# <a name="midl-arrays"></a><span data-ttu-id="8358b-104">MIDL 陣列</span><span class="sxs-lookup"><span data-stu-id="8358b-104">MIDL Arrays</span></span>

<span data-ttu-id="8358b-105">陣列宣告子會在 IDL 檔案的介面主體中顯示為下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="8358b-105">Array declarators appear in the interface body of the IDL file as one of the following:</span></span>

-   <span data-ttu-id="8358b-106">一般宣告的一部分</span><span class="sxs-lookup"><span data-stu-id="8358b-106">Part of a general declaration</span></span>
-   <span data-ttu-id="8358b-107">結構或等位宣告子的成員</span><span class="sxs-lookup"><span data-stu-id="8358b-107">A member of a structure or union declarator</span></span>
-   <span data-ttu-id="8358b-108">遠端程序呼叫的參數</span><span class="sxs-lookup"><span data-stu-id="8358b-108">A parameter to a remote procedure call</span></span>

<span data-ttu-id="8358b-109">陣列中每個維度的界限都會以一組不同的方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="8358b-109">The bounds of each dimension of the array are expressed inside a separate pair of square brackets.</span></span> <span data-ttu-id="8358b-110">評估為 *n* 的運算式表示零的下限和 *n-1* 的上限。</span><span class="sxs-lookup"><span data-stu-id="8358b-110">An expression that evaluates to *n* signifies a lower bound of zero and an upper bound of *n - 1*.</span></span> <span data-ttu-id="8358b-111">如果方括弧是空的，或包含單一星號 (\*) ，下限為零，而上限是在執行時間決定。</span><span class="sxs-lookup"><span data-stu-id="8358b-111">If the square brackets are empty or contain a single asterisk (\*), the lower bound is zero and the upper bound is determined at runtime.</span></span>

<span data-ttu-id="8358b-112">陣列也可以包含兩個值，並以表示陣列的下限和上限的省略號分隔，如下 \[ 所示。*上方* \] 。</span><span class="sxs-lookup"><span data-stu-id="8358b-112">The array can also contain two values separated by an ellipsis that represent the lower and upper bounds of the array, as in \[*lower*...*upper*\].</span></span> <span data-ttu-id="8358b-113">Microsoft RPC 需要的下限為零。</span><span class="sxs-lookup"><span data-stu-id="8358b-113">Microsoft RPC requires a lower bound of zero.</span></span> <span data-ttu-id="8358b-114">MIDL 編譯器無法辨識指定非零下限的結構。</span><span class="sxs-lookup"><span data-stu-id="8358b-114">The MIDL compiler does not recognize constructs that specify nonzero lower bounds.</span></span>

<span data-ttu-id="8358b-115">陣列可以與欄位屬性大小相關聯，[**最大值 \_**](max-is.md)為，[**長度 \_ 為**](length-is.md)，[**第一個 \_ 是**](first-is.md)，[**最後 \_ 是**](last-is.md)指定陣列的大小或陣列中包含有效資料的部分。 [**\_**](size-is.md)</span><span class="sxs-lookup"><span data-stu-id="8358b-115">Arrays can be associated with the field attributes [**size\_is**](size-is.md), [**max\_is**](max-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), and [**last\_is**](last-is.md) to specify the size of the array or the part of the array that contains valid data.</span></span> <span data-ttu-id="8358b-116">這些欄位屬性會識別指定陣列維度或索引的參數、結構欄位或常數。</span><span class="sxs-lookup"><span data-stu-id="8358b-116">These field attributes identify the parameter, structure field, or constant that specifies the array dimension or index.</span></span>

<span data-ttu-id="8358b-117">陣列必須與 field 屬性指定的識別碼相關聯，方法如下：當陣列是參數時，識別碼也必須是相同函式的參數。當陣列是結構欄位時，識別碼必須是相同結構的另一個結構欄位。</span><span class="sxs-lookup"><span data-stu-id="8358b-117">The array must be associated with the identifier specified by the field attribute in the following way: When the array is a parameter, the identifier must also be a parameter to the same function; when the array is a structure field, the identifier must be another structure field of that same structure.</span></span>

<span data-ttu-id="8358b-118">如果任何維度的上限都是在執行時間決定的，則陣列稱為「一致」。</span><span class="sxs-lookup"><span data-stu-id="8358b-118">An array is called "conformant" if the upper bound of any dimension is determined at runtime.</span></span> <span data-ttu-id="8358b-119"> (只有上限可在執行時間決定。 ) 若要判斷上限，陣列宣告必須包含 [大小] 或 [**[ \_**](size-is.md) [**最大值 \_**](max-is.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="8358b-119">(Only upper bounds can be determined at runtime.) To determine the upper bound, the array declaration must include a [**size\_is**](size-is.md) or [**max\_is**](max-is.md) attribute.</span></span>

<span data-ttu-id="8358b-120">當陣列的界限是在編譯時期決定時，陣列稱為「變動」，但是傳輸的元素範圍是在執行時間決定。</span><span class="sxs-lookup"><span data-stu-id="8358b-120">An array is called "varying" when its bounds are determined at compile time, but the range of transmitted elements is determined at runtime.</span></span> <span data-ttu-id="8358b-121">若要判斷已傳送的元素範圍，陣列宣告必須包含 [**長度 \_ 為**](length-is.md)、 [**第一個 \_ 為**](first-is.md)，或 [**最後一個 \_ 是**](last-is.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="8358b-121">To determine the range of transmitted elements, the array declaration must include a [**length\_is**](length-is.md), [**first\_is**](first-is.md), or [**last\_is**](last-is.md) attribute.</span></span>

<span data-ttu-id="8358b-122">一致的不同陣列 (也稱為「開啟」 ) 是一個陣列，其上限和傳送的元素範圍是在執行時間決定。</span><span class="sxs-lookup"><span data-stu-id="8358b-122">A conformant varying array (also called "open") is an array whose upper bound and range of transmitted elements are determined at runtime.</span></span> <span data-ttu-id="8358b-123">最多可以在 C 結構中嵌套一個符合或一致的不同陣列，而且必須是結構的最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="8358b-123">At most, one conformant or conformant varying array can be nested in a C structure and must be the last element of the structure.</span></span> <span data-ttu-id="8358b-124">相反地，nonconformant 變化的陣列可以出現在結構中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="8358b-124">In contrast, nonconformant varying arrays can occur anywhere in a structure.</span></span>

## <a name="examples"></a><span data-ttu-id="8358b-125">範例</span><span class="sxs-lookup"><span data-stu-id="8358b-125">Examples</span></span>

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

<span data-ttu-id="8358b-126">如需詳細資訊，請參閱 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="8358b-126">For more information, see [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

## <a name="multidimensional-arrays"></a><span data-ttu-id="8358b-127">多維陣列</span><span class="sxs-lookup"><span data-stu-id="8358b-127">Multidimensional Arrays</span></span>

<span data-ttu-id="8358b-128">使用者可以宣告類型為數組，然後宣告這類類型的物件陣列。</span><span class="sxs-lookup"><span data-stu-id="8358b-128">The user can declare types that are arrays and then declare arrays of objects of such types.</span></span> <span data-ttu-id="8358b-129">*N* 維度陣列類型的 *m* 維度陣列的語法與 *m* + *n* 維度陣列的語法相同。</span><span class="sxs-lookup"><span data-stu-id="8358b-129">The semantics of *m*-dimensional arrays of *n*-dimensional array types are the same as the semantics of *m*+*n*-dimensional arrays.</span></span>

<span data-ttu-id="8358b-130">例如，型別 RECT \_ 型別可以定義為二維陣列，而變數 *RECT* 可以定義為 RECT 型別的陣列 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8358b-130">For example, the type RECT\_TYPE can be defined as a two-dimensional array and the variable *rect* can be defined as an array of RECT\_TYPE.</span></span> <span data-ttu-id="8358b-131">這相當於三維陣列的 *相等 \_ 矩形*：</span><span class="sxs-lookup"><span data-stu-id="8358b-131">This is equivalent to the three-dimensional array *equivalent\_rect*:</span></span>

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

<span data-ttu-id="8358b-132">Microsoft RPC 為 C 導向。</span><span class="sxs-lookup"><span data-stu-id="8358b-132">Microsoft RPC is C oriented.</span></span> <span data-ttu-id="8358b-133">遵循 C 語言慣例，只有多維陣列的第一個維度可以在執行時間決定。</span><span class="sxs-lookup"><span data-stu-id="8358b-133">Following C-language conventions, only the first dimension of a multidimensional array can be determined at runtime.</span></span> <span data-ttu-id="8358b-134">與支援其他語言之 DCE IDL 陣列的互通性限制為：</span><span class="sxs-lookup"><span data-stu-id="8358b-134">Interoperation with DCE IDL arrays that support other languages is limited to:</span></span>

-   <span data-ttu-id="8358b-135">具有常數的多維度陣列 (編譯時間決定的) 界限。</span><span class="sxs-lookup"><span data-stu-id="8358b-135">Multidimensional arrays with constant (compile-time-determined) bounds.</span></span>
-   <span data-ttu-id="8358b-136">具有所有常數界限（第一個維度除外）的多維度陣列。</span><span class="sxs-lookup"><span data-stu-id="8358b-136">Multidimensional arrays with all constant bounds except the first dimension.</span></span> <span data-ttu-id="8358b-137">第一個維度的已傳輸元素上限和範圍取決於執行時間。</span><span class="sxs-lookup"><span data-stu-id="8358b-137">The upper bound and range of transmitted elements of the first dimension are dependent on runtime.</span></span>
-   <span data-ttu-id="8358b-138">具有零下限的任何一維陣列。</span><span class="sxs-lookup"><span data-stu-id="8358b-138">Any one-dimensional arrays with a lower bound of zero.</span></span>

<span data-ttu-id="8358b-139">當 **\[** [**字串**](string.md) **\]** 屬性用於多維度陣列時，屬性會套用至最右邊的陣列。</span><span class="sxs-lookup"><span data-stu-id="8358b-139">When the **\[**[**string**](string.md)**\]** attribute is used on multidimensional arrays, the attribute applies to the rightmost array.</span></span>

## <a name="arrays-of-pointers"></a><span data-ttu-id="8358b-140">指標陣列</span><span class="sxs-lookup"><span data-stu-id="8358b-140">Arrays of Pointers</span></span>

<span data-ttu-id="8358b-141">參考指標必須指向有效的資料。</span><span class="sxs-lookup"><span data-stu-id="8358b-141">Reference pointers must point to valid data.</span></span> <span data-ttu-id="8358b-142">用戶端應用程式必須為 **\[** [**in**](in.md) **\]** 或 **\[** **in、**[**out**](out-idl.md)參考指標陣列中的所有記憶體配置 **\]** ，尤其是當陣列與 **\[ in \]**、 **\[** **in、 \] out**、 **\[** [**length \_ 為**](length-is.md) **\]** 或 **\[** [**last \_ 為**](last-is.md) **\]** 值時。</span><span class="sxs-lookup"><span data-stu-id="8358b-142">The client application must allocate all memory for an **\[**[**in**](in.md)**\]** or **\[** **in,**[**out**](out-idl.md)**\]** array of reference pointers, especially when the array is associated with **\[in\]**, or **\[** **in,out\]**, **\[**[**length\_is**](length-is.md)**\]**, or **\[**[**last\_is**](last-is.md)**\]** values.</span></span> <span data-ttu-id="8358b-143">用戶端應用程式也必須在呼叫之前初始化所有陣列元素。</span><span class="sxs-lookup"><span data-stu-id="8358b-143">The client application must also initialize all array elements before the call.</span></span> <span data-ttu-id="8358b-144">回到用戶端之前，伺服器應用程式必須確認傳送的範圍中的所有陣列元素都指向有效的儲存體。</span><span class="sxs-lookup"><span data-stu-id="8358b-144">Before returning to the client, the server application must verify that all array elements in the transmitted range point to valid storage.</span></span>

<span data-ttu-id="8358b-145">在伺服器端上，存根會為所有陣列元素配置儲存體，而不管在 **\[** 呼叫時，[**長度 \_ 為**](length-is.md) **\]** 或 **\[** [**最後 \_ 一個**](last-is.md) **\]** 值。</span><span class="sxs-lookup"><span data-stu-id="8358b-145">On the server side, the stub allocates storage for all array elements, regardless of the **\[**[**length\_is**](length-is.md)**\]** or **\[**[**last\_is**](last-is.md)**\]** value at the time of the call.</span></span> <span data-ttu-id="8358b-146">這項功能可能會影響應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="8358b-146">This feature can affect the performance of your application.</span></span>

<span data-ttu-id="8358b-147">唯一指標的陣列沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="8358b-147">No restrictions are placed on arrays of unique pointers.</span></span> <span data-ttu-id="8358b-148">在用戶端和伺服器上，儲存體都會配置給 null 指標。</span><span class="sxs-lookup"><span data-stu-id="8358b-148">On both the client and the server, storage is allocated for null pointers.</span></span> <span data-ttu-id="8358b-149">當指標為非 null 時，資料會放在預先配置的儲存體中。</span><span class="sxs-lookup"><span data-stu-id="8358b-149">When pointers are non-null, data is placed in preallocated storage.</span></span>

<span data-ttu-id="8358b-150">選擇性的指標宣告子可以在陣列宣告子前面。</span><span class="sxs-lookup"><span data-stu-id="8358b-150">An optional pointer declarator can precede the array declarator.</span></span>

<span data-ttu-id="8358b-151">當內嵌參考指標是 **\[** [](out-idl.md) **\]** 僅限輸出的參數時，伺服器管理員程式碼必須將有效值指派給參考指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="8358b-151">When embedded reference pointers are **\[**[**out**](out-idl.md)**\]**-only parameters, the server-manager code must assign valid values to the array of reference pointers.</span></span> <span data-ttu-id="8358b-152">例如：</span><span class="sxs-lookup"><span data-stu-id="8358b-152">For example:</span></span>

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

<span data-ttu-id="8358b-153">產生的存根會配置陣列，並將 null 值指派給內嵌于陣列中的所有指標。</span><span class="sxs-lookup"><span data-stu-id="8358b-153">The generated stubs allocate the array and assign null values to all pointers embedded in the array.</span></span>

 

 