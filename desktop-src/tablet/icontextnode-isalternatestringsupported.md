---
description: 指出指定的已辨識字串是否來自系統字典、使用者字典或字組清單。
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'ICoNtextNode：： IsAlternateStringSupported 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991744"
---
# <a name="icontextnodeisalternatestringsupported-method"></a><span data-ttu-id="3c009-103">ICoNtextNode：： IsAlternateStringSupported 方法</span><span class="sxs-lookup"><span data-stu-id="3c009-103">IContextNode::IsAlternateStringSupported method</span></span>

<span data-ttu-id="3c009-104">指出指定的已辨識字串是否來自系統字典、使用者字典或字組清單。</span><span class="sxs-lookup"><span data-stu-id="3c009-104">Indicates whether the specified recognized string came from the system dictionary, user dictionary, or word list.</span></span> <span data-ttu-id="3c009-105">任何對應的提示節點中的任何限制資料（例如 wordlists、輔助線或 factoids），都將用來判斷是否支援字串。</span><span class="sxs-lookup"><span data-stu-id="3c009-105">Any restricting data, like wordlists, guides or factoids, in any corresponding hint node will be used to determine if the string is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c009-106">語法</span><span class="sxs-lookup"><span data-stu-id="3c009-106">Syntax</span></span>


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="3c009-107">參數</span><span class="sxs-lookup"><span data-stu-id="3c009-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c009-108">*bstrAlternateString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c009-108">*bstrAlternateString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c009-109">已辨識要驗證的字串。</span><span class="sxs-lookup"><span data-stu-id="3c009-109">Recognized string to verify.</span></span>

</dd> <dt>

<span data-ttu-id="3c009-110">*pfIsSupported* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3c009-110">*pfIsSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c009-111">**變異 \_** 如果 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)支援指定的字串，且已套用任何對應的提示節點，則為 TRUE;**變異 \_** 如果不支援，則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="3c009-111">**VARIANT\_TRUE** if the specified string is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; **VARIANT\_FALSE** if not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c009-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c009-112">Return value</span></span>

<span data-ttu-id="3c009-113">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="3c009-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c009-114">備註</span><span class="sxs-lookup"><span data-stu-id="3c009-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3c009-115">需求</span><span class="sxs-lookup"><span data-stu-id="3c009-115">Requirements</span></span>



| <span data-ttu-id="3c009-116">需求</span><span class="sxs-lookup"><span data-stu-id="3c009-116">Requirement</span></span> | <span data-ttu-id="3c009-117">值</span><span class="sxs-lookup"><span data-stu-id="3c009-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c009-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c009-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3c009-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c009-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3c009-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c009-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3c009-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="3c009-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3c009-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3c009-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c009-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="3c009-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3c009-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3c009-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c009-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c009-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3c009-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c009-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c009-127">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="3c009-127">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




