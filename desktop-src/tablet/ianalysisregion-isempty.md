---
description: 抓取值，指出 IAnalysisRegion 是否代表空白區域。
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'IAnalysisRegion：： IsEmpty 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971418"
---
# <a name="ianalysisregionisempty-method"></a><span data-ttu-id="bbafc-103">IAnalysisRegion：： IsEmpty 方法</span><span class="sxs-lookup"><span data-stu-id="bbafc-103">IAnalysisRegion::IsEmpty method</span></span>

<span data-ttu-id="bbafc-104">抓取值，指出 [**IAnalysisRegion**](ianalysisregion.md) 是否代表空白區域。</span><span class="sxs-lookup"><span data-stu-id="bbafc-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an empty region.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbafc-105">語法</span><span class="sxs-lookup"><span data-stu-id="bbafc-105">Syntax</span></span>


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a><span data-ttu-id="bbafc-106">參數</span><span class="sxs-lookup"><span data-stu-id="bbafc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbafc-107">*pfIsEmpty* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bbafc-107">*pfIsEmpty* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbafc-108">**變異 \_** 如果表示的區域是空的，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bbafc-108">**VARIANT\_TRUE** if the represented region is empty; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbafc-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbafc-109">Return value</span></span>

<span data-ttu-id="bbafc-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="bbafc-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbafc-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbafc-111">Requirements</span></span>



| <span data-ttu-id="bbafc-112">需求</span><span class="sxs-lookup"><span data-stu-id="bbafc-112">Requirement</span></span> | <span data-ttu-id="bbafc-113">值</span><span class="sxs-lookup"><span data-stu-id="bbafc-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbafc-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbafc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bbafc-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbafc-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bbafc-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbafc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bbafc-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="bbafc-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bbafc-118">標頭</span><span class="sxs-lookup"><span data-stu-id="bbafc-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbafc-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="bbafc-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bbafc-120">DLL</span><span class="sxs-lookup"><span data-stu-id="bbafc-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbafc-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbafc-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bbafc-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbafc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbafc-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="bbafc-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="bbafc-124">**IAnalysisRegion：： IsInfinite 方法**</span><span class="sxs-lookup"><span data-stu-id="bbafc-124">**IAnalysisRegion::IsInfinite Method**</span></span>](ianalysisregion-isinfinite.md)
</dt> <dt>

[<span data-ttu-id="bbafc-125">**IAnalysisRegion：： MakeEmpty 方法**</span><span class="sxs-lookup"><span data-stu-id="bbafc-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="bbafc-126">**IAnalysisRegion：： MakeInfinite 方法**</span><span class="sxs-lookup"><span data-stu-id="bbafc-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="bbafc-127">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="bbafc-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




