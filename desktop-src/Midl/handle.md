---
title: 控制碼屬性
description: '\ Handle \ 屬性指定使用者定義或 \ 0034; 自訂 \ 0034;控制碼類型。'
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- 處理屬性 MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842288"
---
# <a name="handle-attribute"></a><span data-ttu-id="a7350-104">控制碼屬性</span><span class="sxs-lookup"><span data-stu-id="a7350-104">handle attribute</span></span>

<span data-ttu-id="a7350-105">\[ **Handle** \] 屬性指定使用者定義或「自訂」的控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="a7350-105">The \[**handle**\] attribute specifies a user-defined or "customized" handle type.</span></span>

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a><span data-ttu-id="a7350-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7350-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7350-107">*typename*</span><span class="sxs-lookup"><span data-stu-id="a7350-107">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="a7350-108">指定使用者定義的系結-控制碼類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7350-108">Specifies the name of the user-defined binding-handle type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7350-109">備註</span><span class="sxs-lookup"><span data-stu-id="a7350-109">Remarks</span></span>

<span data-ttu-id="a7350-110">使用者定義控制碼允許開發人員設計對應用程式有意義的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a7350-110">User-defined handles permit developers to design handles that are meaningful to the application.</span></span> <span data-ttu-id="a7350-111">使用者定義控制碼只能在類型宣告中定義，而不能定義在函式宣告子中。</span><span class="sxs-lookup"><span data-stu-id="a7350-111">A user-defined handle can only be defined in a type declaration, not in a function declarator.</span></span>

<span data-ttu-id="a7350-112">Handle 屬性所定義之類型的參數 \[  \] 會用來判斷呼叫的系結，並傳送至呼叫的程式。</span><span class="sxs-lookup"><span data-stu-id="a7350-112">A parameter of a type defined by the \[**handle**\] attribute is used to determine the binding for the call and is transmitted to the called procedure.</span></span>

<span data-ttu-id="a7350-113">使用者必須提供系結和解除系結常式，才能在基本與使用者定義的控制碼類型之間轉換。</span><span class="sxs-lookup"><span data-stu-id="a7350-113">The user must provide binding and unbinding routines to convert between primitive and user-defined handle types.</span></span> <span data-ttu-id="a7350-114">假設使用者定義了類型 *名稱* 類型的控制碼，則使用者必須提供常式 *typename* 系結 \_ 和 *typename* \_ **解除** 系結。</span><span class="sxs-lookup"><span data-stu-id="a7350-114">Given a user-defined handle of type *typename*, the user must supply the routines *typename*\_**bind** and *typename*\_**unbind**.</span></span> <span data-ttu-id="a7350-115">例如，如果使用者定義控制碼類型的名稱是 MYHANDLE，則常式會命名為 MYHANDLE \_ **BIND** 和 MYHANDLE \_ **解除** 系結。</span><span class="sxs-lookup"><span data-stu-id="a7350-115">For example, if the user-defined handle type is named MYHANDLE, the routines are named MYHANDLE\_**bind** and MYHANDLE\_**unbind**.</span></span>

<span data-ttu-id="a7350-116">如果成功， *typename* 系結 \_ 常式應該會傳回有效的基本系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a7350-116">If successful, the *typename*\_**bind** routine should return a valid primitive binding handle.</span></span> <span data-ttu-id="a7350-117">如果不成功，則常式應傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7350-117">If unsuccessful, the routine should return a **NULL**.</span></span> <span data-ttu-id="a7350-118">如果常式傳回 **Null**，則不會呼叫 *typename* \_ **解除** 系結常式。</span><span class="sxs-lookup"><span data-stu-id="a7350-118">If the routine returns **NULL**, the *typename*\_**unbind** routine will not be called.</span></span> <span data-ttu-id="a7350-119">如果系結常式傳回的系結控制碼與 **Null** 不同，則存根行為是未定義的。</span><span class="sxs-lookup"><span data-stu-id="a7350-119">If the binding routine returns an invalid binding handle different from **NULL**, the stub behavior is undefined.</span></span>

<span data-ttu-id="a7350-120">當遠端程式以使用者定義控制碼做為參數或隱含控制碼時，用戶端 stub 會在呼叫遠端程式之前呼叫系結常式。</span><span class="sxs-lookup"><span data-stu-id="a7350-120">When the remote procedure has a user-defined handle as a parameter or as an implicit handle, the client stubs call the binding routine before calling the remote procedure.</span></span> <span data-ttu-id="a7350-121">用戶端 stub 會在遠端呼叫之後呼叫解除系結常式。</span><span class="sxs-lookup"><span data-stu-id="a7350-121">The client stubs call the unbinding routine after the remote call.</span></span>

<span data-ttu-id="a7350-122">在 DCE IDL 中，具有 \[ **handle** \] 屬性的參數必須顯示為遠端過程引數清單中的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="a7350-122">In DCE IDL, a parameter with the \[**handle**\] attribute must appear as the first parameter in the remote procedure argument list.</span></span> <span data-ttu-id="a7350-123">後續的參數（包括其他 \[ **控制碼** \] 屬性）會被視為一般參數。</span><span class="sxs-lookup"><span data-stu-id="a7350-123">Subsequent parameters, including other \[**handle**\] attributes, are treated as ordinary parameters.</span></span> <span data-ttu-id="a7350-124">Microsoft 支援可延伸至 DCE IDL 的延伸模組，可讓使用者定義 \[ **控制碼** \] 參數出現在第一個參數以外的位置。</span><span class="sxs-lookup"><span data-stu-id="a7350-124">Microsoft supports an extension to DCE IDL that allows the user-defined \[**handle**\] parameter to appear in positions other than the first parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="a7350-125">範例</span><span class="sxs-lookup"><span data-stu-id="a7350-125">Examples</span></span>

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a><span data-ttu-id="a7350-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7350-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7350-127">系結和控制碼</span><span class="sxs-lookup"><span data-stu-id="a7350-127">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="a7350-128"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="a7350-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a7350-129">**隱含 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="a7350-129">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="a7350-130">**著**</span><span class="sxs-lookup"><span data-stu-id="a7350-130">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 