---
description: 判斷指定的 IAnalysisRegion 是否包含與目前 IAnalysisRegion 物件相同的值。
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'IAnalysisRegion：： EqualsRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113408"
---
# <a name="ianalysisregionequalsregion-method"></a><span data-ttu-id="04fcf-103">IAnalysisRegion：： EqualsRegion 方法</span><span class="sxs-lookup"><span data-stu-id="04fcf-103">IAnalysisRegion::EqualsRegion method</span></span>

<span data-ttu-id="04fcf-104">判斷指定的 [**IAnalysisRegion**](ianalysisregion.md) 是否包含與目前 **IAnalysisRegion** 物件相同的值。</span><span class="sxs-lookup"><span data-stu-id="04fcf-104">Determines whether the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current **IAnalysisRegion** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="04fcf-105">語法</span><span class="sxs-lookup"><span data-stu-id="04fcf-105">Syntax</span></span>


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a><span data-ttu-id="04fcf-106">參數</span><span class="sxs-lookup"><span data-stu-id="04fcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04fcf-107">*pOtherRegion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04fcf-107">*pOtherRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04fcf-108">要與目前 **IAnalysisRegion** 比較的 [**IAnalysisRegion**](ianalysisregion.md)物件。</span><span class="sxs-lookup"><span data-stu-id="04fcf-108">The [**IAnalysisRegion**](ianalysisregion.md) object to compare with the current **IAnalysisRegion**.</span></span>

</dd> <dt>

<span data-ttu-id="04fcf-109">*pfRegionsEqual* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="04fcf-109">*pfRegionsEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04fcf-110">**變異 \_** 如果指定的 [**IAnalysisRegion**](ianalysisregion.md)包含與目前 IAnalysisRegion 相同的值，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="04fcf-110">**VARIANT\_TRUE** if the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current IAnalysisRegion; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04fcf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="04fcf-111">Return value</span></span>

<span data-ttu-id="04fcf-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="04fcf-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04fcf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="04fcf-113">Requirements</span></span>



| <span data-ttu-id="04fcf-114">需求</span><span class="sxs-lookup"><span data-stu-id="04fcf-114">Requirement</span></span> | <span data-ttu-id="04fcf-115">值</span><span class="sxs-lookup"><span data-stu-id="04fcf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04fcf-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04fcf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="04fcf-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04fcf-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04fcf-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04fcf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="04fcf-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="04fcf-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="04fcf-120">標頭</span><span class="sxs-lookup"><span data-stu-id="04fcf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="04fcf-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="04fcf-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="04fcf-122">DLL</span><span class="sxs-lookup"><span data-stu-id="04fcf-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04fcf-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04fcf-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="04fcf-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04fcf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04fcf-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="04fcf-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> </dl>

 

 




