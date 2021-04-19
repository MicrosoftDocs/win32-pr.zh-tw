---
description: 指出這個 ICoNtextNode 的已辨識字串來自系統字典、使用者字典或字組清單。
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'ICoNtextNode：： IsStringSupported 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972053"
---
# <a name="icontextnodeisstringsupported-method"></a><span data-ttu-id="0fcc7-103">ICoNtextNode：： IsStringSupported 方法</span><span class="sxs-lookup"><span data-stu-id="0fcc7-103">IContextNode::IsStringSupported method</span></span>

<span data-ttu-id="0fcc7-104">指出這個 [**ICoNtextNode**](icontextnode.md) 的已辨識字串來自系統字典、使用者字典或字組清單。</span><span class="sxs-lookup"><span data-stu-id="0fcc7-104">Indicates whether recognized string of this [**IContextNode**](icontextnode.md) came from the system dictionary, user dictionary, or word list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fcc7-105">語法</span><span class="sxs-lookup"><span data-stu-id="0fcc7-105">Syntax</span></span>


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="0fcc7-106">參數</span><span class="sxs-lookup"><span data-stu-id="0fcc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fcc7-107">*pfIsSupported* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="0fcc7-107">*pfIsSupported* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0fcc7-108">**變異 \_** 如果 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)支援此 [**ICoNtextNode**](icontextnode.md)的可辨識字串值，且已套用任何對應的提示節點，則為 TRUE。否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0fcc7-108">**VARIANT\_TRUE** if the recognized string value of this [**IContextNode**](icontextnode.md) is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fcc7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fcc7-109">Return value</span></span>

<span data-ttu-id="0fcc7-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="0fcc7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fcc7-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fcc7-111">Requirements</span></span>



| <span data-ttu-id="0fcc7-112">需求</span><span class="sxs-lookup"><span data-stu-id="0fcc7-112">Requirement</span></span> | <span data-ttu-id="0fcc7-113">值</span><span class="sxs-lookup"><span data-stu-id="0fcc7-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fcc7-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fcc7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0fcc7-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fcc7-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0fcc7-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fcc7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0fcc7-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="0fcc7-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0fcc7-118">標頭</span><span class="sxs-lookup"><span data-stu-id="0fcc7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fcc7-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="0fcc7-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0fcc7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0fcc7-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fcc7-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fcc7-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0fcc7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fcc7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fcc7-123">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="0fcc7-123">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




