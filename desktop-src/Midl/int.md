---
title: int 屬性
description: 關鍵字 int 指定32位平臺上的32位帶正負號的整數。 在16位平臺上，關鍵字 int 是選擇性的關鍵字，可伴隨關鍵字 small、short 和 long。
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- int 屬性 MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678243"
---
# <a name="int-attribute"></a><span data-ttu-id="2e5b6-105">int 屬性</span><span class="sxs-lookup"><span data-stu-id="2e5b6-105">int attribute</span></span>

<span data-ttu-id="2e5b6-106">關鍵字 **int** 指定32位平臺上的32位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-106">The keyword **int** specifies a 32-bit signed integer on 32-bit platforms.</span></span> <span data-ttu-id="2e5b6-107">在16位平臺上，關鍵字 **int** 是選擇性的關鍵字，可伴隨關鍵字 [**small**](small.md)、 [**short**](short.md)和 [**long**](long.md)。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-107">On 16-bit platforms, the keyword **int** is an optional keyword that can accompany the keywords [**small**](small.md), [**short**](short.md), and [**long**](long.md).</span></span>

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="2e5b6-108">參數</span><span class="sxs-lookup"><span data-stu-id="2e5b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e5b6-109">*整數修飾詞*</span><span class="sxs-lookup"><span data-stu-id="2e5b6-109">*integer-modifier*</span></span> 
</dt> <dd>

<span data-ttu-id="2e5b6-110">指定關鍵字 [**small**](small.md)、 [**short**](short.md)、 [**long**](long.md)、[**超**](hyper.md)、 [**\_ \_ int3264**](--int3264.md)或 [**\_ \_ int64**](--int64.md)，以選取整數資料的大小。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-110">Specifies the keyword [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_\_int3264**](--int3264.md), or [**\_\_int64**](--int64.md),which selects the size of the integer data.</span></span> <span data-ttu-id="2e5b6-111">在16位平臺上，大小限定詞必須存在。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-111">On 16-bit platforms, the size qualifier must be present.</span></span>

</dd> <dt>

<span data-ttu-id="2e5b6-112">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="2e5b6-112">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2e5b6-113">指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-113">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="2e5b6-114">在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-114">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="2e5b6-115">未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-115">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e5b6-116">備註</span><span class="sxs-lookup"><span data-stu-id="2e5b6-116">Remarks</span></span>

<span data-ttu-id="2e5b6-117">整數類型是介面定義語言 (IDL) 的基底類型。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-117">Integer types are among the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="2e5b6-118">它們可以在 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-118">They can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="2e5b6-119">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-119">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="2e5b6-120">如果未提供整數符號規格，則整數類型會預設為 [**已簽署**](signed.md)。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-120">If no integer sign specification is provided, the integer type defaults to [**signed**](signed.md).</span></span>

<span data-ttu-id="2e5b6-121">DCE IDL 編譯器不允許關鍵字 [**簽署**](signed.md) 來指定整數類型的正負號。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-121">DCE IDL compilers do not allow the keyword [**signed**](signed.md) to specify the sign of integer types.</span></span> <span data-ttu-id="2e5b6-122">因此，當您使用 MIDL 編譯器 [**/osf**](-osf.md) 參數時，就無法使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-122">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="2e5b6-123">如果可以避免，Microsoft 不建議使用 \_ \_ int3264 進行遠端處理。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-123">Microsoft does not recommend the use of \_\_int3264 for remoting if it can be avoided.</span></span> <span data-ttu-id="2e5b6-124">如需有關其使用方式和限制的詳細資訊，請參閱 [**\_ \_ int3264**](--int3264.md)的主題。</span><span class="sxs-lookup"><span data-stu-id="2e5b6-124">Please see the topic on [**\_\_int3264**](--int3264.md) for more information regarding it's use and limitations.</span></span>

## <a name="examples"></a><span data-ttu-id="2e5b6-125">範例</span><span class="sxs-lookup"><span data-stu-id="2e5b6-125">Examples</span></span>

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a><span data-ttu-id="2e5b6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e5b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5b6-127">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="2e5b6-127">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-128">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-128">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-129">**超**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-129">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-130"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="2e5b6-130">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-131">**long**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-131">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-133">**short**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-133">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-134">**signed**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-134">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-135">**小**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-135">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-136">**結構**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-136">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-137">**著**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-137">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="2e5b6-138">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="2e5b6-138">**union**</span></span>](union.md)
</dt> </dl>

 

 




