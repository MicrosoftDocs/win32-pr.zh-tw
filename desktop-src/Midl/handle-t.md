---
title: handle_t 屬性
description: 控制碼 \_ t 關鍵字會將物件宣告為基本型別控制碼 t 的基本控制碼類型 \_ 。 基本系結控制碼是可供應用程式用來代表系結的資料物件。
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t 屬性 MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314821"
---
# <a name="handle_t-attribute"></a><span data-ttu-id="1a417-105">處理 \_ t 屬性</span><span class="sxs-lookup"><span data-stu-id="1a417-105">handle\_t attribute</span></span>

<span data-ttu-id="1a417-106">**控制碼 \_ t** 關鍵字會將物件宣告為基本型 **別控制碼 \_ t** 的基本控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="1a417-106">The **handle\_t** keyword declares an object to be of the primitive handle type **handle\_t**.</span></span> <span data-ttu-id="1a417-107">基本系結控制碼是可供應用程式用來代表系結的資料物件。</span><span class="sxs-lookup"><span data-stu-id="1a417-107">A primitive binding handle is a data object that can be used by the application to represent the binding.</span></span>

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a><span data-ttu-id="1a417-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a417-108">Parameters</span></span>

<span data-ttu-id="1a417-109">這個屬性沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1a417-109">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a417-110">備註</span><span class="sxs-lookup"><span data-stu-id="1a417-110">Remarks</span></span>

<span data-ttu-id="1a417-111">**控制碼 \_ t** 類型是介面定義語言 (IDL) 其中一個預先定義的類型。</span><span class="sxs-lookup"><span data-stu-id="1a417-111">The **handle\_t** type is one of the predefined types of the interface definition language (IDL).</span></span> <span data-ttu-id="1a417-112">它可以在 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="1a417-112">It can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="1a417-113">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="1a417-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="1a417-114">在 Microsoft RPC 中，類型 **控制碼 \_ t** 的參數只能 **\[** [**在參數中**](in.md)發生 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="1a417-114">In Microsoft RPC, parameters of type **handle\_t** can occur only as **\[**[**in**](in.md)**\]** parameters.</span></span> <span data-ttu-id="1a417-115">基本控制碼不能具有 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1a417-115">Primitive handles cannot have the **\[**[**unique**](unique.md)**\]** or **\[**[**ptr**](ptr.md)**\]** attribute.</span></span>

<span data-ttu-id="1a417-116">不會在網路上傳輸) 的 **控制碼 \_ t** (基本控制碼參數類型的參數。</span><span class="sxs-lookup"><span data-stu-id="1a417-116">Parameters of type **handle\_t** (primitive handle parameters) are not transmitted on the network.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a417-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a417-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a417-118">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="1a417-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="1a417-119">系結和控制碼</span><span class="sxs-lookup"><span data-stu-id="1a417-119">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="1a417-120"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="1a417-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="1a417-121">**在**</span><span class="sxs-lookup"><span data-stu-id="1a417-121">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="1a417-122">**著**</span><span class="sxs-lookup"><span data-stu-id="1a417-122">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="1a417-123">**ptr**</span><span class="sxs-lookup"><span data-stu-id="1a417-123">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="1a417-124">**獨特**</span><span class="sxs-lookup"><span data-stu-id="1a417-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 