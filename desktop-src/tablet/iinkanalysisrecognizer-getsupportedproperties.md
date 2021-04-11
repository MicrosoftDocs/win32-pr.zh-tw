---
description: 針對此 IInkAnalysisRecognizer 可為分析結果產生的屬性，抓取 (Guid) 的全域唯一識別碼。
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'IInkAnalysisRecognizer：： GetSupportedProperties 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943468"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a><span data-ttu-id="88cc7-103">IInkAnalysisRecognizer：： GetSupportedProperties 方法</span><span class="sxs-lookup"><span data-stu-id="88cc7-103">IInkAnalysisRecognizer::GetSupportedProperties method</span></span>

<span data-ttu-id="88cc7-104">針對此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 可為分析結果產生的屬性，抓取 (guid) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="88cc7-104">Retrieves the globally unique identifiers (GUIDs) for the properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

## <a name="syntax"></a><span data-ttu-id="88cc7-105">語法</span><span class="sxs-lookup"><span data-stu-id="88cc7-105">Syntax</span></span>


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="88cc7-106">參數</span><span class="sxs-lookup"><span data-stu-id="88cc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88cc7-107">*pulPropertiesCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="88cc7-107">*pulPropertiesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="88cc7-108">*PpProperties* 中的 guid 數目。</span><span class="sxs-lookup"><span data-stu-id="88cc7-108">The number of GUIDs in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="88cc7-109">*ppProperties* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="88cc7-109">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88cc7-110">此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 可為分析結果產生的屬性 guid 指標。</span><span class="sxs-lookup"><span data-stu-id="88cc7-110">A pointer to the GUIDs of properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88cc7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="88cc7-111">Return value</span></span>

<span data-ttu-id="88cc7-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="88cc7-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="88cc7-113">備註</span><span class="sxs-lookup"><span data-stu-id="88cc7-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="88cc7-114">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppProperties* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="88cc7-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppProperties* when you no longer need the information.</span></span>

 

<span data-ttu-id="88cc7-115">辨識器可支援線條度量、行號、信賴等級等等。</span><span class="sxs-lookup"><span data-stu-id="88cc7-115">A recognizer can support line metrics, line numbers, confidence levels, and so on.</span></span> <span data-ttu-id="88cc7-116">如需辨識器可支援之屬性的完整清單，請參閱 [RecognitionProperty 常數](recognitionproperty-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="88cc7-116">For a complete list of the properties that a recognizer can support, see [RecognitionProperty Constants](recognitionproperty-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88cc7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="88cc7-117">Requirements</span></span>



| <span data-ttu-id="88cc7-118">需求</span><span class="sxs-lookup"><span data-stu-id="88cc7-118">Requirement</span></span> | <span data-ttu-id="88cc7-119">值</span><span class="sxs-lookup"><span data-stu-id="88cc7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88cc7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88cc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="88cc7-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88cc7-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="88cc7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88cc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="88cc7-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="88cc7-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="88cc7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="88cc7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="88cc7-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="88cc7-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="88cc7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="88cc7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88cc7-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88cc7-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="88cc7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88cc7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cc7-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="88cc7-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="88cc7-130">RecognitionProperty 常數</span><span class="sxs-lookup"><span data-stu-id="88cc7-130">RecognitionProperty Constants</span></span>](recognitionproperty-constants.md)
</dt> <dt>

[<span data-ttu-id="88cc7-131">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="88cc7-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

