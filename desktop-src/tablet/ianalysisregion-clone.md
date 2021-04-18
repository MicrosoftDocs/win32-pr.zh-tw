---
description: 建立 IAnalysisRegion 的複本。
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: 'IAnalysisRegion：： Clone 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fb069ddb461ab4422f8cbbc8990fb6d735808e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971420"
---
# <a name="ianalysisregionclone-method"></a><span data-ttu-id="c7079-103">IAnalysisRegion：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="c7079-103">IAnalysisRegion::Clone method</span></span>

<span data-ttu-id="c7079-104">建立 [**IAnalysisRegion**](ianalysisregion.md)的複本。</span><span class="sxs-lookup"><span data-stu-id="c7079-104">Creates a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7079-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7079-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="c7079-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7079-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7079-107">*pClonedRegion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c7079-107">*pClonedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7079-108">[**IAnalysisRegion**](ianalysisregion.md)複本的指標。</span><span class="sxs-lookup"><span data-stu-id="c7079-108">A pointer to a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7079-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7079-109">Return value</span></span>

<span data-ttu-id="c7079-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c7079-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7079-111">備註</span><span class="sxs-lookup"><span data-stu-id="c7079-111">Remarks</span></span>

<span data-ttu-id="c7079-112">在 .NET Framework 中，此方法會 eqivalent 至 AnalysisCore. AnalysisRegionBase。</span><span class="sxs-lookup"><span data-stu-id="c7079-112">This method is eqivalent to theSystem.Windows.Ink.AnalysisCore.AnalysisRegionBase.Clone Method in the .NET Framework.</span></span>

> [!Caution]  
> <span data-ttu-id="c7079-113">若要避免記憶體流失，請在 pClonedRegion 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用複製的分析區域時）。</span><span class="sxs-lookup"><span data-stu-id="c7079-113">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pClonedRegion* when you no longer need to use the cloned analysis region.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c7079-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7079-114">Requirements</span></span>



| <span data-ttu-id="c7079-115">需求</span><span class="sxs-lookup"><span data-stu-id="c7079-115">Requirement</span></span> | <span data-ttu-id="c7079-116">值</span><span class="sxs-lookup"><span data-stu-id="c7079-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7079-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7079-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7079-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7079-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c7079-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7079-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7079-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="c7079-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c7079-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c7079-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7079-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c7079-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c7079-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c7079-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7079-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7079-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c7079-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7079-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7079-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="c7079-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="c7079-127">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c7079-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

