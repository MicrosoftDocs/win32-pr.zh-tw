---
description: 抓取辨識器 (GUID) 的全域唯一識別碼。
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: 'IInkAnalysisRecognizer：： GetGuid 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848087"
---
# <a name="iinkanalysisrecognizergetguid-method"></a><span data-ttu-id="88b84-103">IInkAnalysisRecognizer：： GetGuid 方法</span><span class="sxs-lookup"><span data-stu-id="88b84-103">IInkAnalysisRecognizer::GetGuid method</span></span>

<span data-ttu-id="88b84-104">抓取辨識器 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b84-104">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b84-105">語法</span><span class="sxs-lookup"><span data-stu-id="88b84-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="88b84-106">參數</span><span class="sxs-lookup"><span data-stu-id="88b84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b84-107">*pId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="88b84-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88b84-108">識別此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)的 GUID。</span><span class="sxs-lookup"><span data-stu-id="88b84-108">The GUID that identifies this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b84-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="88b84-109">Return value</span></span>

<span data-ttu-id="88b84-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="88b84-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88b84-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="88b84-111">Requirements</span></span>



| <span data-ttu-id="88b84-112">需求</span><span class="sxs-lookup"><span data-stu-id="88b84-112">Requirement</span></span> | <span data-ttu-id="88b84-113">值</span><span class="sxs-lookup"><span data-stu-id="88b84-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b84-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88b84-114">Minimum supported client</span></span><br/> | <span data-ttu-id="88b84-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88b84-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="88b84-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88b84-116">Minimum supported server</span></span><br/> | <span data-ttu-id="88b84-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="88b84-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="88b84-118">標頭</span><span class="sxs-lookup"><span data-stu-id="88b84-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="88b84-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="88b84-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="88b84-120">DLL</span><span class="sxs-lookup"><span data-stu-id="88b84-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88b84-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88b84-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="88b84-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88b84-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b84-123">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="88b84-123">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="88b84-124">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="88b84-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




