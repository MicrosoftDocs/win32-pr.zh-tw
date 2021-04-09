---
description: 抓取 ICoNtextNode 物件的集合，這些物件與指定之內容節點的指定文字範圍有關。
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'IInkAnalyzer：： GetNodesFromTextRange 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690583"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a><span data-ttu-id="b4861-103">IInkAnalyzer：： GetNodesFromTextRange 方法</span><span class="sxs-lookup"><span data-stu-id="b4861-103">IInkAnalyzer::GetNodesFromTextRange method</span></span>

<span data-ttu-id="b4861-104">抓取 [**ICoNtextNode**](icontextnode.md) 物件的集合，這些物件與指定之內容節點的指定文字範圍有關。</span><span class="sxs-lookup"><span data-stu-id="b4861-104">Retrieves a collection of [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4861-105">語法</span><span class="sxs-lookup"><span data-stu-id="b4861-105">Syntax</span></span>


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a><span data-ttu-id="b4861-106">參數</span><span class="sxs-lookup"><span data-stu-id="b4861-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4861-107">*plStart* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b4861-107">*plStart* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4861-108">在可辨識字串的 *pNodesToSearch* 部分中，文字範圍開頭的參考。</span><span class="sxs-lookup"><span data-stu-id="b4861-108">A reference to the start of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="b4861-109">*plLength* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b4861-109">*plLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4861-110">在可辨識字串的 *pNodesToSearch* 部分中，文字範圍長度的參考。</span><span class="sxs-lookup"><span data-stu-id="b4861-110">A reference to the length of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="b4861-111">*ppCoNtextNodes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b4861-111">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4861-112">與指定之內容節點的指定文字範圍相關之 [**ICoNtextNode**](icontextnode.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="b4861-112">A pointer to the [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

</dd> <dt>

<span data-ttu-id="b4861-113">*pNodesToSearch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4861-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4861-114">要限制搜尋的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b4861-114">The [**IContextNode**](icontextnode.md) objects to which to limit the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4861-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4861-115">Return value</span></span>

<span data-ttu-id="b4861-116">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b4861-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4861-117">備註</span><span class="sxs-lookup"><span data-stu-id="b4861-117">Remarks</span></span>

<span data-ttu-id="b4861-118">指定的文字範圍應該相對於 [**IInkAnalyzer**](iinkanalyzer.md)字串的 *pNodesToSearch* 部分，而不是整個 **IInkAnalyzer** 的可辨識字串。</span><span class="sxs-lookup"><span data-stu-id="b4861-118">The specified text range should be relative to the *pNodesToSearch* portion of the recognized string of the [**IInkAnalyzer**](iinkanalyzer.md), rather than to the recognized string of the entire **IInkAnalyzer**.</span></span>

<span data-ttu-id="b4861-119">這個方法會將文字範圍展開至最接近的單字界限，藉以修改 *plStart* 和 *plLength* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="b4861-119">This method modifies the values of the *plStart* and *plLength* parameters by expanding the text range to the nearest word boundaries.</span></span>

<span data-ttu-id="b4861-120">例如，如果可辨識的字串為 "I am"，而且您使用 *plStart* 的參數值來呼叫這個方法，並使用 *plLength* 的參數值（對應至「晚期」中的字母 "a"），這個方法會傳回包含單一 [**ICoNtextNode**](icontextnode.md)的集合，也就是對應至 "晚期" 這個字的 InkWord 或 TextWord。</span><span class="sxs-lookup"><span data-stu-id="b4861-120">For example, if the recognized string is "I am late" and you call this method using the parameter values of 6 for *plStart* and 1 for *plLength*, which corresponds to the letter "a" in "late", this method returns a collection containing a single [**IContextNode**](icontextnode.md), the InkWord or TextWord that corresponds to the word "late".</span></span> <span data-ttu-id="b4861-121">在此範例中，這個方法也會將 *plStart* 的值修改為5，並將 *plLength* 的值修改為對應至 "晚期" 這個字的4。</span><span class="sxs-lookup"><span data-stu-id="b4861-121">For this example, this method also modifies the value of *plStart* to 5 and the value of *plLength* to 4, which corresponds to the word "late".</span></span>

> [!Note]  
> <span data-ttu-id="b4861-122">*PlStart* 參數相對於 *pNodesToSearch* 參數的可辨識字串。</span><span class="sxs-lookup"><span data-stu-id="b4861-122">The *plStart* parameter is relative to the recognized string of the *pNodesToSearch* parameter.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b4861-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4861-123">Requirements</span></span>



| <span data-ttu-id="b4861-124">需求</span><span class="sxs-lookup"><span data-stu-id="b4861-124">Requirement</span></span> | <span data-ttu-id="b4861-125">值</span><span class="sxs-lookup"><span data-stu-id="b4861-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4861-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4861-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b4861-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4861-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4861-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4861-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b4861-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="b4861-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b4861-130">標頭</span><span class="sxs-lookup"><span data-stu-id="b4861-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4861-131"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b4861-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4861-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b4861-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4861-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4861-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b4861-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4861-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4861-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b4861-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




