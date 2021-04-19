---
description: 抓取集合中位於指定索引位置的 IAnalysisAlternate 物件。
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'IAnalysisAlternates：： GetAnalysisAlternate 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966727"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a><span data-ttu-id="05f57-103">IAnalysisAlternates：： GetAnalysisAlternate 方法</span><span class="sxs-lookup"><span data-stu-id="05f57-103">IAnalysisAlternates::GetAnalysisAlternate method</span></span>

<span data-ttu-id="05f57-104">抓取集合中位於指定索引位置的 [**IAnalysisAlternate**](ianalysisalternate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="05f57-104">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f57-105">語法</span><span class="sxs-lookup"><span data-stu-id="05f57-105">Syntax</span></span>


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="05f57-106">參數</span><span class="sxs-lookup"><span data-stu-id="05f57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f57-107">*ulIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05f57-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05f57-108">要取得之 [**IAnalysisAlternate**](ianalysisalternate.md) 物件的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="05f57-108">The zero-based index of the [**IAnalysisAlternate**](ianalysisalternate.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="05f57-109">*ppAlternate* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="05f57-109">*ppAlternate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05f57-110">集合中位於指定索引位置之 [**IAnalysisAlternate**](ianalysisalternate.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="05f57-110">A pointer to the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f57-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="05f57-111">Return value</span></span>

<span data-ttu-id="05f57-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="05f57-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05f57-113">備註</span><span class="sxs-lookup"><span data-stu-id="05f57-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="05f57-114">若要避免記憶體流失，當您不再需要流量分析替代時，請在 ppAlternate 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \*  。</span><span class="sxs-lookup"><span data-stu-id="05f57-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternate* when you no longer need to use the analysis alternate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05f57-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="05f57-115">Requirements</span></span>



| <span data-ttu-id="05f57-116">需求</span><span class="sxs-lookup"><span data-stu-id="05f57-116">Requirement</span></span> | <span data-ttu-id="05f57-117">值</span><span class="sxs-lookup"><span data-stu-id="05f57-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f57-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05f57-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05f57-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05f57-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="05f57-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05f57-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05f57-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="05f57-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="05f57-122">標頭</span><span class="sxs-lookup"><span data-stu-id="05f57-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f57-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="05f57-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="05f57-124">DLL</span><span class="sxs-lookup"><span data-stu-id="05f57-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05f57-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05f57-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="05f57-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05f57-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f57-127">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="05f57-127">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="05f57-128">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="05f57-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

