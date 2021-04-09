---
title: long 屬性
description: Long 關鍵字會指定32位的整數。
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- long 屬性 MIDL
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932663"
---
# <a name="long-attribute"></a><span data-ttu-id="36939-104">long 屬性</span><span class="sxs-lookup"><span data-stu-id="36939-104">long attribute</span></span>

<span data-ttu-id="36939-105">**Long** 關鍵字會指定32位的整數。</span><span class="sxs-lookup"><span data-stu-id="36939-105">The **long** keyword designates a 32-bit integer.</span></span>

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="36939-106">參數</span><span class="sxs-lookup"><span data-stu-id="36939-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36939-107">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="36939-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="36939-108">指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="36939-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="36939-109">在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。</span><span class="sxs-lookup"><span data-stu-id="36939-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="36939-110">未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。</span><span class="sxs-lookup"><span data-stu-id="36939-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36939-111">備註</span><span class="sxs-lookup"><span data-stu-id="36939-111">Remarks</span></span>

<span data-ttu-id="36939-112">**Long** 關鍵字的前面可以是關鍵字 [**帶正負**](signed.md)號或不 [**帶正負**](unsigned.md)號的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="36939-112">The **long** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="36939-113">[**Int**](int.md)關鍵字是選擇性的，可以省略。</span><span class="sxs-lookup"><span data-stu-id="36939-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="36939-114">若為 MIDL 編譯器，則預設會簽署長整數，而且與帶正負號的 **long int** 同義。在32位平臺上， **long** 與 **int** 同義。</span><span class="sxs-lookup"><span data-stu-id="36939-114">To the MIDL compiler, a long integer is signed by default and is synonymous with **signed long int**. On 32-bit platforms, **long** is synonymous with **int**.</span></span>

<span data-ttu-id="36939-115">**長** 整數類型是 IDL 語言的其中一種基底類型。</span><span class="sxs-lookup"><span data-stu-id="36939-115">The **long** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="36939-116">**長** 整數類型可顯示為 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="36939-116">The **long** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="36939-117">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="36939-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="36939-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36939-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36939-119">**const**</span><span class="sxs-lookup"><span data-stu-id="36939-119">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="36939-120">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="36939-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="36939-121">**超**</span><span class="sxs-lookup"><span data-stu-id="36939-121">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="36939-122">**int**</span><span class="sxs-lookup"><span data-stu-id="36939-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="36939-123">**short**</span><span class="sxs-lookup"><span data-stu-id="36939-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="36939-124">**signed**</span><span class="sxs-lookup"><span data-stu-id="36939-124">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="36939-125">**小**</span><span class="sxs-lookup"><span data-stu-id="36939-125">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="36939-126">**著**</span><span class="sxs-lookup"><span data-stu-id="36939-126">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="36939-127">**符號**</span><span class="sxs-lookup"><span data-stu-id="36939-127">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




