---
title: short 屬性
description: Short 關鍵字會指定16位整數。
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- short 屬性 MIDL
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312741"
---
# <a name="short-attribute"></a><span data-ttu-id="e8917-104">short 屬性</span><span class="sxs-lookup"><span data-stu-id="e8917-104">short attribute</span></span>

<span data-ttu-id="e8917-105">**Short** 關鍵字會指定16位整數。</span><span class="sxs-lookup"><span data-stu-id="e8917-105">The **short** keyword designates a 16-bit integer.</span></span>

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="e8917-106">參數</span><span class="sxs-lookup"><span data-stu-id="e8917-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8917-107">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="e8917-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e8917-108">指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="e8917-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e8917-109">在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。</span><span class="sxs-lookup"><span data-stu-id="e8917-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="e8917-110">未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。</span><span class="sxs-lookup"><span data-stu-id="e8917-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8917-111">備註</span><span class="sxs-lookup"><span data-stu-id="e8917-111">Remarks</span></span>

<span data-ttu-id="e8917-112">**Short** 關鍵字的前面可以是關鍵字 [**帶正負**](signed.md)號或不 [**帶正負**](unsigned.md)號的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="e8917-112">The **short** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="e8917-113">[**Int**](int.md)關鍵字是選擇性的，可以省略。</span><span class="sxs-lookup"><span data-stu-id="e8917-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="e8917-114">對 MIDL 編譯器而言，預設會簽署簡短的整數，並以帶正負號的 **short** 整數為同義。</span><span class="sxs-lookup"><span data-stu-id="e8917-114">To the MIDL compiler, a short integer is signed by default and is synonymous with **signed short int**.</span></span>

<span data-ttu-id="e8917-115">**Short** 整數類型是 IDL 語言的其中一種基底類型。</span><span class="sxs-lookup"><span data-stu-id="e8917-115">The **short** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="e8917-116">**Short** 整數型別可以在 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="e8917-116">The **short** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="e8917-117">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="e8917-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e8917-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8917-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8917-119">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="e8917-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e8917-120"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="e8917-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e8917-121">**int**</span><span class="sxs-lookup"><span data-stu-id="e8917-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="e8917-122">**long**</span><span class="sxs-lookup"><span data-stu-id="e8917-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="e8917-123">**signed**</span><span class="sxs-lookup"><span data-stu-id="e8917-123">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="e8917-124">**小**</span><span class="sxs-lookup"><span data-stu-id="e8917-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="e8917-125">**符號**</span><span class="sxs-lookup"><span data-stu-id="e8917-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




