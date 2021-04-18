---
title: 未簽署的屬性
description: 不帶正負號的關鍵字表示整數變數中最重要的位代表資料位，而不是帶正負號的位。
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- 不帶正負號的屬性 MIDL
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106964996"
---
# <a name="unsigned-attribute"></a><span data-ttu-id="7fc2e-104">未簽署的屬性</span><span class="sxs-lookup"><span data-stu-id="7fc2e-104">unsigned attribute</span></span>

<span data-ttu-id="7fc2e-105">不 **帶正負** 號的關鍵字表示整數變數中最重要的位代表資料位，而不是帶正負號的位。</span><span class="sxs-lookup"><span data-stu-id="7fc2e-105">The **unsigned** keyword indicates that the most significant bit of an integer variable represents a data bit rather than a signed bit.</span></span>

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="7fc2e-106">參數</span><span class="sxs-lookup"><span data-stu-id="7fc2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fc2e-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="7fc2e-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc2e-108">可以是 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**long**](long.md)、 [**int**](int.md)、 [**short**](short.md)和 [**small**](small.md)的任何一個。</span><span class="sxs-lookup"><span data-stu-id="7fc2e-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fc2e-109">*識別碼-名稱*</span><span class="sxs-lookup"><span data-stu-id="7fc2e-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc2e-110">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fc2e-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="7fc2e-111">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="7fc2e-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fc2e-112">備註</span><span class="sxs-lookup"><span data-stu-id="7fc2e-112">Remarks</span></span>

<span data-ttu-id="7fc2e-113">這個關鍵字是選擇性的，可以搭配任何字元和整數類型 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**long**](long.md)、 [**short**](short.md)和 [**small**](small.md)使用。</span><span class="sxs-lookup"><span data-stu-id="7fc2e-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="7fc2e-114">您可以選擇性地在類型限定詞之後包含關鍵字 [**int**](int.md) ， **long**、 **short** 和 **small**。</span><span class="sxs-lookup"><span data-stu-id="7fc2e-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="7fc2e-115">當您使用 MIDL 編譯器參數 [**/char**](-char.md)時，會在產生的標頭檔中，以 [**帶正負**](signed.md)**號或不帶正負號** 的關鍵字來顯示出現在 IDL 檔案中的字元和整數類型。</span><span class="sxs-lookup"><span data-stu-id="7fc2e-115">When you use the MIDL compiler switch [**/char**](-char.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the [**signed**](signed.md) or **unsigned** keyword in the generated header file.</span></span> <span data-ttu-id="7fc2e-116">為了避免混淆，請指定整數和字元類型的正負號。</span><span class="sxs-lookup"><span data-stu-id="7fc2e-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fc2e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fc2e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc2e-118">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="7fc2e-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="7fc2e-119">**字元**</span><span class="sxs-lookup"><span data-stu-id="7fc2e-119">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="7fc2e-120">**/char**</span><span class="sxs-lookup"><span data-stu-id="7fc2e-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="7fc2e-121"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="7fc2e-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7fc2e-122">**int**</span><span class="sxs-lookup"><span data-stu-id="7fc2e-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="7fc2e-123">**long**</span><span class="sxs-lookup"><span data-stu-id="7fc2e-123">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="7fc2e-124">**short**</span><span class="sxs-lookup"><span data-stu-id="7fc2e-124">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="7fc2e-125">**signed**</span><span class="sxs-lookup"><span data-stu-id="7fc2e-125">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="7fc2e-126">**小**</span><span class="sxs-lookup"><span data-stu-id="7fc2e-126">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="7fc2e-127">**wchar \_ t**</span><span class="sxs-lookup"><span data-stu-id="7fc2e-127">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




