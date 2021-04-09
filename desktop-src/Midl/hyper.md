---
title: 超屬性
description: 關鍵字 [超] 表示可以宣告為帶正負號或不帶正負號的64位整數。
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- 超屬性 MIDL
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678247"
---
# <a name="hyper-attribute"></a><span data-ttu-id="ad8c5-104">超屬性</span><span class="sxs-lookup"><span data-stu-id="ad8c5-104">hyper attribute</span></span>

<span data-ttu-id="ad8c5-105">關鍵字 [ **超** ] 表示可以宣告為帶正負號或不帶正負號的64位整數。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-105">The keyword **hyper** indicates a 64-bit integer that can be declared as either signed or unsigned.</span></span>

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="ad8c5-106">參數</span><span class="sxs-lookup"><span data-stu-id="ad8c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad8c5-107">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="ad8c5-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8c5-108">指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="ad8c5-109">在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="ad8c5-110">未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad8c5-111">備註</span><span class="sxs-lookup"><span data-stu-id="ad8c5-111">Remarks</span></span>

<span data-ttu-id="ad8c5-112">**超** 類型是介面定義語言 (IDL) 的其中一種基底類型。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-112">The **hyper** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="ad8c5-113">**超** 型別可以在 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-113">The **hyper** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="ad8c5-114">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="ad8c5-115">若是16位平臺，MIDL 編譯器會以 **midl \_ uhyper** 取代不帶正負號的超整數。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-115">For 16-bit platforms, the MIDL compiler replaces unsigned hyper integers with **MIDL\_uhyper**.</span></span> <span data-ttu-id="ad8c5-116">這允許在不直接支援64位整數的平臺上，定義不帶正負號之超整數的介面。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-116">This allows interfaces with unsigned hyper integers to be defined on platforms that do not directly support 64-bit integers.</span></span> <span data-ttu-id="ad8c5-117">**MIDL \_ uhyper** 是在 RPC 標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="ad8c5-117">**MIDL\_uhyper** is defined in the RPC header files.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="ad8c5-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad8c5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad8c5-119">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="ad8c5-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="ad8c5-120">**const**</span><span class="sxs-lookup"><span data-stu-id="ad8c5-120">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="ad8c5-121"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="ad8c5-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ad8c5-122">**著**</span><span class="sxs-lookup"><span data-stu-id="ad8c5-122">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




