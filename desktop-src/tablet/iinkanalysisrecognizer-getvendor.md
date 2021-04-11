---
description: 抓取 IInkAnalysisRecognizer 的廠商名稱。
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: 'IInkAnalysisRecognizer：： GetVendor 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113357"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a><span data-ttu-id="0e44f-103">IInkAnalysisRecognizer：： GetVendor 方法</span><span class="sxs-lookup"><span data-stu-id="0e44f-103">IInkAnalysisRecognizer::GetVendor method</span></span>

<span data-ttu-id="0e44f-104">抓取 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)的廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="0e44f-104">Retrieves the vendor name of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e44f-105">語法</span><span class="sxs-lookup"><span data-stu-id="0e44f-105">Syntax</span></span>


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a><span data-ttu-id="0e44f-106">參數</span><span class="sxs-lookup"><span data-stu-id="0e44f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e44f-107">*pbstrVendor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0e44f-107">*pbstrVendor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e44f-108">廠商的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e44f-108">The name of the vendor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e44f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e44f-109">Return value</span></span>

<span data-ttu-id="0e44f-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="0e44f-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e44f-111">備註</span><span class="sxs-lookup"><span data-stu-id="0e44f-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="0e44f-112">若要避免記憶體流失， [](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) \* 當您不再需要使用字串時，請在 *pbstrVendor* 上呼叫 SysFreeString。</span><span class="sxs-lookup"><span data-stu-id="0e44f-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrVendor* when you no longer need to use the string.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e44f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e44f-113">Requirements</span></span>



| <span data-ttu-id="0e44f-114">需求</span><span class="sxs-lookup"><span data-stu-id="0e44f-114">Requirement</span></span> | <span data-ttu-id="0e44f-115">值</span><span class="sxs-lookup"><span data-stu-id="0e44f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e44f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e44f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0e44f-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e44f-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0e44f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e44f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0e44f-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="0e44f-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0e44f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0e44f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e44f-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="0e44f-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0e44f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0e44f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e44f-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e44f-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0e44f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e44f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e44f-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="0e44f-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="0e44f-126">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="0e44f-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

