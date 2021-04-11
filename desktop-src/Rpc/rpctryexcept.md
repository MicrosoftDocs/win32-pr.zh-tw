---
title: 'RpcTryExcept (的 Rpc .h) '
description: RpcTryExcept 語句提供 RPC 應用程式的結構化例外狀況處理。
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RpcTryExcept RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104376"
---
# <a name="rpctryexcept"></a><span data-ttu-id="8522e-104">RpcTryExcept</span><span class="sxs-lookup"><span data-stu-id="8522e-104">RpcTryExcept</span></span>

<span data-ttu-id="8522e-105">**RpcTryExcept** 語句提供 RPC 應用程式的結構化例外狀況處理。</span><span class="sxs-lookup"><span data-stu-id="8522e-105">The **RpcTryExcept** statement provides structured exception handling for RPC applications.</span></span> <span data-ttu-id="8522e-106">如果 **RpcTryExcept** 中的任何程式語句造成例外狀況，則會執行 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) 程式碼區塊中的語句。</span><span class="sxs-lookup"><span data-stu-id="8522e-106">If any of the program statements in the **RpcTryExcept** cause an exception, the statements in the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) code block are executed.</span></span> <span data-ttu-id="8522e-107">所有 **RpcTryExcept** 語句都必須由 [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) 語句終止。</span><span class="sxs-lookup"><span data-stu-id="8522e-107">All **RpcTryExcept** statements must be terminated by the [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) statement.</span></span>

<span data-ttu-id="8522e-108">如需詳細資訊，請參閱 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)。</span><span class="sxs-lookup"><span data-stu-id="8522e-108">For more information, see [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

<span data-ttu-id="8522e-109">**Windows Vista 和更新版本的 windows：** 建議將 [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)用於最常見例外狀況的結構化例外狀況處理，做為使用 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)的自訂篩選準則的替代方案。  </span><span class="sxs-lookup"><span data-stu-id="8522e-109">**Windows Vista and later versions of Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

## <a name="requirements"></a><span data-ttu-id="8522e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8522e-110">Requirements</span></span>



| <span data-ttu-id="8522e-111">需求</span><span class="sxs-lookup"><span data-stu-id="8522e-111">Requirement</span></span> | <span data-ttu-id="8522e-112">值</span><span class="sxs-lookup"><span data-stu-id="8522e-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8522e-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8522e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8522e-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8522e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8522e-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8522e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8522e-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8522e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8522e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8522e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8522e-118"><dt>Rpc。h</dt></span><span class="sxs-lookup"><span data-stu-id="8522e-118"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8522e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8522e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8522e-120">**RpcExcept**</span><span class="sxs-lookup"><span data-stu-id="8522e-120">**RpcExcept**</span></span>](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[<span data-ttu-id="8522e-121">**RpcExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="8522e-121">**RpcExceptionFilter**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[<span data-ttu-id="8522e-122">**RpcTryFinally**</span><span class="sxs-lookup"><span data-stu-id="8522e-122">**RpcTryFinally**</span></span>](rpctryfinally.md)
</dt> </dl>

 

