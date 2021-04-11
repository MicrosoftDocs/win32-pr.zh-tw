---
description: 抓取字元範圍的陣列，表示支援的 Unicode 字元範圍。
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'IInkAnalysisRecognizer：： GetUnicodeRanges 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848085"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a><span data-ttu-id="21878-103">IInkAnalysisRecognizer：： GetUnicodeRanges 方法</span><span class="sxs-lookup"><span data-stu-id="21878-103">IInkAnalysisRecognizer::GetUnicodeRanges method</span></span>

<span data-ttu-id="21878-104">抓取字元範圍的陣列，表示支援的 Unicode 字元範圍。</span><span class="sxs-lookup"><span data-stu-id="21878-104">Retrieves an array of character ranges representing the supported Unicode character ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="21878-105">語法</span><span class="sxs-lookup"><span data-stu-id="21878-105">Syntax</span></span>


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a><span data-ttu-id="21878-106">參數</span><span class="sxs-lookup"><span data-stu-id="21878-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21878-107">*pulNumberOfRanges* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="21878-107">*pulNumberOfRanges* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="21878-108">*PpulLowUnicode* 所指向的字元範圍數目。</span><span class="sxs-lookup"><span data-stu-id="21878-108">The number of character ranges pointed to by *ppulLowUnicode*.</span></span>

</dd> <dt>

<span data-ttu-id="21878-109">*ppulLowUnicode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="21878-109">*ppulLowUnicode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21878-110">字元範圍陣列的指標，表示支援的 Unicode 字元範圍。</span><span class="sxs-lookup"><span data-stu-id="21878-110">Pointer to an array of character ranges representing the supported Unicode character ranges.</span></span>

</dd> <dt>

<span data-ttu-id="21878-111">*ppusUnicodeRangeLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="21878-111">*ppusUnicodeRangeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21878-112">值陣列的指標，指出每個陣列指向 *ppulLowUnicode* 的長度。</span><span class="sxs-lookup"><span data-stu-id="21878-112">Pointer to an array of values indicating the length of each array point to by *ppulLowUnicode*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21878-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="21878-113">Return value</span></span>

<span data-ttu-id="21878-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="21878-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21878-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="21878-115">Requirements</span></span>



| <span data-ttu-id="21878-116">需求</span><span class="sxs-lookup"><span data-stu-id="21878-116">Requirement</span></span> | <span data-ttu-id="21878-117">值</span><span class="sxs-lookup"><span data-stu-id="21878-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21878-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21878-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21878-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21878-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="21878-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21878-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21878-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="21878-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="21878-122">標頭</span><span class="sxs-lookup"><span data-stu-id="21878-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21878-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="21878-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="21878-124">DLL</span><span class="sxs-lookup"><span data-stu-id="21878-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21878-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21878-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="21878-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21878-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21878-127">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="21878-127">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




