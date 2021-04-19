---
description: 建立 ICoNtextNodes 物件。
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'IInkAnalyzer：： CreateCoNtextNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998070"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a><span data-ttu-id="c1c54-103">IInkAnalyzer：： CreateCoNtextNodes 方法</span><span class="sxs-lookup"><span data-stu-id="c1c54-103">IInkAnalyzer::CreateContextNodes method</span></span>

<span data-ttu-id="c1c54-104">建立 [**ICoNtextNodes**](icontextnodes.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c1c54-104">Creates an [**IContextNodes**](icontextnodes.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c54-105">語法</span><span class="sxs-lookup"><span data-stu-id="c1c54-105">Syntax</span></span>


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="c1c54-106">參數</span><span class="sxs-lookup"><span data-stu-id="c1c54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c54-107">*ppCoNtextNodes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1c54-107">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c54-108">[**ICoNtextNodes**](icontextnodes.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c1c54-108">A pointer to the [**IContextNodes**](icontextnodes.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c54-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1c54-109">Return value</span></span>

<span data-ttu-id="c1c54-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c1c54-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c1c54-111">備註</span><span class="sxs-lookup"><span data-stu-id="c1c54-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c1c54-112">若要避免記憶體流失，請在 *ppCoNtextNodes* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="c1c54-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodes* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="c1c54-113">您可以使用這個方法來建立與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的空 [**ICoNtextNodes**](icontextnodes.md)集合。</span><span class="sxs-lookup"><span data-stu-id="c1c54-113">Use this method to create an empty [**IContextNodes**](icontextnodes.md) collection that is associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="c1c54-114">新的 **ICoNtextNodes** 集合不是 **IInkAnalyzer** 物件的內容樹狀結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="c1c54-114">The new **IContextNodes** collection is not part of the **IInkAnalyzer** object's context tree.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1c54-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1c54-115">Requirements</span></span>



| <span data-ttu-id="c1c54-116">需求</span><span class="sxs-lookup"><span data-stu-id="c1c54-116">Requirement</span></span> | <span data-ttu-id="c1c54-117">值</span><span class="sxs-lookup"><span data-stu-id="c1c54-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c54-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1c54-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c54-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1c54-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c1c54-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1c54-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c54-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="c1c54-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c1c54-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c1c54-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c54-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c1c54-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c1c54-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c1c54-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1c54-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1c54-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c1c54-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1c54-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c54-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c1c54-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c1c54-128">**ICoNtextNodes**</span><span class="sxs-lookup"><span data-stu-id="c1c54-128">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="c1c54-129">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c1c54-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

