---
description: 減少 IAnalysisRegion 以代表空白區域。
ms.assetid: 647a90ee-a5fe-4019-92bb-76b84207d86e
title: 'IAnalysisRegion：： MakeEmpty 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.MakeEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76ca10d98ad6c240ebcd61b7bf83934fefd838b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690608"
---
# <a name="ianalysisregionmakeempty-method"></a><span data-ttu-id="d737c-103">IAnalysisRegion：： MakeEmpty 方法</span><span class="sxs-lookup"><span data-stu-id="d737c-103">IAnalysisRegion::MakeEmpty method</span></span>

<span data-ttu-id="d737c-104">減少 [**IAnalysisRegion**](ianalysisregion.md) 以代表空白區域。</span><span class="sxs-lookup"><span data-stu-id="d737c-104">Reduces the [**IAnalysisRegion**](ianalysisregion.md) to represent an empty area.</span></span>

## <a name="syntax"></a><span data-ttu-id="d737c-105">語法</span><span class="sxs-lookup"><span data-stu-id="d737c-105">Syntax</span></span>


```C++
HRESULT MakeEmpty();
```



## <a name="parameters"></a><span data-ttu-id="d737c-106">參數</span><span class="sxs-lookup"><span data-stu-id="d737c-106">Parameters</span></span>

<span data-ttu-id="d737c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d737c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d737c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d737c-108">Return value</span></span>

<span data-ttu-id="d737c-109">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d737c-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d737c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d737c-110">Requirements</span></span>



| <span data-ttu-id="d737c-111">需求</span><span class="sxs-lookup"><span data-stu-id="d737c-111">Requirement</span></span> | <span data-ttu-id="d737c-112">值</span><span class="sxs-lookup"><span data-stu-id="d737c-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d737c-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d737c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d737c-114">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d737c-114">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d737c-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d737c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d737c-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="d737c-116">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d737c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d737c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d737c-118"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d737c-118"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d737c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d737c-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d737c-120"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d737c-120"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d737c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d737c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d737c-122">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="d737c-122">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="d737c-123">**IAnalysisRegion：： IsEmpty 方法**</span><span class="sxs-lookup"><span data-stu-id="d737c-123">**IAnalysisRegion::IsEmpty Method**</span></span>](ianalysisregion-isempty.md)
</dt> <dt>

[<span data-ttu-id="d737c-124">**IAnalysisRegion：： IsInfinite 方法**</span><span class="sxs-lookup"><span data-stu-id="d737c-124">**IAnalysisRegion::IsInfinite Method**</span></span>](ianalysisregion-isinfinite.md)
</dt> <dt>

[<span data-ttu-id="d737c-125">**IAnalysisRegion：： MakeInfinite 方法**</span><span class="sxs-lookup"><span data-stu-id="d737c-125">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="d737c-126">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="d737c-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




