---
title: small 屬性
description: Small 關鍵字會指定8位的整數。
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- small 屬性 MIDL
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372883"
---
# <a name="small-attribute"></a><span data-ttu-id="e3a85-104">small 屬性</span><span class="sxs-lookup"><span data-stu-id="e3a85-104">small attribute</span></span>

<span data-ttu-id="e3a85-105">**Small** 關鍵字會指定8位的整數。</span><span class="sxs-lookup"><span data-stu-id="e3a85-105">The **small** keyword designates an 8-bit integer number.</span></span>

``` syntax
small identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="e3a85-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3a85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a85-107">*識別碼-名稱*</span><span class="sxs-lookup"><span data-stu-id="e3a85-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a85-108">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3a85-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="e3a85-109">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="e3a85-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3a85-110">備註</span><span class="sxs-lookup"><span data-stu-id="e3a85-110">Remarks</span></span>

<span data-ttu-id="e3a85-111">**Small** 關鍵字的前面可以是關鍵字 [**帶正負**](signed.md)號或不 [**帶正負**](unsigned.md)號的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="e3a85-111">The **small** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="e3a85-112">[**Int**](int.md)關鍵字是選擇性的，可以省略。</span><span class="sxs-lookup"><span data-stu-id="e3a85-112">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="e3a85-113">對 MIDL 編譯器而言，預設會 **簽署** 一個小整數，而且與 **帶正負** 號的小整數同義。</span><span class="sxs-lookup"><span data-stu-id="e3a85-113">To the MIDL compiler, a small integer is **signed** by default and is synonymous with **signed small int**.</span></span>

<span data-ttu-id="e3a85-114">**小** 整數類型是 IDL 語言的其中一種基底類型。</span><span class="sxs-lookup"><span data-stu-id="e3a85-114">The **small** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="e3a85-115">**小** 整數類型可顯示為 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範和) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="e3a85-115">The **small** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="e3a85-116">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="e3a85-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="e3a85-117">您可以使用 MIDL 編譯器參數 [**/char**](-char.md)來修改 **small** 型別的正負號。</span><span class="sxs-lookup"><span data-stu-id="e3a85-117">The sign of the **small** type can be modified by the MIDL compiler switch [**/char**](-char.md).</span></span> <span data-ttu-id="e3a85-118">若要避免混淆，請使用 [**已簽署**](signed.md) 和 [**未簽署**](unsigned.md)的關鍵字來指定整數類型的正負號。</span><span class="sxs-lookup"><span data-stu-id="e3a85-118">To avoid confusion, specify the sign of the integer type with the keywords [**signed**](signed.md) and [**unsigned**](unsigned.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e3a85-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3a85-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a85-120">**/char**</span><span class="sxs-lookup"><span data-stu-id="e3a85-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="e3a85-121">**const**</span><span class="sxs-lookup"><span data-stu-id="e3a85-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e3a85-122"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="e3a85-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e3a85-123">**int**</span><span class="sxs-lookup"><span data-stu-id="e3a85-123">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="e3a85-124">**long**</span><span class="sxs-lookup"><span data-stu-id="e3a85-124">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="e3a85-125">**short**</span><span class="sxs-lookup"><span data-stu-id="e3a85-125">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="e3a85-126">**signed**</span><span class="sxs-lookup"><span data-stu-id="e3a85-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="e3a85-127">**符號**</span><span class="sxs-lookup"><span data-stu-id="e3a85-127">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="e3a85-128">**著**</span><span class="sxs-lookup"><span data-stu-id="e3a85-128">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




