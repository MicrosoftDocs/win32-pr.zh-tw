---
description: 取得 IAnalysisAlternate 物件的已識別字串值。
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'IAnalysisAlternate：： GetRecognizedString 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511708"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a><span data-ttu-id="04972-103">IAnalysisAlternate：： GetRecognizedString 方法</span><span class="sxs-lookup"><span data-stu-id="04972-103">IAnalysisAlternate::GetRecognizedString method</span></span>

<span data-ttu-id="04972-104">取得 [**IAnalysisAlternate**](ianalysisalternate.md) 物件的已識別字串值。</span><span class="sxs-lookup"><span data-stu-id="04972-104">Gets the recognized string value of the [**IAnalysisAlternate**](ianalysisalternate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="04972-105">語法</span><span class="sxs-lookup"><span data-stu-id="04972-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="04972-106">參數</span><span class="sxs-lookup"><span data-stu-id="04972-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04972-107">*pbstrRecognizedString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="04972-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04972-108">設為可辨識之字串值的 **BSTR** 指標。</span><span class="sxs-lookup"><span data-stu-id="04972-108">A pointer to the **BSTR** that is set to the recognized string value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04972-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="04972-109">Return value</span></span>

<span data-ttu-id="04972-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="04972-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04972-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="04972-111">Requirements</span></span>



| <span data-ttu-id="04972-112">需求</span><span class="sxs-lookup"><span data-stu-id="04972-112">Requirement</span></span> | <span data-ttu-id="04972-113">值</span><span class="sxs-lookup"><span data-stu-id="04972-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04972-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04972-114">Minimum supported client</span></span><br/> | <span data-ttu-id="04972-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04972-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04972-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04972-116">Minimum supported server</span></span><br/> | <span data-ttu-id="04972-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="04972-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="04972-118">標頭</span><span class="sxs-lookup"><span data-stu-id="04972-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="04972-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="04972-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="04972-120">DLL</span><span class="sxs-lookup"><span data-stu-id="04972-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04972-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04972-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="04972-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04972-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04972-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="04972-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="04972-124">**IInkAnalyzer：： GetRecognizedString 方法**</span><span class="sxs-lookup"><span data-stu-id="04972-124">**IInkAnalyzer::GetRecognizedString Method**</span></span>](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




