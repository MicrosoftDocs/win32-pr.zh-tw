---
title: enum 屬性
description: 關鍵字列舉可識別列舉型別。
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- enum 屬性 MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312219"
---
# <a name="enum-attribute"></a><span data-ttu-id="156eb-104">enum 屬性</span><span class="sxs-lookup"><span data-stu-id="156eb-104">enum attribute</span></span>

<span data-ttu-id="156eb-105">關鍵字 **列舉** 可識別列舉型別。</span><span class="sxs-lookup"><span data-stu-id="156eb-105">The keyword **enum** identifies an enumerated type.</span></span>

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a><span data-ttu-id="156eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="156eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="156eb-107">*標籤*</span><span class="sxs-lookup"><span data-stu-id="156eb-107">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="156eb-108">指定列舉類型的選擇性標記。</span><span class="sxs-lookup"><span data-stu-id="156eb-108">Specifies an optional tag for the enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="156eb-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="156eb-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="156eb-110">指定特定列舉。</span><span class="sxs-lookup"><span data-stu-id="156eb-110">Specifies the particular enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="156eb-111">*整數值*</span><span class="sxs-lookup"><span data-stu-id="156eb-111">*integer-value*</span></span> 
</dt> <dd>

<span data-ttu-id="156eb-112">指定常數整數值。</span><span class="sxs-lookup"><span data-stu-id="156eb-112">Specifies a constant integer value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="156eb-113">備註</span><span class="sxs-lookup"><span data-stu-id="156eb-113">Remarks</span></span>

<span data-ttu-id="156eb-114">**列舉** 型別可以在 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別或) 的參數類型指定名稱。</span><span class="sxs-lookup"><span data-stu-id="156eb-114">**enum** types can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (either as the function-return-type or as a parameter-type specifier).</span></span> <span data-ttu-id="156eb-115">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="156eb-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="156eb-116">在 MIDL 編譯器的預設模式中，您可以將整數值指派給枚舉器。</span><span class="sxs-lookup"><span data-stu-id="156eb-116">In the MIDL compiler's default mode, you can assign integer values to enumerators.</span></span> <span data-ttu-id="156eb-117"> (當您使用 [**/osf**](-osf.md) 參數進行編譯時，無法使用此功能。 ) 與 C 語言列舉值相同，列舉值名稱必須是唯一的，但是列舉值不需要。</span><span class="sxs-lookup"><span data-stu-id="156eb-117">(This feature is not available when you compile with the [**/osf**](-osf.md) switch.) As with C-language enumerators, enumerator names must be unique, but the enumerator values need not be.</span></span>

<span data-ttu-id="156eb-118">未提供指派運算子時，識別碼會從左至右對應至連續的整數，從零開始。</span><span class="sxs-lookup"><span data-stu-id="156eb-118">When assignment operators are not provided, identifiers are mapped to consecutive integers from left to right, starting with zero.</span></span> <span data-ttu-id="156eb-119">當提供指派運算子時，指派的值會從最近指派的值開始。</span><span class="sxs-lookup"><span data-stu-id="156eb-119">When assignment operators are provided, assigned values start from the most recently assigned value.</span></span>

<span data-ttu-id="156eb-120">識別碼的最大數目是65535。</span><span class="sxs-lookup"><span data-stu-id="156eb-120">The maximum number of identifiers is 65,535.</span></span>

<span data-ttu-id="156eb-121">**列舉** 類型的物件是 [**int**](int.md)類型，而其大小與系統相依。</span><span class="sxs-lookup"><span data-stu-id="156eb-121">Objects of type **enum** are [**int**](int.md) types, and their size is system-dependent.</span></span> <span data-ttu-id="156eb-122">根據預設，在透過網路 [**傳輸時，**](short.md) **列舉** 類型的物件會被視為不 [**帶正負**](unsigned.md)號的16位物件。</span><span class="sxs-lookup"><span data-stu-id="156eb-122">By default, objects of **enum** types are treated as 16-bit objects of type [**unsigned**](unsigned.md) [**short**](short.md) when transmitted over a network.</span></span> <span data-ttu-id="156eb-123">範圍 0-32767 以外的值會導致執行時間例外狀況 RPC \_ X \_ 列舉 \_ 值 \_ 超出 \_ \_ 範圍。</span><span class="sxs-lookup"><span data-stu-id="156eb-123">Values outside the range 0 - 32,767 cause the run-time exception RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="156eb-124">若要將物件傳輸為32位實體，請將 **\[** [**v1 \_ 列舉**](v1-enum.md) **\]** 屬性套用至 **列舉** typedef。</span><span class="sxs-lookup"><span data-stu-id="156eb-124">To transmit objects as 32-bit entities, apply the **\[**[**v1\_enum**](v1-enum.md)**\]** attribute to the **enum** typedef.</span></span>

## <a name="examples"></a><span data-ttu-id="156eb-125">範例</span><span class="sxs-lookup"><span data-stu-id="156eb-125">Examples</span></span>

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a><span data-ttu-id="156eb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="156eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="156eb-127"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="156eb-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="156eb-128">**int**</span><span class="sxs-lookup"><span data-stu-id="156eb-128">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="156eb-129">**short**</span><span class="sxs-lookup"><span data-stu-id="156eb-129">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="156eb-130">**著**</span><span class="sxs-lookup"><span data-stu-id="156eb-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="156eb-131">**符號**</span><span class="sxs-lookup"><span data-stu-id="156eb-131">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="156eb-132">**v1 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="156eb-132">**v1\_enum**</span></span>](v1-enum.md)
</dt> </dl>

 

 




