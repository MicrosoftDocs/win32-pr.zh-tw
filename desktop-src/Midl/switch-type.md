---
title: switch_type 屬性
description: '\ Switch \_ 類型 \ 屬性會識別用來當做聯集判別的變數類型。 參數類型可以是整數、字元、布林值或列舉類型。'
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type 屬性 MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841339"
---
# <a name="switch_type-attribute"></a><span data-ttu-id="e5adc-105">切換 \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="e5adc-105">switch\_type attribute</span></span>

<span data-ttu-id="e5adc-106">**\[ Switch \_ type \]** 屬性會識別當做聯集判別使用的變數類型。</span><span class="sxs-lookup"><span data-stu-id="e5adc-106">The **\[switch\_type\]** attribute identifies the type of the variable used as the union discriminant.</span></span> <span data-ttu-id="e5adc-107">參數類型可以是整數、字元、布林值或列舉類型。</span><span class="sxs-lookup"><span data-stu-id="e5adc-107">The switch type can be an integer, character, Boolean, or enumeration type.</span></span>

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a><span data-ttu-id="e5adc-108">參數</span><span class="sxs-lookup"><span data-stu-id="e5adc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5adc-109">*參數類型規範*</span><span class="sxs-lookup"><span data-stu-id="e5adc-109">*switch-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e5adc-110">指定 [**int**](int.md)、 [**char**](char-idl.md)、 [**Boolean**](boolean.md)或 [**enum**](enum.md) 型別，或這類類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5adc-110">Specifies an [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md), or [**enum**](enum.md) type, or an identifier of such a type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5adc-111">備註</span><span class="sxs-lookup"><span data-stu-id="e5adc-111">Remarks</span></span>

<span data-ttu-id="e5adc-112">**\[ Switch \_ type \]** 屬性會識別變數型別，而參數 **\[** [**\_ 是**](switch-is.md)屬性（attribute）， **\]** 它會指定做為聯集判別的參數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5adc-112">While the **\[switch\_type\]** attribute identifies the variable type, the **\[**[**switch\_is**](switch-is.md)**\]** attribute specifies the name of the parameter that is the union discriminant.</span></span> <span data-ttu-id="e5adc-113">**\[ Switch \_ type \]** 屬性會套用至結構或等位的參數或成員。</span><span class="sxs-lookup"><span data-stu-id="e5adc-113">The **\[switch\_type\]** attribute applies to parameters or members of structures or unions.</span></span>

<span data-ttu-id="e5adc-114">Union 及其判別必須在相同的邏輯層級上指定。</span><span class="sxs-lookup"><span data-stu-id="e5adc-114">The union and its discriminant must be specified at the same logical level.</span></span> <span data-ttu-id="e5adc-115">當 union 是參數時，聯集判別必須是另一個參數。</span><span class="sxs-lookup"><span data-stu-id="e5adc-115">When the union is a parameter, the union discriminant must be another parameter.</span></span> <span data-ttu-id="e5adc-116">當聯集是結構的欄位時，判別必須是結構與聯集欄位相同層級的另一個欄位。</span><span class="sxs-lookup"><span data-stu-id="e5adc-116">When the union is a field of a structure, the discriminant must be another field of the structure at the same level as the union field.</span></span>

## <a name="examples"></a><span data-ttu-id="e5adc-117">範例</span><span class="sxs-lookup"><span data-stu-id="e5adc-117">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="e5adc-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5adc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5adc-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e5adc-119">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="e5adc-120">**字元**</span><span class="sxs-lookup"><span data-stu-id="e5adc-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="e5adc-121">封裝聯集</span><span class="sxs-lookup"><span data-stu-id="e5adc-121">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="e5adc-122">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="e5adc-122">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e5adc-123"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="e5adc-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e5adc-124">**int**</span><span class="sxs-lookup"><span data-stu-id="e5adc-124">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="e5adc-125">Nonencapsulated 聯集</span><span class="sxs-lookup"><span data-stu-id="e5adc-125">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="e5adc-126">**切換 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="e5adc-126">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="e5adc-127">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="e5adc-127">**union**</span></span>](union.md)
</dt> </dl>

 

 




