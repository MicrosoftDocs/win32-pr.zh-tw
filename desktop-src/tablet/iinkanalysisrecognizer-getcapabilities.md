---
description: 抓取辨識器的功能。
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'IInkAnalysisRecognizer：： GetCapabilities 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113361"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a><span data-ttu-id="7ac7f-103">IInkAnalysisRecognizer：： GetCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="7ac7f-103">IInkAnalysisRecognizer::GetCapabilities method</span></span>

<span data-ttu-id="7ac7f-104">抓取辨識器的功能。</span><span class="sxs-lookup"><span data-stu-id="7ac7f-104">Retrieves the capabilities of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac7f-105">語法</span><span class="sxs-lookup"><span data-stu-id="7ac7f-105">Syntax</span></span>


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="7ac7f-106">參數</span><span class="sxs-lookup"><span data-stu-id="7ac7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ac7f-107">*pCapabilities* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ac7f-107">*pCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ac7f-108">[**RecognizerCapabilities**](recognizercapabilities.md)值的位元組合。</span><span class="sxs-lookup"><span data-stu-id="7ac7f-108">A bitwise combination of [**RecognizerCapabilities**](recognizercapabilities.md) values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ac7f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ac7f-109">Return value</span></span>

<span data-ttu-id="7ac7f-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="7ac7f-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ac7f-111">備註</span><span class="sxs-lookup"><span data-stu-id="7ac7f-111">Remarks</span></span>

<span data-ttu-id="7ac7f-112">每個 IInkAnalysisRecognizer 的這個值都是常數[ ](iinkanalysisrecognizer.md)</span><span class="sxs-lookup"><span data-stu-id="7ac7f-112">This value is constant for each [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac7f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ac7f-113">Requirements</span></span>



| <span data-ttu-id="7ac7f-114">需求</span><span class="sxs-lookup"><span data-stu-id="7ac7f-114">Requirement</span></span> | <span data-ttu-id="7ac7f-115">值</span><span class="sxs-lookup"><span data-stu-id="7ac7f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac7f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ac7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac7f-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ac7f-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7ac7f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ac7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac7f-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="7ac7f-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7ac7f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7ac7f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ac7f-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7ac7f-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7ac7f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7ac7f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ac7f-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ac7f-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7ac7f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ac7f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac7f-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="7ac7f-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="7ac7f-126">**RecognizerCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7ac7f-126">**RecognizerCapabilities**</span></span>](recognizercapabilities.md)
</dt> <dt>

[<span data-ttu-id="7ac7f-127">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="7ac7f-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




