---
description: 傳回與這個 IAnalysisAlternate 相關聯的筆觸識別碼。
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'IAnalysisAlternate：： GetStrokeIds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848097"
---
# <a name="ianalysisalternategetstrokeids-method"></a><span data-ttu-id="8385a-103">IAnalysisAlternate：： GetStrokeIds 方法</span><span class="sxs-lookup"><span data-stu-id="8385a-103">IAnalysisAlternate::GetStrokeIds method</span></span>

<span data-ttu-id="8385a-104">傳回與這個 [**IAnalysisAlternate**](ianalysisalternate.md)相關聯的筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="8385a-104">Returns the stroke identifiers that are associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8385a-105">語法</span><span class="sxs-lookup"><span data-stu-id="8385a-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="8385a-106">參數</span><span class="sxs-lookup"><span data-stu-id="8385a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8385a-107">*pulStrokeIdsCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8385a-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8385a-108">**ULONG** 的指標，設定為與這個 [**IAnalysisAlternate**](ianalysisalternate.md)相關聯的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="8385a-108">A pointer to a **ULONG** that is set to the number of stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> <dt>

<span data-ttu-id="8385a-109">*pplStrokeIds* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8385a-109">*pplStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8385a-110">\[out，size \_ 是 (\* *PULSTROKEIDSCOUNT* \* sizeof (LONG) ) \]</span><span class="sxs-lookup"><span data-stu-id="8385a-110">\[out, size\_is(\**pulStrokeIdsCount* \* sizeof(LONG))\]</span></span>

<span data-ttu-id="8385a-111">長度 **為** *pulStrokeIdsCount* 的陣列，這個陣列會設定為與此 [**IAnalysisAlternate**](ianalysisalternate.md)相關聯的筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="8385a-111">An array of **LONG** of length *pulStrokeIdsCount* that is set to the stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8385a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8385a-112">Return value</span></span>

<span data-ttu-id="8385a-113">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8385a-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8385a-114">備註</span><span class="sxs-lookup"><span data-stu-id="8385a-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8385a-115">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *pplStrokeIds* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8385a-115">To avoid a memory leak, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokeIds* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8385a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8385a-116">Requirements</span></span>



| <span data-ttu-id="8385a-117">需求</span><span class="sxs-lookup"><span data-stu-id="8385a-117">Requirement</span></span> | <span data-ttu-id="8385a-118">值</span><span class="sxs-lookup"><span data-stu-id="8385a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8385a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8385a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8385a-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8385a-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8385a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8385a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8385a-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="8385a-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8385a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8385a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8385a-124"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8385a-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8385a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8385a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8385a-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8385a-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8385a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8385a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8385a-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="8385a-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="8385a-129">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="8385a-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

