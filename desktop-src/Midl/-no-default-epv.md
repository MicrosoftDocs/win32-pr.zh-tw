---
title: /no_default_epv 參數
description: /No \_ 預設 \_ epv 參數會指示 MIDL 編譯器不要產生預設的進入點向量 (epv) 。 不建議使用此屬性。
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv switch MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933127"
---
# <a name="no_default_epv-switch"></a><span data-ttu-id="ca02b-105">/no \_ 預設 \_ epv 參數</span><span class="sxs-lookup"><span data-stu-id="ca02b-105">/no\_default\_epv switch</span></span>

<span data-ttu-id="ca02b-106">**/No \_ 預設 \_ epv** 參數會指示 MIDL 編譯器不要產生預設的進入點向量 (epv) 。</span><span class="sxs-lookup"><span data-stu-id="ca02b-106">The **/no\_default\_epv** switch directs the MIDL compiler not to generate a default entry-point vector (epv).</span></span> <span data-ttu-id="ca02b-107">不建議使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="ca02b-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a><span data-ttu-id="ca02b-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="ca02b-108">Switch Options</span></span>

<span data-ttu-id="ca02b-109">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ca02b-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca02b-110">備註</span><span class="sxs-lookup"><span data-stu-id="ca02b-110">Remarks</span></span>

<span data-ttu-id="ca02b-111">在此情況下，應用程式必須向 [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) 呼叫註冊 epv。</span><span class="sxs-lookup"><span data-stu-id="ca02b-111">In this case, the application must register an epv with the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span> <span data-ttu-id="ca02b-112">將此參數與 [**/use \_ epv**](-use-epv.md) 參數進行比較。</span><span class="sxs-lookup"><span data-stu-id="ca02b-112">Compare this switch with the [**/use\_epv**](-use-epv.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="ca02b-113">範例</span><span class="sxs-lookup"><span data-stu-id="ca02b-113">Examples</span></span>

<span data-ttu-id="ca02b-114">**midl/no \_ 預設 \_ epv 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="ca02b-114">**midl /no\_default\_epv filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="ca02b-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca02b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca02b-116">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="ca02b-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="ca02b-117"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="ca02b-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ca02b-118">**/use \_ epv**</span><span class="sxs-lookup"><span data-stu-id="ca02b-118">**/use\_epv**</span></span>](-use-epv.md)
</dt> <dt>

[<span data-ttu-id="ca02b-119">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="ca02b-119">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 