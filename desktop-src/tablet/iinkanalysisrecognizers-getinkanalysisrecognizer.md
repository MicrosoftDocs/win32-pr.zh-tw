---
description: 抓取位於指定之索引處的 IInkAnalysisRecognizer。
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'IInkAnalysisRecognizers：： GetInkAnalysisRecognizer 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469132"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a><span data-ttu-id="b2d36-103">IInkAnalysisRecognizers：： GetInkAnalysisRecognizer 方法</span><span class="sxs-lookup"><span data-stu-id="b2d36-103">IInkAnalysisRecognizers::GetInkAnalysisRecognizer method</span></span>

<span data-ttu-id="b2d36-104">抓取位於指定之索引處的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 。</span><span class="sxs-lookup"><span data-stu-id="b2d36-104">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d36-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2d36-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="b2d36-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2d36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d36-107">*ulIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2d36-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d36-108">要取得之 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 物件的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="b2d36-108">The zero-based index of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="b2d36-109">*ppInkAnalysisRecognizer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b2d36-109">*ppInkAnalysisRecognizer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d36-110">位於指定索引處之 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="b2d36-110">A pointer to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d36-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2d36-111">Return value</span></span>

<span data-ttu-id="b2d36-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b2d36-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2d36-113">備註</span><span class="sxs-lookup"><span data-stu-id="b2d36-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b2d36-114">若要避免記憶體流失，請在 ppInkAnalysisRecognizer 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用筆墨分析辨識器時）。</span><span class="sxs-lookup"><span data-stu-id="b2d36-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppInkAnalysisRecognizer* when you no longer need to use the ink analysis recognizer.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2d36-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2d36-115">Requirements</span></span>



| <span data-ttu-id="b2d36-116">需求</span><span class="sxs-lookup"><span data-stu-id="b2d36-116">Requirement</span></span> | <span data-ttu-id="b2d36-117">值</span><span class="sxs-lookup"><span data-stu-id="b2d36-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d36-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2d36-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2d36-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2d36-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b2d36-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2d36-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2d36-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="b2d36-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b2d36-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b2d36-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2d36-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b2d36-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b2d36-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b2d36-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2d36-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2d36-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b2d36-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2d36-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d36-127">**InkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="b2d36-127">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="b2d36-128">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="b2d36-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

