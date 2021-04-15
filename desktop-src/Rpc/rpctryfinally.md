---
title: 'RpcTryFinally (的 Rpc .h) '
description: RpcTryFinally 語句提供結構化終止處理。
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RpcTryFinally RPC
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465833"
---
# <a name="rpctryfinally"></a><span data-ttu-id="312c6-104">RpcTryFinally</span><span class="sxs-lookup"><span data-stu-id="312c6-104">RpcTryFinally</span></span>

<span data-ttu-id="312c6-105">**RpcTryFinally** 語句提供結構化終止處理。</span><span class="sxs-lookup"><span data-stu-id="312c6-105">The **RpcTryFinally** statement provides structured termination handling.</span></span> <span data-ttu-id="312c6-106">例外狀況發生在與 **RpcTryFinally** 語句相關聯之程式碼區塊的執行語句期間，會執行與 [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) 語句相關聯之程式碼區塊中的語句。</span><span class="sxs-lookup"><span data-stu-id="312c6-106">It an exception occurs during the execution statements of the code block associated with the **RpcTryFinally** statement, the statements in the code block associated with the [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) statement are executed.</span></span> <span data-ttu-id="312c6-107">所有 **RpcTryFinally** 語句都必須由 [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) 語句終止。</span><span class="sxs-lookup"><span data-stu-id="312c6-107">All **RpcTryFinally** statements must be terminated by an [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) statement.</span></span>

<span data-ttu-id="312c6-108">如需詳細資訊，請參閱 [**RpcFinally**](/previous-versions/aa375699(v=vs.80))。</span><span class="sxs-lookup"><span data-stu-id="312c6-108">For more information, see [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span></span>

## <a name="requirements"></a><span data-ttu-id="312c6-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="312c6-109">Requirements</span></span>



| <span data-ttu-id="312c6-110">需求</span><span class="sxs-lookup"><span data-stu-id="312c6-110">Requirement</span></span> | <span data-ttu-id="312c6-111">值</span><span class="sxs-lookup"><span data-stu-id="312c6-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="312c6-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="312c6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="312c6-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="312c6-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="312c6-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="312c6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="312c6-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="312c6-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="312c6-116">標頭</span><span class="sxs-lookup"><span data-stu-id="312c6-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="312c6-117"><dt>Rpc。h</dt></span><span class="sxs-lookup"><span data-stu-id="312c6-117"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="312c6-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="312c6-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="312c6-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="312c6-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span></span>
</dt> <dt>

<span data-ttu-id="312c6-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="312c6-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span></span>
</dt> </dl>

 

