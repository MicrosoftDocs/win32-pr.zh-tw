---
description: 如果發生錯誤，則捕獲背景筆墨分析作業的錯誤碼。
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'IAnalysisWarning：： GetBackgroundError 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191421"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a><span data-ttu-id="ac08c-103">IAnalysisWarning：： GetBackgroundError 方法</span><span class="sxs-lookup"><span data-stu-id="ac08c-103">IAnalysisWarning::GetBackgroundError method</span></span>

<span data-ttu-id="ac08c-104">如果發生錯誤，則捕獲背景筆墨分析作業的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ac08c-104">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac08c-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac08c-105">Syntax</span></span>


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a><span data-ttu-id="ac08c-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac08c-106">Parameters</span></span>

<span data-ttu-id="ac08c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ac08c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac08c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac08c-108">Return value</span></span>

<span data-ttu-id="ac08c-109">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="ac08c-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac08c-110">備註</span><span class="sxs-lookup"><span data-stu-id="ac08c-110">Remarks</span></span>

<span data-ttu-id="ac08c-111">如果背景分析作業中發生錯誤，則 [**IInkAnalyzer**](iinkanalyzer.md) 無法傳回錯誤碼，因為它發生在不同的執行緒中。</span><span class="sxs-lookup"><span data-stu-id="ac08c-111">If an error occurs within a background analysis operation, the [**IInkAnalyzer**](iinkanalyzer.md) cannot return the error code because it is occurring in a different thread.</span></span> <span data-ttu-id="ac08c-112">相反地， [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件處理常式會 [**接收 IAnalysisStatus**](ianalysisstatus.md) ，其中包含 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)為 **AnalysisWarningCode \_ BackgroundException** 的 [**IAnalysisWarning**](ianalysiswarning.md) 。</span><span class="sxs-lookup"><span data-stu-id="ac08c-112">Instead, the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event handler receives an [**IAnalysisStatus**](ianalysisstatus.md) that contains an [**IAnalysisWarning**](ianalysiswarning.md) with an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) of **AnalysisWarningCode\_BackgroundException**.</span></span> <span data-ttu-id="ac08c-113">此 **IAnalysisWarning** 包含背景分析操作的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ac08c-113">This **IAnalysisWarning** contains the error code for the background analysis operation.</span></span> <span data-ttu-id="ac08c-114">一般情況下，您的 **\_ IAnalysisEvents：： Results** 事件處理常式會傳回此錯誤碼，讓您可以在應用程式中的其他地方處理此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ac08c-114">In general, your **\_IAnalysisEvents::Results** event handler will return this error code so that it can be handled elsewhere in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac08c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac08c-115">Requirements</span></span>



| <span data-ttu-id="ac08c-116">需求</span><span class="sxs-lookup"><span data-stu-id="ac08c-116">Requirement</span></span> | <span data-ttu-id="ac08c-117">值</span><span class="sxs-lookup"><span data-stu-id="ac08c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac08c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac08c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac08c-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac08c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ac08c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac08c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac08c-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="ac08c-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ac08c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ac08c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac08c-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="ac08c-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ac08c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ac08c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac08c-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac08c-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ac08c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac08c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac08c-127">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="ac08c-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="ac08c-128">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="ac08c-128">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="ac08c-129">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="ac08c-129">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ac08c-130">**\_IAnalysisEvents：： Results**</span><span class="sxs-lookup"><span data-stu-id="ac08c-130">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="ac08c-131">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="ac08c-131">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="ac08c-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="ac08c-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

