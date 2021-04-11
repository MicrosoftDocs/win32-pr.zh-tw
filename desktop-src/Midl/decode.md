---
title: 解碼屬性
description: '\ 解碼 \ ACF 屬性指定程式或類型需要還原序列化支援。'
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- 解碼屬性 MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314905"
---
# <a name="decode-attribute"></a><span data-ttu-id="138c0-104">解碼屬性</span><span class="sxs-lookup"><span data-stu-id="138c0-104">decode attribute</span></span>

<span data-ttu-id="138c0-105">解碼 ACF 屬性指定程式或類型需要還原序列化支援。 **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="138c0-105">The **\[decode\]** ACF attribute specifies that a procedure or a type needs de-serialization support.</span></span>

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="138c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="138c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="138c0-107">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="138c0-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="138c0-108">指定適用于整個介面的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="138c0-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="138c0-109">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="138c0-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="138c0-110">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="138c0-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="138c0-111">*介面定義*</span><span class="sxs-lookup"><span data-stu-id="138c0-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="138c0-112">指定組成介面定義的 IDL 語句。</span><span class="sxs-lookup"><span data-stu-id="138c0-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="138c0-113">*op-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="138c0-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="138c0-114">指定適用于程式的其他操作屬性，例如 **\[** [**編碼**](encode.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="138c0-114">Specifies other operational attributes that apply to the procedure such as **\[**[**encode**](encode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="138c0-115">*進程名稱*</span><span class="sxs-lookup"><span data-stu-id="138c0-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="138c0-116">指定程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="138c0-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="138c0-117">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="138c0-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="138c0-118">指定其他屬性，例如 **\[** [**編碼**](encode.md) **\]** 和 **\[** [**配置**](allocate.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="138c0-118">Specifies other attributes such as **\[**[**encode**](encode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="138c0-119">*類型名稱*</span><span class="sxs-lookup"><span data-stu-id="138c0-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="138c0-120">指定 IDL 檔案中定義的類型。</span><span class="sxs-lookup"><span data-stu-id="138c0-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="138c0-121">備註</span><span class="sxs-lookup"><span data-stu-id="138c0-121">Remarks</span></span>

<span data-ttu-id="138c0-122">解碼屬性會導致 MIDL 編譯器產生程式碼，應用程式可以使用該程式碼從緩衝區取出序列化的資料。 **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="138c0-122">The **\[decode\]** attribute causes the MIDL compiler to generate code that an application can use to retrieve serialized data from a buffer.</span></span> <span data-ttu-id="138c0-123">**\[**[**編碼**](encode.md) **\]** 屬性提供序列化支援，產生將資料序列化為緩衝區的程式碼。</span><span class="sxs-lookup"><span data-stu-id="138c0-123">The **\[**[**encode**](encode.md)**\]** attribute provides serialization support, generating the code to serialize data into a buffer.</span></span>

<span data-ttu-id="138c0-124">使用 **\[** [](encode.md) **\]** ACF 中的 **\[ \]** 編碼和解碼屬性，為介面的 IDL 檔中定義的程式或類型產生序列化程式碼。</span><span class="sxs-lookup"><span data-stu-id="138c0-124">Use the **\[**[**encode**](encode.md)**\]** and **\[decode\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="138c0-125">當做介面屬性使用 **時， \[ \] 解碼** 會套用至 IDL 檔案中定義的所有類型和程式。</span><span class="sxs-lookup"><span data-stu-id="138c0-125">When used as an interface attribute, **\[decode\]** applies to all types and procedures defined in the IDL file.</span></span> <span data-ttu-id="138c0-126">當做型別屬性使用時， **\[ \] 解碼只適用于指定** 的型別。</span><span class="sxs-lookup"><span data-stu-id="138c0-126">When used as a type attribute, **\[decode\]** applies only to the specified type.</span></span> <span data-ttu-id="138c0-127">作為操作屬性使用時， **\[ \] 只會套用至** 該程式。</span><span class="sxs-lookup"><span data-stu-id="138c0-127">When used as an operational attribute, **\[decode\]** applies only to that procedure.</span></span>

<span data-ttu-id="138c0-128">如需使用此序列化支援的詳細資訊，請參閱 [序列化服務](/windows/desktop/Rpc/serialization-services)和 **\[** [**編碼**](encode.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="138c0-128">For more information about using this serialization support, see [Serialization Services](/windows/desktop/Rpc/serialization-services) and **\[**[**encode**](encode.md)**\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="138c0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="138c0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="138c0-130">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="138c0-130">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="138c0-131">**分配**</span><span class="sxs-lookup"><span data-stu-id="138c0-131">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="138c0-132">**編碼**</span><span class="sxs-lookup"><span data-stu-id="138c0-132">**encode**</span></span>](encode.md)
</dt> </dl>

 

 