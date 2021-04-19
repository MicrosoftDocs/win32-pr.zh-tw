---
title: /use_epv 參數
description: /Use \_ epv 參數會指示 MIDL 編譯器產生伺服器 stub 程式碼，該程式碼會透過進入點向量 (epv) ，而不是透過靜態呼叫來呼叫伺服器應用程式常式。 不建議使用此屬性。
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv switch MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966446"
---
# <a name="use_epv-switch"></a><span data-ttu-id="371f4-105">/use \_ epv 參數</span><span class="sxs-lookup"><span data-stu-id="371f4-105">/use\_epv switch</span></span>

<span data-ttu-id="371f4-106">**/Use \_ epv** 參數會指示 MIDL 編譯器產生伺服器 stub 程式碼，該程式碼會透過進入點向量 (epv) ，而不是透過靜態呼叫來呼叫伺服器應用程式常式。</span><span class="sxs-lookup"><span data-stu-id="371f4-106">The **/use\_epv** switch directs the MIDL compiler to generate server stub code that calls the server application routine through an entry-point vector (epv), rather than by a static call.</span></span> <span data-ttu-id="371f4-107">不建議使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="371f4-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /use_epv
```

## <a name="switch-options"></a><span data-ttu-id="371f4-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="371f4-108">Switch Options</span></span>

<span data-ttu-id="371f4-109">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="371f4-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="371f4-110">備註</span><span class="sxs-lookup"><span data-stu-id="371f4-110">Remarks</span></span>

<span data-ttu-id="371f4-111">一般而言，應用程式需要將靜態連結到伺服器應用程式常式。</span><span class="sxs-lookup"><span data-stu-id="371f4-111">Typically, applications require static linkage to the server application routine.</span></span> <span data-ttu-id="371f4-112">MIDL 編譯器預設會產生這類呼叫。</span><span class="sxs-lookup"><span data-stu-id="371f4-112">The MIDL compiler generates such a call by default.</span></span> <span data-ttu-id="371f4-113">但是，如果應用程式需要伺服器 stub 才能使用 epv 來呼叫伺服器應用程式常式，就必須指定 **/use \_ epv** 參數。</span><span class="sxs-lookup"><span data-stu-id="371f4-113">However, if an application requires the server stub to call the server application routine by using the epv, the **/use\_epv** switch must be specified.</span></span> <span data-ttu-id="371f4-114">當指定 **/use \_ epv** 參數時，MIDL 編譯器會產生預設 epv。</span><span class="sxs-lookup"><span data-stu-id="371f4-114">When the **/use\_epv** switch is specified, the MIDL compiler generates a default epv.</span></span> <span data-ttu-id="371f4-115">如果應用程式未透過 [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) 呼叫註冊另一個 epv，則會使用此預設 epv。</span><span class="sxs-lookup"><span data-stu-id="371f4-115">This default epv is then used if the application does not register another epv through the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span>

## <a name="examples"></a><span data-ttu-id="371f4-116">範例</span><span class="sxs-lookup"><span data-stu-id="371f4-116">Examples</span></span>

<span data-ttu-id="371f4-117">**midl/use \_ epv** *檔案名 \* \* \* .idl*\*</span><span class="sxs-lookup"><span data-stu-id="371f4-117">**midl /use\_epv** *filename\*\*\*.idl*\*</span></span>

## <a name="see-also"></a><span data-ttu-id="371f4-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="371f4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="371f4-119">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="371f4-119">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="371f4-120"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="371f4-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="371f4-121">**/no \_ 預設 \_ epv**</span><span class="sxs-lookup"><span data-stu-id="371f4-121">**/no\_default\_epv**</span></span>](-no-default-epv.md)
</dt> <dt>

[<span data-ttu-id="371f4-122">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="371f4-122">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 