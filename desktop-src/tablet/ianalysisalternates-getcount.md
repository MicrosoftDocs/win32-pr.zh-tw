---
description: 捕獲 IAnalysisAlternates 集合中包含的 IAnalysisAlternate 物件數目。
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'IAnalysisAlternates：： GetCount 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6300ff994d7bd49461e9be39aa433586ecaabc75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970441"
---
# <a name="ianalysisalternatesgetcount-method"></a><span data-ttu-id="13358-103">IAnalysisAlternates：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="13358-103">IAnalysisAlternates::GetCount method</span></span>

<span data-ttu-id="13358-104">捕獲 [**IAnalysisAlternates**](ianalysisalternates.md)集合中包含的 [**IAnalysisAlternate**](ianalysisalternate.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="13358-104">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="13358-105">語法</span><span class="sxs-lookup"><span data-stu-id="13358-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="13358-106">參數</span><span class="sxs-lookup"><span data-stu-id="13358-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13358-107">*pulCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="13358-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13358-108">不帶正負號的32位整數，設定為包含在 [**IAnalysisAlternates**](ianalysisalternates.md)集合中的 [**IAnalysisAlternate**](ianalysisalternate.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="13358-108">An unsigned 32-bit integer that is set to the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13358-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="13358-109">Return value</span></span>

<span data-ttu-id="13358-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="13358-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13358-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="13358-111">Requirements</span></span>



| <span data-ttu-id="13358-112">需求</span><span class="sxs-lookup"><span data-stu-id="13358-112">Requirement</span></span> | <span data-ttu-id="13358-113">值</span><span class="sxs-lookup"><span data-stu-id="13358-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13358-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13358-114">Minimum supported client</span></span><br/> | <span data-ttu-id="13358-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13358-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="13358-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13358-116">Minimum supported server</span></span><br/> | <span data-ttu-id="13358-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="13358-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="13358-118">標頭</span><span class="sxs-lookup"><span data-stu-id="13358-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="13358-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="13358-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="13358-120">DLL</span><span class="sxs-lookup"><span data-stu-id="13358-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13358-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13358-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="13358-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13358-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13358-123">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="13358-123">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="13358-124">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="13358-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




