---
title: 已簽署屬性
description: 帶正負號的關鍵字表示整數變數中最重要的位代表正負號位，而不是資料位。
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- 簽署的屬性 MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103840968"
---
# <a name="signed-attribute"></a><span data-ttu-id="b8b83-104">已簽署屬性</span><span class="sxs-lookup"><span data-stu-id="b8b83-104">signed attribute</span></span>

<span data-ttu-id="b8b83-105">**帶正負** 號的關鍵字表示整數變數中最重要的位代表正負號位，而不是資料位。</span><span class="sxs-lookup"><span data-stu-id="b8b83-105">The **signed** keyword indicates the most significant bit of an integer variable represents a sign bit rather than a data bit.</span></span>

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="b8b83-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8b83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b83-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="b8b83-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b83-108">可以是 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**long**](long.md)、 [**short**](short.md)和 [**small**](small.md)的任何一個。</span><span class="sxs-lookup"><span data-stu-id="b8b83-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b83-109">*識別碼-名稱*</span><span class="sxs-lookup"><span data-stu-id="b8b83-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b83-110">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8b83-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="b8b83-111">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="b8b83-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8b83-112">備註</span><span class="sxs-lookup"><span data-stu-id="b8b83-112">Remarks</span></span>

<span data-ttu-id="b8b83-113">這個關鍵字是選擇性的，可以搭配任何字元和整數類型 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**long**](long.md)、 [**short**](short.md)和 [**small**](small.md)使用。</span><span class="sxs-lookup"><span data-stu-id="b8b83-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="b8b83-114">您可以選擇性地在類型限定詞之後包含關鍵字 [**int**](int.md) ， **long**、 **short** 和 **small**。</span><span class="sxs-lookup"><span data-stu-id="b8b83-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="b8b83-115">當您使用 MIDL 編譯器參數 [**char**](char-idl.md)時，在產生的標頭檔中，會以 **帶正負**[**號或不帶正負號**](unsigned.md)的關鍵字來顯示出現在 IDL 檔案中的字元和整數類型（不含明確的正負號關鍵字）。</span><span class="sxs-lookup"><span data-stu-id="b8b83-115">When you use the MIDL compiler switch [**char**](char-idl.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the **signed** or [**unsigned**](unsigned.md) keywords in the generated header file.</span></span> <span data-ttu-id="b8b83-116">為了避免混淆，請指定整數和字元類型的正負號。</span><span class="sxs-lookup"><span data-stu-id="b8b83-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8b83-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8b83-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b83-118">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="b8b83-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="b8b83-119">**/char**</span><span class="sxs-lookup"><span data-stu-id="b8b83-119">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="b8b83-120"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="b8b83-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b8b83-121">**int**</span><span class="sxs-lookup"><span data-stu-id="b8b83-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="b8b83-122">**long**</span><span class="sxs-lookup"><span data-stu-id="b8b83-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="b8b83-123">**short**</span><span class="sxs-lookup"><span data-stu-id="b8b83-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="b8b83-124">**小**</span><span class="sxs-lookup"><span data-stu-id="b8b83-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="b8b83-125">**符號**</span><span class="sxs-lookup"><span data-stu-id="b8b83-125">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="b8b83-126">**wchar \_ t**</span><span class="sxs-lookup"><span data-stu-id="b8b83-126">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




