---
description: 抓取辨識器的名稱。
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: 'IInkAnalysisRecognizer：： GetName 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fe263878d1fd5e914cf033111997d297a20c54f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971413"
---
# <a name="iinkanalysisrecognizergetname-method"></a><span data-ttu-id="33dce-103">IInkAnalysisRecognizer：： GetName 方法</span><span class="sxs-lookup"><span data-stu-id="33dce-103">IInkAnalysisRecognizer::GetName method</span></span>

<span data-ttu-id="33dce-104">抓取辨識器的名稱。</span><span class="sxs-lookup"><span data-stu-id="33dce-104">Retrieves the name of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="33dce-105">語法</span><span class="sxs-lookup"><span data-stu-id="33dce-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="33dce-106">參數</span><span class="sxs-lookup"><span data-stu-id="33dce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33dce-107">*pbstrName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="33dce-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33dce-108">辨識器的名稱。</span><span class="sxs-lookup"><span data-stu-id="33dce-108">The name of the recognizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33dce-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="33dce-109">Return value</span></span>

<span data-ttu-id="33dce-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="33dce-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="33dce-111">備註</span><span class="sxs-lookup"><span data-stu-id="33dce-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="33dce-112">若要避免記憶體流失， [](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) \* 當您不再需要使用字串時，請在 *pbstrName* 上呼叫 SysFreeString。</span><span class="sxs-lookup"><span data-stu-id="33dce-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrName* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="33dce-113">此名稱會針對辨識器所支援的區域中立語言進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="33dce-113">The name is localized for the region-neutral language that the recognizer supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="33dce-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="33dce-114">Requirements</span></span>



| <span data-ttu-id="33dce-115">需求</span><span class="sxs-lookup"><span data-stu-id="33dce-115">Requirement</span></span> | <span data-ttu-id="33dce-116">值</span><span class="sxs-lookup"><span data-stu-id="33dce-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33dce-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33dce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33dce-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33dce-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="33dce-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33dce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33dce-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="33dce-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="33dce-121">標頭</span><span class="sxs-lookup"><span data-stu-id="33dce-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="33dce-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="33dce-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="33dce-123">DLL</span><span class="sxs-lookup"><span data-stu-id="33dce-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33dce-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33dce-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="33dce-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33dce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33dce-126">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="33dce-126">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="33dce-127">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="33dce-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

