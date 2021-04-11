---
description: 抓取值，指出 IAnalysisRegion 是否代表無限區域。
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'IAnalysisRegion：： IsInfinite 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191425"
---
# <a name="ianalysisregionisinfinite-method"></a><span data-ttu-id="e7aaa-103">IAnalysisRegion：： IsInfinite 方法</span><span class="sxs-lookup"><span data-stu-id="e7aaa-103">IAnalysisRegion::IsInfinite method</span></span>

<span data-ttu-id="e7aaa-104">抓取值，指出 [**IAnalysisRegion**](ianalysisregion.md) 是否代表無限區域。</span><span class="sxs-lookup"><span data-stu-id="e7aaa-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite region.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7aaa-105">語法</span><span class="sxs-lookup"><span data-stu-id="e7aaa-105">Syntax</span></span>


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a><span data-ttu-id="e7aaa-106">參數</span><span class="sxs-lookup"><span data-stu-id="e7aaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7aaa-107">*pfIsInfinite* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e7aaa-107">*pfIsInfinite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7aaa-108">**變異 \_** 如果表示的區域是無限的，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e7aaa-108">**VARIANT\_TRUE** if the represented region is infinite; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7aaa-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7aaa-109">Return value</span></span>

<span data-ttu-id="e7aaa-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="e7aaa-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7aaa-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7aaa-111">Requirements</span></span>



| <span data-ttu-id="e7aaa-112">需求</span><span class="sxs-lookup"><span data-stu-id="e7aaa-112">Requirement</span></span> | <span data-ttu-id="e7aaa-113">值</span><span class="sxs-lookup"><span data-stu-id="e7aaa-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7aaa-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7aaa-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e7aaa-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7aaa-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e7aaa-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7aaa-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e7aaa-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="e7aaa-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e7aaa-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e7aaa-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7aaa-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e7aaa-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e7aaa-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e7aaa-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7aaa-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7aaa-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e7aaa-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7aaa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7aaa-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="e7aaa-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="e7aaa-124">**IAnalysisRegion：： IsEmpty 方法**</span><span class="sxs-lookup"><span data-stu-id="e7aaa-124">**IAnalysisRegion::IsEmpty Method**</span></span>](ianalysisregion-isempty.md)
</dt> <dt>

[<span data-ttu-id="e7aaa-125">**IAnalysisRegion：： MakeEmpty 方法**</span><span class="sxs-lookup"><span data-stu-id="e7aaa-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="e7aaa-126">**IAnalysisRegion：： MakeInfinite 方法**</span><span class="sxs-lookup"><span data-stu-id="e7aaa-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="e7aaa-127">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="e7aaa-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




