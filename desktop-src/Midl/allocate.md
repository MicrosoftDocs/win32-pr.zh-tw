---
title: 配置屬性
description: '\ 配置 \ ACF 屬性可讓您自訂 IDL 檔案中定義之類型的記憶體配置和解除配置。'
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- 配置屬性 MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841155"
---
# <a name="allocate-attribute"></a><span data-ttu-id="43d10-104">配置屬性</span><span class="sxs-lookup"><span data-stu-id="43d10-104">allocate attribute</span></span>

<span data-ttu-id="43d10-105">**\[ 配置 \]** ACF 屬性可讓您自訂 IDL 檔案中定義之類型的記憶體配置和解除配置。</span><span class="sxs-lookup"><span data-stu-id="43d10-105">The **\[allocate\]** ACF attribute lets you customize memory allocation and deallocation for a type defined in the IDL file.</span></span>

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="43d10-106">參數</span><span class="sxs-lookup"><span data-stu-id="43d10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d10-107">*配置-選項-清單*</span><span class="sxs-lookup"><span data-stu-id="43d10-107">*allocate-option-list*</span></span> 
</dt> <dd>

<span data-ttu-id="43d10-108">指定一或多個記憶體配置選項。</span><span class="sxs-lookup"><span data-stu-id="43d10-108">Specifies one or more memory-allocation options.</span></span> <span data-ttu-id="43d10-109">選取 **單一 \_ 節點** 或 **所有 \_ 節點** 的其中一個節點，或選取 [ **免費** ] 或 [ **無 \_ 可用**] 或 [每一組] 中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="43d10-109">Select one of either **single\_node** or **all\_nodes**, or one of either **free** or **dont\_free**, or one from each pair.</span></span> <span data-ttu-id="43d10-110">當您指定一個以上的選項時，請以逗號分隔選項。</span><span class="sxs-lookup"><span data-stu-id="43d10-110">When you specify more than one option, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="43d10-111">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="43d10-111">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="43d10-112">指定其他選擇性的 ACF 型別屬性。</span><span class="sxs-lookup"><span data-stu-id="43d10-112">Specifies other optional ACF-type attributes.</span></span> <span data-ttu-id="43d10-113">當您指定一個以上的類型屬性時，請以逗號分隔選項。</span><span class="sxs-lookup"><span data-stu-id="43d10-113">When you specify more than one type attribute, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="43d10-114">*類型名稱*</span><span class="sxs-lookup"><span data-stu-id="43d10-114">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="43d10-115">指定 IDL 檔案中定義的類型。</span><span class="sxs-lookup"><span data-stu-id="43d10-115">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43d10-116">備註</span><span class="sxs-lookup"><span data-stu-id="43d10-116">Remarks</span></span>

<span data-ttu-id="43d10-117">**\[ 配置 \]** 屬性具有下列有效的選項。</span><span class="sxs-lookup"><span data-stu-id="43d10-117">The **\[allocate\]** attribute has the following valid options.</span></span>



| <span data-ttu-id="43d10-118">選項</span><span class="sxs-lookup"><span data-stu-id="43d10-118">Option</span></span>           | <span data-ttu-id="43d10-119">Description</span><span class="sxs-lookup"><span data-stu-id="43d10-119">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="43d10-120">**所有 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="43d10-120">**all\_nodes**</span></span>   | <span data-ttu-id="43d10-121">建立一個呼叫，以針對所有節點配置和釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="43d10-121">Makes one call to allocate and free memory for all nodes.</span></span>             |
| <span data-ttu-id="43d10-122">**單一 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="43d10-122">**single\_node**</span></span> | <span data-ttu-id="43d10-123">進行許多個別呼叫，以配置和釋放每個記憶體節點。</span><span class="sxs-lookup"><span data-stu-id="43d10-123">Makes many individual calls to allocate and free each node of memory.</span></span> |
| <span data-ttu-id="43d10-124">**free**</span><span class="sxs-lookup"><span data-stu-id="43d10-124">**free**</span></span>         | <span data-ttu-id="43d10-125">從伺服器 stub 傳回時釋出記憶體。</span><span class="sxs-lookup"><span data-stu-id="43d10-125">Frees memory on return from the server stub.</span></span>                          |
| <span data-ttu-id="43d10-126">**\_免費**</span><span class="sxs-lookup"><span data-stu-id="43d10-126">**dont\_free**</span></span>   | <span data-ttu-id="43d10-127">從伺服器 stub 傳回時，不會釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="43d10-127">Does not free memory on return from the server stub.</span></span>                  |



 

<span data-ttu-id="43d10-128">根據預設，存根可以針對每個指標個別呼叫 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md) 和 [**midl \_ 使用者 \_**](midl-user-free-1.md) ，來為唯一或完整指標所參考的資料配置儲存區。</span><span class="sxs-lookup"><span data-stu-id="43d10-128">By default, the stubs may allocate storage for data referenced by a unique or full pointer by calling [**midl\_user\_allocate**](midl-user-allocate-1.md) and [**midl\_user\_free**](midl-user-free-1.md) individually for each pointer.</span></span>

<span data-ttu-id="43d10-129">您可以藉由指定 **all \_ 節點** 選項來優化應用程式的速度。</span><span class="sxs-lookup"><span data-stu-id="43d10-129">You can optimize the speed of your application by specifying the option **all\_nodes**.</span></span> <span data-ttu-id="43d10-130">此選項會指示存根計算透過指定類型的指標所參考的所有記憶體大小，以及對 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md)進行單一呼叫。</span><span class="sxs-lookup"><span data-stu-id="43d10-130">This option directs the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span> <span data-ttu-id="43d10-131">存根會藉由對 [**midl \_ 使用者 \_ 免費**](midl-user-free-1.md)進行一次呼叫來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="43d10-131">The stub releases the memory by making one call to [**midl\_user\_free**](midl-user-free-1.md).</span></span>

<span data-ttu-id="43d10-132">Not **\_ free** 選項會指示 MIDL 編譯器產生不會針對指定的型別呼叫 [**MIDL \_ 使用者 \_ free**](midl-user-free-1.md) 的伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="43d10-132">The **dont\_free** option directs the MIDL compiler to generate a server stub that does not call [**midl\_user\_free**](midl-user-free-1.md) for the specified type.</span></span> <span data-ttu-id="43d10-133">[ **無 \_ 可用** ] 選項允許在遠端程序呼叫完成並傳回用戶端之後，讓伺服器應用程式能夠存取指標結構。</span><span class="sxs-lookup"><span data-stu-id="43d10-133">The **dont\_free** option allows the pointer structures to remain accessible to the server application after the remote procedure call has completed and returned to the client.</span></span>

<span data-ttu-id="43d10-134">**\[ 配置 \]** 屬性將會導致任何 **\[ in、out \]** 參數（其為以 [**所有 \_ 節點**] 選項限定的型別指標），以在資料取消封送處理時重新配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="43d10-134">The **\[allocate\]** attribute will cause any **\[in, out\]** parameter that is a pointer to a type qualified with the **all\_nodes** option to reallocate memory when the data is unmarshaled.</span></span> <span data-ttu-id="43d10-135">應用程式必須負責釋放先前為此參數所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="43d10-135">It is the responsibility of the application to free the memory allocated previously for this parameter.</span></span> <span data-ttu-id="43d10-136">例如：</span><span class="sxs-lookup"><span data-stu-id="43d10-136">For example:</span></span>

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

<span data-ttu-id="43d10-137">資料類型 PTHISTYPE 會在封送之前由存根以 [**\[ 輸出 \]**](out-idl.md)方向重新配置。</span><span class="sxs-lookup"><span data-stu-id="43d10-137">The data type PTHISTYPE will be reallocated in the [**\[out\]**](out-idl.md) direction by the stub before unmarshaling.</span></span> <span data-ttu-id="43d10-138">因此，應用程式必須釋放先前為此參數資料配置的記憶體，否則會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="43d10-138">Therefore, the application must free the memory it previously allocated for this parameter's data, or a memory leak will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="43d10-139">範例</span><span class="sxs-lookup"><span data-stu-id="43d10-139">Examples</span></span>

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a><span data-ttu-id="43d10-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43d10-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d10-141">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="43d10-141">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="43d10-142">**在**</span><span class="sxs-lookup"><span data-stu-id="43d10-142">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="43d10-143">**midl \_ 使用者 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="43d10-143">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="43d10-144">**midl \_ 使用者 \_ 免費**</span><span class="sxs-lookup"><span data-stu-id="43d10-144">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="43d10-145">**擴展**</span><span class="sxs-lookup"><span data-stu-id="43d10-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="43d10-146">**著**</span><span class="sxs-lookup"><span data-stu-id="43d10-146">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




