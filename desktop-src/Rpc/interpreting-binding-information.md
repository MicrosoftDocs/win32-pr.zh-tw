---
title: 解讀系結資訊
description: Microsoft RPC 可讓您的用戶端和伺服器程式存取及解讀系結控制碼中的資訊。
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- 遠端程序呼叫 RPC、工作、解讀系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462453"
---
# <a name="interpreting-binding-information"></a><span data-ttu-id="7ec22-104">解讀系結資訊</span><span class="sxs-lookup"><span data-stu-id="7ec22-104">Interpreting Binding Information</span></span>

<span data-ttu-id="7ec22-105">Microsoft RPC 可讓您的用戶端和伺服器程式存取及解讀系結控制碼中的資訊。</span><span class="sxs-lookup"><span data-stu-id="7ec22-105">Microsoft RPC enables your client and server programs access to and interpret the information in a binding handle.</span></span> <span data-ttu-id="7ec22-106">這並不表示您可以或嘗試直接存取系結控制碼的內容。</span><span class="sxs-lookup"><span data-stu-id="7ec22-106">This does not mean that you can or should try to access the contents of a binding handle directly.</span></span> <span data-ttu-id="7ec22-107">Microsoft RPC 提供的函式可設定和取出系結控制碼中的資訊。</span><span class="sxs-lookup"><span data-stu-id="7ec22-107">Microsoft RPC provides functions that set and retrieve the information in binding handles.</span></span>

<span data-ttu-id="7ec22-108">若要取得系結控制碼中的資訊，請將控制碼傳遞給 [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)。</span><span class="sxs-lookup"><span data-stu-id="7ec22-108">To get the information in a binding handle, pass the handle to [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="7ec22-109">它會以字串形式傳回系結資訊。</span><span class="sxs-lookup"><span data-stu-id="7ec22-109">It returns the binding information as a string.</span></span> <span data-ttu-id="7ec22-110">對於 **RpcBindingToStringBinding** 的每個呼叫，您都必須有對應的函數 [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree)呼叫。</span><span class="sxs-lookup"><span data-stu-id="7ec22-110">For every call to **RpcBindingToStringBinding**, you must have a corresponding call to the function [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span></span>

<span data-ttu-id="7ec22-111">您可以呼叫函式 [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) ，以剖析您從 [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)取得的字串。</span><span class="sxs-lookup"><span data-stu-id="7ec22-111">You can call the function [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to parse the string you obtain from [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="7ec22-112">此函式會配置字串以包含它所剖析的資訊。</span><span class="sxs-lookup"><span data-stu-id="7ec22-112">This function allocates strings to contain the information it parses.</span></span> <span data-ttu-id="7ec22-113">如果您不想要它剖析特定的系結資訊片段，請傳遞 **Null** 做為該參數的值。</span><span class="sxs-lookup"><span data-stu-id="7ec22-113">If you do not want it to parse a particular piece of binding information, pass a **NULL** as the value of that parameter.</span></span> <span data-ttu-id="7ec22-114">務必針對它所配置的每個字串呼叫 [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) 。</span><span class="sxs-lookup"><span data-stu-id="7ec22-114">Be sure to call [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) for each of the strings it allocates.</span></span>

<span data-ttu-id="7ec22-115">下列程式碼片段會說明應用程式如何呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="7ec22-115">The following code fragment illustrates how an application might call these functions.</span></span>


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



<span data-ttu-id="7ec22-116">上述範例程式碼會呼叫 [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) 和 [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) 函式，以在有效的系結控制碼中取得和剖析資訊。</span><span class="sxs-lookup"><span data-stu-id="7ec22-116">The preceding sample code calls the functions [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) and [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to get and parse the information in a valid binding handle.</span></span> <span data-ttu-id="7ec22-117">請注意， **Null** 值已做為第二個參數傳遞至 **RpcStringBindingParse**。</span><span class="sxs-lookup"><span data-stu-id="7ec22-117">Note that the value **NULL** was passed as the second parameter to **RpcStringBindingParse**.</span></span> <span data-ttu-id="7ec22-118">這會導致該函式略過剖析物件 UUID。</span><span class="sxs-lookup"><span data-stu-id="7ec22-118">This causes that function to skip parsing the object UUID.</span></span> <span data-ttu-id="7ec22-119">因為它不會剖析 UUID，所以 **RpcStringBindingParse** 不會為其配置字串。</span><span class="sxs-lookup"><span data-stu-id="7ec22-119">Since it does not parse the UUID, **RpcStringBindingParse** will not allocate a string for it.</span></span> <span data-ttu-id="7ec22-120">這項技術可讓您的應用程式只針對您想要剖析和分析的資訊配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="7ec22-120">This technique enables your application to only allocate memory for the information you are interested in parsing and analyzing.</span></span>

 

 




