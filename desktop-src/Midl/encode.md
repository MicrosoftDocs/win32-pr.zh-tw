---
title: 編碼屬性
description: '\ 編碼 \ ACF 屬性指定程式或資料類型需要序列化支援。'
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- 編碼屬性 MIDL
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933119"
---
# <a name="encode-attribute"></a><span data-ttu-id="08342-104">編碼屬性</span><span class="sxs-lookup"><span data-stu-id="08342-104">encode attribute</span></span>

<span data-ttu-id="08342-105">**\[ 編碼 \]** ACF 屬性指定程式或資料類型需要序列化支援。</span><span class="sxs-lookup"><span data-stu-id="08342-105">The **\[encode\]** ACF attribute specifies that a procedure or a data type needs serialization support.</span></span>

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a><span data-ttu-id="08342-106">參數</span><span class="sxs-lookup"><span data-stu-id="08342-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08342-107">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="08342-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="08342-108">指定適用于整個介面的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="08342-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="08342-109">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="08342-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="08342-110">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="08342-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="08342-111">*介面定義*</span><span class="sxs-lookup"><span data-stu-id="08342-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="08342-112">指定組成介面定義的 IDL 語句。</span><span class="sxs-lookup"><span data-stu-id="08342-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="08342-113">*op-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="08342-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="08342-114">指定適用于程式的其他操作屬性，例如解碼 **\[** [](decode.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="08342-114">Specifies other operational attributes that apply to the procedure such as **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="08342-115">*進程名稱*</span><span class="sxs-lookup"><span data-stu-id="08342-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="08342-116">指定程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="08342-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="08342-117">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="08342-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="08342-118">指定適用于類型的其他屬性，例如解碼 **\[** [](decode.md) **\]** 和 **\[** [**配置**](allocate.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="08342-118">Specifies other attributes that apply to the type such as **\[**[**decode**](decode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="08342-119">*類型名稱*</span><span class="sxs-lookup"><span data-stu-id="08342-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="08342-120">指定 IDL 檔案中定義的類型。</span><span class="sxs-lookup"><span data-stu-id="08342-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08342-121">備註</span><span class="sxs-lookup"><span data-stu-id="08342-121">Remarks</span></span>

<span data-ttu-id="08342-122">**\[ 編碼 \]** 屬性會導致 MIDL 編譯器產生程式碼，應用程式可以使用該程式碼將資料序列化為緩衝區。</span><span class="sxs-lookup"><span data-stu-id="08342-122">The **\[encode\]** attribute causes the MIDL compiler to generate code that an application can use to serialize data into a buffer.</span></span> <span data-ttu-id="08342-123">解碼 **\[** [](decode.md) **\]** 屬性會產生用來從緩衝區封送資料的程式碼。</span><span class="sxs-lookup"><span data-stu-id="08342-123">The **\[**[**decode**](decode.md)**\]** attribute generates the code for unmarshaling data from a buffer.</span></span>

<span data-ttu-id="08342-124">使用 ACF 中的 **\[ \] 編碼** 和解碼 **\[** [](decode.md) **\]** 屬性，為介面的 IDL 檔中定義的程式或類型產生序列化程式碼。</span><span class="sxs-lookup"><span data-stu-id="08342-124">Use the **\[encode\]** and **\[**[**decode**](decode.md)**\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="08342-125">當做介面屬性使用時，會將 **\[ 編碼 \]** 套用至 IDL 檔案中定義的所有類型和程式。</span><span class="sxs-lookup"><span data-stu-id="08342-125">When used as an interface attribute, **\[encode\]** applies to all the types and procedures defined in the IDL file.</span></span> <span data-ttu-id="08342-126">當做操作屬性使用時，只會將 **\[ 編碼 \]** 套用至指定的程式。</span><span class="sxs-lookup"><span data-stu-id="08342-126">When used as an operational attribute, **\[encode\]** applies only to the specified procedure.</span></span> <span data-ttu-id="08342-127">當做型別屬性使用時，只會將 **\[ 編碼 \]** 套用至指定的型別。</span><span class="sxs-lookup"><span data-stu-id="08342-127">When used as a type attribute, **\[encode\]** applies only to the specified type.</span></span>

<span data-ttu-id="08342-128">當 **\[ 編碼 \]** 或解碼 **\[** [](decode.md) **\]** 屬性套用至程式時，MIDL 編譯器會以類似的方式產生序列化存根，以產生遠端常式的遠端存根。</span><span class="sxs-lookup"><span data-stu-id="08342-128">When the **\[encode\]** or **\[**[**decode**](decode.md)**\]** attribute is applied to a procedure, the MIDL compiler generates a serialization stub in a similar fashion as remote stubs are generated for remote routines.</span></span> <span data-ttu-id="08342-129">程式可以是遠端或序列化程式，但不能同時為這兩種方法。</span><span class="sxs-lookup"><span data-stu-id="08342-129">A procedure can be either a remote or a serializing procedure, but it cannot be both.</span></span> <span data-ttu-id="08342-130">產生之常式的原型會傳送至存根。H 檔案，而存根本身會進入存根的 \_ c. 檔案。</span><span class="sxs-lookup"><span data-stu-id="08342-130">The prototype of the generated routine is sent to the STUB.H file while the stub itself goes into the STUB\_C.C file.</span></span>

<span data-ttu-id="08342-131">MIDL 編譯器會針對 **\[ 編碼 \]** 屬性所套用的每個類型產生兩個函式，並針對解碼 **\[** 屬性套用的每個類型產生一個 [**額外的函**](decode.md)式 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="08342-131">The MIDL compiler generates two functions for each type the **\[encode\]** attribute applies to, and one additional function for each type the **\[**[**decode**](decode.md)**\]** attribute applies to.</span></span> <span data-ttu-id="08342-132">例如，針對名為 MyType 的使用者定義型別，編譯器會針對 MyType \_ 編碼、MyType 解碼 \_ 和 MyType AlignSize 函數產生程式碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="08342-132">For example, for a user-defined type named MyType, the compiler generates code for the MyType\_Encode, MyType\_Decode, and MyType\_AlignSize functions.</span></span> <span data-ttu-id="08342-133">針對這些函式，編譯器會將原型寫入存根。H 和來源程式碼至 STUB \_ C.C。</span><span class="sxs-lookup"><span data-stu-id="08342-133">For these functions, the compiler writes prototypes to STUB.H and source code to STUB\_C.C.</span></span>

<span data-ttu-id="08342-134">如需有關序列化控制碼和編碼或解碼資料的詳細資訊，請參閱 [序列化服務](/windows/desktop/Rpc/serialization-services)。</span><span class="sxs-lookup"><span data-stu-id="08342-134">For additional information about serialization handles and encoding or decoding data, see [Serialization Services](/windows/desktop/Rpc/serialization-services).</span></span>

## <a name="examples"></a><span data-ttu-id="08342-135">範例</span><span class="sxs-lookup"><span data-stu-id="08342-135">Examples</span></span>

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a><span data-ttu-id="08342-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08342-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08342-137">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="08342-137">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="08342-138">**分配**</span><span class="sxs-lookup"><span data-stu-id="08342-138">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="08342-139">**解碼**</span><span class="sxs-lookup"><span data-stu-id="08342-139">**decode**</span></span>](decode.md)
</dt> </dl>

 

 