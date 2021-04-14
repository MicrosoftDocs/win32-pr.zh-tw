---
description: 抓取此 IInkAnalysisRecognizer 支援之地區設定的識別碼。
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'IInkAnalysisRecognizer：： GetLanguages 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848086"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a><span data-ttu-id="cb8cb-103">IInkAnalysisRecognizer：： GetLanguages 方法</span><span class="sxs-lookup"><span data-stu-id="cb8cb-103">IInkAnalysisRecognizer::GetLanguages method</span></span>

<span data-ttu-id="cb8cb-104">抓取此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 支援之地區設定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb8cb-104">Retrieves the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb8cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="cb8cb-105">Syntax</span></span>


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a><span data-ttu-id="cb8cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="cb8cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb8cb-107">*pulLanguagesCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="cb8cb-107">*pulLanguagesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb8cb-108">*PpulLanguages* 中的識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="cb8cb-108">The number of identifiers in *ppulLanguages*.</span></span>

</dd> <dt>

<span data-ttu-id="cb8cb-109">*ppulLanguages* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cb8cb-109">*ppulLanguages* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb8cb-110">此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 支援之地區設定的識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="cb8cb-110">A pointer to the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb8cb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb8cb-111">Return value</span></span>

<span data-ttu-id="cb8cb-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="cb8cb-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb8cb-113">備註</span><span class="sxs-lookup"><span data-stu-id="cb8cb-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cb8cb-114">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppulLanguages* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cb8cb-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppulLanguages* when you no longer need the information.</span></span>

 

<span data-ttu-id="cb8cb-115">這個方法會傳回物件和手勢辨識器的空陣列。</span><span class="sxs-lookup"><span data-stu-id="cb8cb-115">This method returns an empty array for object and gesture recognizers.</span></span>

<span data-ttu-id="cb8cb-116">如需語言識別項的詳細資訊，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。</span><span class="sxs-lookup"><span data-stu-id="cb8cb-116">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb8cb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb8cb-117">Requirements</span></span>



| <span data-ttu-id="cb8cb-118">需求</span><span class="sxs-lookup"><span data-stu-id="cb8cb-118">Requirement</span></span> | <span data-ttu-id="cb8cb-119">值</span><span class="sxs-lookup"><span data-stu-id="cb8cb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb8cb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb8cb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb8cb-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb8cb-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cb8cb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb8cb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb8cb-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="cb8cb-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cb8cb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cb8cb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb8cb-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="cb8cb-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cb8cb-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cb8cb-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb8cb-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb8cb-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cb8cb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb8cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb8cb-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="cb8cb-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="cb8cb-130">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="cb8cb-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

