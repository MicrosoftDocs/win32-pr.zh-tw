---
UID: ''
title: GuardCheckLongJumpTarget 函式
description: 嘗試驗證 longjmp 的目標是否有效。
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "106968893"
---
# <a name="guardchecklongjumptarget-function"></a><span data-ttu-id="62081-103">GuardCheckLongJumpTarget 函式</span><span class="sxs-lookup"><span data-stu-id="62081-103">GuardCheckLongJumpTarget function</span></span>

## <a name="description"></a><span data-ttu-id="62081-104">Description</span><span class="sxs-lookup"><span data-stu-id="62081-104">Description</span></span>

<span data-ttu-id="62081-105">嘗試確認 [longjmp](/cpp/c-runtime-library/reference/longjmp) 的目標是否適用于具有 [控制流程防護 (CFG) ](../secbp/control-flow-guard.md) 啟用的進程。</span><span class="sxs-lookup"><span data-stu-id="62081-105">Attempts to verify whether the target of a [longjmp](/cpp/c-runtime-library/reference/longjmp) is valid for a process which has [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) enabled.</span></span>

<span data-ttu-id="62081-106">如果目標位址對應至影像對應，就會針對二進位檔解壓縮有效的目標。</span><span class="sxs-lookup"><span data-stu-id="62081-106">If the target address corresponds to an image mapping, the valid targets are extracted for the binary.</span></span>
<span data-ttu-id="62081-107">函數會使用這些目標來驗證目標。</span><span class="sxs-lookup"><span data-stu-id="62081-107">The function uses those targets to validate the target.</span></span>
<span data-ttu-id="62081-108">如果二進位檔沒有描述有效 *longjmp* 目標集合的中繼資料，則函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="62081-108">If the binary does not have metadata that describes the set of valid *longjmp* targets, the function returns **TRUE**.</span></span>

<span data-ttu-id="62081-109">如果目標位址對應到非影像對應（如同在 JIT 程式碼中），則會參考全域唯讀原則來判斷是否允許跳躍。</span><span class="sxs-lookup"><span data-stu-id="62081-109">If the target address corresponds to a non-image mapping, as in JIT code, a global read-only policy is consulted to determine whether the jump is allowed.</span></span>

## <a name="parameters"></a><span data-ttu-id="62081-110">參數</span><span class="sxs-lookup"><span data-stu-id="62081-110">Parameters</span></span>

### <a name="targetaddress-in"></a><span data-ttu-id="62081-111">TargetAddress [in]</span><span class="sxs-lookup"><span data-stu-id="62081-111">TargetAddress [in]</span></span>

<span data-ttu-id="62081-112">跳躍的目標位址。</span><span class="sxs-lookup"><span data-stu-id="62081-112">The target address for the jump.</span></span>

### <a name="flags-in"></a><span data-ttu-id="62081-113">旗標 [in]</span><span class="sxs-lookup"><span data-stu-id="62081-113">Flags [in]</span></span>

<span data-ttu-id="62081-114">描述要在位址上執行之作業的旗標。</span><span class="sxs-lookup"><span data-stu-id="62081-114">Flags describing the operation to be performed on the address.</span></span>
<span data-ttu-id="62081-115">如果您指定 **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1) ，則如果目標無效，此函數不會終止進程。</span><span class="sxs-lookup"><span data-stu-id="62081-115">If you specify **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), this function does not terminate the process if the target is invalid.</span></span>

## <a name="returns"></a><span data-ttu-id="62081-116">傳回</span><span class="sxs-lookup"><span data-stu-id="62081-116">Returns</span></span>

<span data-ttu-id="62081-117">如果目標有效則 **為 TRUE** ，否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="62081-117">**TRUE** if the target is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62081-118">備註</span><span class="sxs-lookup"><span data-stu-id="62081-118">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="62081-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62081-119">See also</span></span>
