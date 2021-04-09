---
title: 基本和自訂系結控制碼
description: 以控制碼 t 或 RPC 系結控制碼類型宣告的所有控制碼 \_ \_ \_ 都是基本的系結控制碼。
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023977"
---
# <a name="primitive-and-custom-binding-handles"></a><span data-ttu-id="99ce4-103">基本和自訂系結控制碼</span><span class="sxs-lookup"><span data-stu-id="99ce4-103">Primitive and Custom Binding Handles</span></span>

<span data-ttu-id="99ce4-104">以 [控制碼 \_ t](/windows/desktop/Midl/handle-t) 或 RPC 系結 [**\_ \_ 控制碼**](rpc-binding-handle.md) 類型宣告的所有控制碼都是基本的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="99ce4-104">All handles declared with the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types are primitive binding handles.</span></span> <span data-ttu-id="99ce4-105">您可以擴充 [控制碼 \_ t](/windows/desktop/Midl/handle-t) 或 [**RPC 系結 \_ \_ 控制碼**](rpc-binding-handle.md) 類型，以包含更多或不同于基本控制碼類型所包含的資訊。</span><span class="sxs-lookup"><span data-stu-id="99ce4-105">You can extend the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types to include more or different information than the primitive handle type contains.</span></span> <span data-ttu-id="99ce4-106">當您這樣做時，您會建立自訂系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="99ce4-106">When you do, you create a custom binding handle.</span></span>

<span data-ttu-id="99ce4-107">若要為您的分散式應用程式建立自訂系結控制碼，您必須建立自己的資料類型，並在 IDL 檔案的 \[ 類型定義上指定[控制碼](/windows/desktop/Midl/handle) \] 屬性。</span><span class="sxs-lookup"><span data-stu-id="99ce4-107">To make a custom binding handle for your distributed application, you will need to create your own data type and specify the \[ [handle](/windows/desktop/Midl/handle)\] attribute on a type definition in your IDL file.</span></span> <span data-ttu-id="99ce4-108">最後，存根檔案會將自訂系結控制碼對應至基本控制碼。</span><span class="sxs-lookup"><span data-stu-id="99ce4-108">Ultimately, the stub files map custom binding handles to primitive handles.</span></span>

<span data-ttu-id="99ce4-109">如果您建立自己的系結控制碼類型，您也必須提供系結和解除系結程式，用戶端 stub 會使用這些常式將自訂控制碼對應至基本控制碼。</span><span class="sxs-lookup"><span data-stu-id="99ce4-109">If you do create your own binding handle type, you must also supply bind and unbind routines that the client stub uses to map a custom handle to a primitive handle.</span></span> <span data-ttu-id="99ce4-110">Stub 會在每個遠端程序呼叫的開頭和結尾呼叫您的系結和解除系結常式。</span><span class="sxs-lookup"><span data-stu-id="99ce4-110">The stub calls your bind and unbind routines at the beginning and end of each remote procedure call.</span></span> <span data-ttu-id="99ce4-111">系結和解除系結常式必須符合下列函式原型。</span><span class="sxs-lookup"><span data-stu-id="99ce4-111">The bind and unbind routines must conform to the following function prototypes.</span></span>



| <span data-ttu-id="99ce4-112">函式原型</span><span class="sxs-lookup"><span data-stu-id="99ce4-112">Function prototype</span></span>                     | <span data-ttu-id="99ce4-113">Description</span><span class="sxs-lookup"><span data-stu-id="99ce4-113">Description</span></span>       |
|----------------------------------------|-------------------|
| <span data-ttu-id="99ce4-114">處理 \_ t 類型系結 \_ (*類型*) </span><span class="sxs-lookup"><span data-stu-id="99ce4-114">handle\_t type\_bind(*type*)</span></span>           | <span data-ttu-id="99ce4-115">系結常式</span><span class="sxs-lookup"><span data-stu-id="99ce4-115">Binding routine</span></span>   |
| <span data-ttu-id="99ce4-116">void 類型 \_ 解除系結 (*類型*， *處理 \_ t*) </span><span class="sxs-lookup"><span data-stu-id="99ce4-116">void type\_unbind(*type*, *handle\_t*)</span></span> | <span data-ttu-id="99ce4-117">解除系結常式</span><span class="sxs-lookup"><span data-stu-id="99ce4-117">Unbinding routine</span></span> |



 

<span data-ttu-id="99ce4-118">下列範例顯示如何在 IDL 檔案中定義自訂系結控制碼：</span><span class="sxs-lookup"><span data-stu-id="99ce4-118">The following example shows how a custom binding handle can be defined in the IDL file:</span></span>

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

<span data-ttu-id="99ce4-119">如果系結常式遇到錯誤，則應該使用 [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) 函數引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="99ce4-119">If the bind routine encounters an error, it should raise an exception using the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) function.</span></span> <span data-ttu-id="99ce4-120">然後，用戶端 stub 將會清除，讓例外狀況篩選至用戶端上遠端程序呼叫周圍的例外狀況區塊。</span><span class="sxs-lookup"><span data-stu-id="99ce4-120">The client stub will then clean up, and let the exception filter through to the exception block surrounding the remote procedure call on the client side.</span></span> <span data-ttu-id="99ce4-121">如果系結常式只會傳回 **Null**，用戶端程式代碼會取得錯誤 RPC S 不正確系結 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="99ce4-121">If the bind routine simply returns **NULL**, the client code gets error RPC\_S\_INVALID\_BINDING.</span></span> <span data-ttu-id="99ce4-122">雖然在某些情況下這可能是可接受的，但在其他情況下 (例如記憶體不足) 也不會有任何回應。</span><span class="sxs-lookup"><span data-stu-id="99ce4-122">While this might be acceptable in certain situations, other situations (such as being out of memory) do not respond well.</span></span> <span data-ttu-id="99ce4-123">解除系結常式應設計為不會失敗。</span><span class="sxs-lookup"><span data-stu-id="99ce4-123">The unbind routine should be designed so that it does not fail.</span></span> <span data-ttu-id="99ce4-124">解除系結常式不應引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="99ce4-124">The unbind routine should not raise exceptions.</span></span>

<span data-ttu-id="99ce4-125">程式設計師定義的系結和解除系結常式會出現在用戶端應用程式中。</span><span class="sxs-lookup"><span data-stu-id="99ce4-125">The programmer-defined bind and unbind routines appear in the client application.</span></span> <span data-ttu-id="99ce4-126">在下列範例中，bind 常式會呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) ，以將字串系結資訊轉換成系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="99ce4-126">In the following example, the bind routine calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to convert the string-binding information to a binding handle.</span></span> <span data-ttu-id="99ce4-127">解除系結常式會呼叫 [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) ，以釋放系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="99ce4-127">The unbind routine calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to free the binding handle.</span></span>

<span data-ttu-id="99ce4-128">程式設計師定義的系結控制碼名稱（資料 \_ 控制碼 \_ 類型）會顯示為函式名稱的一部分。</span><span class="sxs-lookup"><span data-stu-id="99ce4-128">The name of the programmer-defined binding handle, DATA\_HANDLE\_TYPE, appears as part of the name of the functions.</span></span> <span data-ttu-id="99ce4-129">它也會當做函數參數中的參數類型使用。</span><span class="sxs-lookup"><span data-stu-id="99ce4-129">It is also used as the parameter type in the function parameters.</span></span>

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

<span data-ttu-id="99ce4-130">隱含和明確的系結控制碼可以是基本或自訂控制碼。</span><span class="sxs-lookup"><span data-stu-id="99ce4-130">Both implicit and explicit binding handles can either be primitive or custom handles.</span></span> <span data-ttu-id="99ce4-131">也就是說，控制碼可以是：</span><span class="sxs-lookup"><span data-stu-id="99ce4-131">That is, a handle may be:</span></span>

-   <span data-ttu-id="99ce4-132">基本和隱含</span><span class="sxs-lookup"><span data-stu-id="99ce4-132">Primitive and implicit</span></span>
-   <span data-ttu-id="99ce4-133">自訂和隱含</span><span class="sxs-lookup"><span data-stu-id="99ce4-133">Custom and implicit</span></span>
-   <span data-ttu-id="99ce4-134">基本和明確</span><span class="sxs-lookup"><span data-stu-id="99ce4-134">Primitive and explicit</span></span>
-   <span data-ttu-id="99ce4-135">自訂和明確</span><span class="sxs-lookup"><span data-stu-id="99ce4-135">Custom and explicit</span></span>

 

 