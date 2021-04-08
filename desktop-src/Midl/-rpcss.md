---
title: /rpcss 參數
description: 指定/rpcss 參數時，會將 \_ 介面的所有作業都指定為啟用配置屬性。 不建議使用此屬性。
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /rpcss 參數 MIDL
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022324"
---
# <a name="rpcss-switch"></a><span data-ttu-id="643d9-105">/rpcss 參數</span><span class="sxs-lookup"><span data-stu-id="643d9-105">/rpcss switch</span></span>

<span data-ttu-id="643d9-106">指定 **/rpcss** 參數時，會將介面的所有作業都指定為 [**啟用 \_ 配置**](enable-allocate.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="643d9-106">The **/rpcss** switch, when specified, acts as though the [**enable\_allocate**](enable-allocate.md) attribute was specified on all operations of the interface.</span></span> <span data-ttu-id="643d9-107">不建議使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="643d9-107">The usage of this attribute is not recommended.</span></span>

``` syntax
midl /rpcss
```

## <a name="switch-options"></a><span data-ttu-id="643d9-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="643d9-108">Switch Options</span></span>

<span data-ttu-id="643d9-109">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="643d9-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="643d9-110">備註</span><span class="sxs-lookup"><span data-stu-id="643d9-110">Remarks</span></span>

<span data-ttu-id="643d9-111">在預設模式下，只有在程式或介面具有 [**啟用 \_ 配置**](enable-allocate.md) 屬性，或在命令列上指定 **/rpcss** 參數時，才會啟用 RpcSs 套件。</span><span class="sxs-lookup"><span data-stu-id="643d9-111">In default mode, the RpcSs package is enabled only if either the procedure or interface has the [**enable\_allocate**](enable-allocate.md) attribute or the **/rpcss** switch is specified on the command line.</span></span> <span data-ttu-id="643d9-112">在 **/osf** 模式中，伺服器端 stub 會啟用 RpcSs 配置封裝。</span><span class="sxs-lookup"><span data-stu-id="643d9-112">In **/osf** mode, the server-side stub enables the RpcSs allocation package.</span></span>

## <a name="examples"></a><span data-ttu-id="643d9-113">範例</span><span class="sxs-lookup"><span data-stu-id="643d9-113">Examples</span></span>

<span data-ttu-id="643d9-114">**midl/rpcss 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="643d9-114">**midl /rpcss filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="643d9-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="643d9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643d9-116">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="643d9-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="643d9-117"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="643d9-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="643d9-118">**啟用 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="643d9-118">**enable\_allocate**</span></span>](enable-allocate.md)
</dt> <dt>

[<span data-ttu-id="643d9-119">**/osf**</span><span class="sxs-lookup"><span data-stu-id="643d9-119">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




