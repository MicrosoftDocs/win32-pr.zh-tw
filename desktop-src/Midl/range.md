---
title: range 屬性
description: '\ Range \ 屬性可讓您指定引數或欄位的允許值範圍，其值會在執行時間設定。 當與管道類型搭配使用時，屬性會針對管道區塊中的元素計數指定允許的範圍。'
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- 範圍屬性 MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106979666"
---
# <a name="range-attribute"></a><span data-ttu-id="945b1-105">range 屬性</span><span class="sxs-lookup"><span data-stu-id="945b1-105">range attribute</span></span>

<span data-ttu-id="945b1-106">**\[ 範圍 \]** 屬性可讓您指定引數或欄位的允許值範圍，其值會在執行時間進行設定。</span><span class="sxs-lookup"><span data-stu-id="945b1-106">The **\[range\]** attribute lets you specify a range of allowable values for arguments or fields whose values are set at run time.</span></span> <span data-ttu-id="945b1-107">當與管道類型搭配使用時，屬性會針對管道區塊中的元素計數指定允許的範圍。</span><span class="sxs-lookup"><span data-stu-id="945b1-107">When used with a pipe type, the attribute specifies the allowable range for the count of elements in the pipe chunks.</span></span>

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a><span data-ttu-id="945b1-108">參數</span><span class="sxs-lookup"><span data-stu-id="945b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="945b1-109">*低-val*</span><span class="sxs-lookup"><span data-stu-id="945b1-109">*low-val*</span></span> 
</dt> <dd>

<span data-ttu-id="945b1-110">參數或欄位可以容納的最小允許值。</span><span class="sxs-lookup"><span data-stu-id="945b1-110">The lowest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="945b1-111">*高 val*</span><span class="sxs-lookup"><span data-stu-id="945b1-111">*high-val*</span></span> 
</dt> <dd>

<span data-ttu-id="945b1-112">參數或欄位可以容納的最大允許值。</span><span class="sxs-lookup"><span data-stu-id="945b1-112">The highest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="945b1-113">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="945b1-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="945b1-114">非 [**超**](hyper.md)整數類型或 [**\_ \_ int64**](--int64.md)以外的整數類資料類型、整數型別的型別識別碼、[**列舉**](enum.md)型別或管道型別名稱。</span><span class="sxs-lookup"><span data-stu-id="945b1-114">An integral type other than [**hyper**](hyper.md) or [**\_\_int64**](--int64.md), a type identifier to an integral type, an [**enum**](enum.md) type, or a pipe type name.</span></span>

</dd> <dt>

<span data-ttu-id="945b1-115">*符中*</span><span class="sxs-lookup"><span data-stu-id="945b1-115">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="945b1-116">標準 C 宣告子，例如識別碼。</span><span class="sxs-lookup"><span data-stu-id="945b1-116">A standard C declarator, such as an identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="945b1-117">備註</span><span class="sxs-lookup"><span data-stu-id="945b1-117">Remarks</span></span>

<span data-ttu-id="945b1-118">您可以使用 [ **\[ 範圍 \]** ] 屬性來修改敏感性參數或欄位的意義，例如，用於大小或長度、具有一致或不同陣列的意義; 或每次您想要針對有效值的範圍檢查參數或域值。</span><span class="sxs-lookup"><span data-stu-id="945b1-118">Use the **\[range\]** attribute to modify the meaning of sensitive parameters or fields, such as those used for size or length, with conformant or varying arrays; or whenever you want to check a parameter or field value against a range of valid values.</span></span> <span data-ttu-id="945b1-119">屬性適用于最上層參數，以及較低層級的參數和欄位。</span><span class="sxs-lookup"><span data-stu-id="945b1-119">The attribute is applicable to top-level parameters as well as lower-level parameters and fields.</span></span> <span data-ttu-id="945b1-120">將 **\[ range \]** 屬性加入至類型並不會變更其電傳格式，因此不會影響回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="945b1-120">Adding the **\[range\]** attribute to a type does not change its wire format, thus does not affect backward compatibility.</span></span>

<span data-ttu-id="945b1-121">**\[ 範圍 \]** 屬性也可以用於符合規範的資料，例如緩衝區或具有一致性屬性的陣列。</span><span class="sxs-lookup"><span data-stu-id="945b1-121">The **\[range\]** attribute can also be used on conformant data such as buffers or arrays with a conformance attribute.</span></span> <span data-ttu-id="945b1-122">其效果是將一致資料的所有一致性大小限制為指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="945b1-122">The effect is to limit all conformance sizes for the conformant data to the specified range.</span></span> <span data-ttu-id="945b1-123">如果一致的資料是多維陣列，則每個陣列維度都會限制為指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="945b1-123">If the conformant data is a multi-dimensional array, each array dimension is limited to the specified range.</span></span>

<span data-ttu-id="945b1-124">在一致的資料上使用 **\[ 範圍 \]** 需要編譯目標為「目標 NT60 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="945b1-124">Use of **\[range\]** on conformant data requires that the compilation target be â€“target NT60 or higher.</span></span>

<span data-ttu-id="945b1-125">請注意，當您編譯 IDL 檔案時，必須使用 [**/robust**](-robust.md) 編譯器選項，才能產生將執行這些檢查的 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="945b1-125">Note that you must use the [**/robust**](-robust.md) compiler option when you compile your IDL file in order to generate the stub code that will perform these checks.</span></span> <span data-ttu-id="945b1-126">在沒有 **/robust** 參數的情況下，MIDL 編譯器會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="945b1-126">Without the **/robust** switch, the MIDL compiler ignores this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="945b1-127">範例</span><span class="sxs-lookup"><span data-stu-id="945b1-127">Examples</span></span>

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a><span data-ttu-id="945b1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="945b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945b1-129"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="945b1-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="945b1-130">陣列</span><span class="sxs-lookup"><span data-stu-id="945b1-130">arrays</span></span>](/windows/desktop/Rpc/arrays)
</dt> <dt>

[<span data-ttu-id="945b1-131">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="945b1-131">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="945b1-132">**last \_**</span><span class="sxs-lookup"><span data-stu-id="945b1-132">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="945b1-133">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="945b1-133">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="945b1-134">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="945b1-134">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="945b1-135">**/robust**</span><span class="sxs-lookup"><span data-stu-id="945b1-135">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="945b1-136">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="945b1-136">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="945b1-137">**切換 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="945b1-137">**switch\_is**</span></span>](switch-is.md)
</dt> </dl>

 

 