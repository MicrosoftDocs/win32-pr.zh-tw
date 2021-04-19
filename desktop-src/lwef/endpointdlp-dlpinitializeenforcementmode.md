---
description: 針對一組端點資料遺失防止 (DLP) 作業，通知系統所需的強制模式。
title: 'DlpInitializeEnforcementMode 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495522"
---
# <a name="dlpinitializeenforcementmode-function"></a><span data-ttu-id="3b6f2-103">DlpInitializeEnforcementMode 函式</span><span class="sxs-lookup"><span data-stu-id="3b6f2-103">DlpInitializeEnforcementMode function</span></span>

<span data-ttu-id="3b6f2-104">針對一組端點資料遺失防止 (DLP) 作業，通知系統所需的強制模式。</span><span class="sxs-lookup"><span data-stu-id="3b6f2-104">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b6f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b6f2-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a><span data-ttu-id="3b6f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b6f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b6f2-107">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b6f2-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6f2-108">**DWORD** ，指定包含在 *OperationEnforcement* 陣列中的作業數目。</span><span class="sxs-lookup"><span data-stu-id="3b6f2-108">A **DWORD** specifying the number of operations included in the *OperationEnforcement* array.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3b6f2-109">*OperationEnforcement* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b6f2-109">*OperationEnforcement* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6f2-110">[DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md)結構的陣列，可指定端點 DLP 作業的強制等級。</span><span class="sxs-lookup"><span data-stu-id="3b6f2-110">An array of [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structures that specify the enforcement level for an endpoint DLP operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="3b6f2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b6f2-111">Return value</span></span>

<span data-ttu-id="3b6f2-112">傳回 HRESULT （包括但不限於下列值）。</span><span class="sxs-lookup"><span data-stu-id="3b6f2-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="3b6f2-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3b6f2-113">HRESULT</span></span> | <span data-ttu-id="3b6f2-114">描述</span><span class="sxs-lookup"><span data-stu-id="3b6f2-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="3b6f2-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b6f2-115">S_OK</span></span> | <span data-ttu-id="3b6f2-116">函數已順利完成</span><span class="sxs-lookup"><span data-stu-id="3b6f2-116">The function completed successfully</span></span> |
| <span data-ttu-id="3b6f2-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3b6f2-117">E_INVALIDARG</span></span> | <span data-ttu-id="3b6f2-118">一或多個函數參數無效。</span><span class="sxs-lookup"><span data-stu-id="3b6f2-118">One or more of the function parameters are invalid.</span></span> |
| <span data-ttu-id="3b6f2-119">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="3b6f2-119">E_OUTOFMEMORY</span></span> | <span data-ttu-id="3b6f2-120">作業的記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="3b6f2-120">Memory allocation for the operation failed.</span></span> |



## <a name="remarks"></a><span data-ttu-id="3b6f2-121">備註</span><span class="sxs-lookup"><span data-stu-id="3b6f2-121">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="3b6f2-122">需求</span><span class="sxs-lookup"><span data-stu-id="3b6f2-122">Requirements</span></span>



| <span data-ttu-id="3b6f2-123">需求</span><span class="sxs-lookup"><span data-stu-id="3b6f2-123">Requirement</span></span>          |    <span data-ttu-id="3b6f2-124">值</span><span class="sxs-lookup"><span data-stu-id="3b6f2-124">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b6f2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b6f2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3b6f2-126">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="3b6f2-126">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="3b6f2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3b6f2-127">DLL</span></span><br/>                      | <span data-ttu-id="3b6f2-128">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="3b6f2-128">EndpointDlp.dll</span></span> |