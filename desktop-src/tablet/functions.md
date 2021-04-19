---
description: 本章節包含 Tablet PC 的核心功能。
ms.assetid: 8f94a82c-de93-4649-a9b5-0adcbe01333d
title: 核心 Tablet PC 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9d0369a223959f011612b5aefc820a3668eeff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998457"
---
# <a name="core-tablet-pc-functions"></a><span data-ttu-id="d3786-103">核心 Tablet PC 功能</span><span class="sxs-lookup"><span data-stu-id="d3786-103">Core Tablet PC Functions</span></span>

<span data-ttu-id="d3786-104">本章節包含 Tablet PC 的核心功能。</span><span class="sxs-lookup"><span data-stu-id="d3786-104">This section contains the core functions for Tablet PC.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d3786-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="d3786-105">In This Section</span></span>



| <span data-ttu-id="d3786-106">函式</span><span class="sxs-lookup"><span data-stu-id="d3786-106">Function</span></span>                                                         | <span data-ttu-id="d3786-107">描述</span><span class="sxs-lookup"><span data-stu-id="d3786-107">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3786-108">**AddOneStroke**</span><span class="sxs-lookup"><span data-stu-id="d3786-108">**AddOneStroke**</span></span>](addonestroke.md)                             | <span data-ttu-id="d3786-109">將新的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件加入至傳入的 [**InkDivider**](inkdivider-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d3786-109">Adds a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to the [**InkDivider**](inkdivider-class.md) object that was passed in.</span></span>                                                                 |
| [<span data-ttu-id="d3786-110">**CallDivide**</span><span class="sxs-lookup"><span data-stu-id="d3786-110">**CallDivide**</span></span>](calldivide.md)                                 | <span data-ttu-id="d3786-111">從 [**InkDivider**](inkdivider-class.md) 物件中取出分析資訊。</span><span class="sxs-lookup"><span data-stu-id="d3786-111">Retrieves analysis information from the [**InkDivider**](inkdivider-class.md) object.</span></span>                                                                                                              |
| [<span data-ttu-id="d3786-112">**CallDivideResults**</span><span class="sxs-lookup"><span data-stu-id="d3786-112">**CallDivideResults**</span></span>](calldivideresults.md)                   | <span data-ttu-id="d3786-113">傳回 [**InkDivider**](inkdivider-class.md) 物件的分析結果。</span><span class="sxs-lookup"><span data-stu-id="d3786-113">Returns analysis results from the [**InkDivider**](inkdivider-class.md) object.</span></span>                                                                                                                    |
| [<span data-ttu-id="d3786-114">**CallDivideResultsStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="d3786-114">**CallDivideResultsStrokeIds**</span></span>](calldivideresultsstrokeids.md) | <span data-ttu-id="d3786-115">抓取筆墨分析所決定之對應單字、線條、段落或繪圖的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性。</span><span class="sxs-lookup"><span data-stu-id="d3786-115">Retrieves the [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects of the corresponding word, line, paragraph, or drawing determined by ink analysis.</span></span> |
| [<span data-ttu-id="d3786-116">**CreateInkDivider**</span><span class="sxs-lookup"><span data-stu-id="d3786-116">**CreateInkDivider**</span></span>](createinkdivider.md)                     | <span data-ttu-id="d3786-117">具現化 [**InkDivider**](inkdivider-class.md) 介面的執行，並傳回其控制碼。</span><span class="sxs-lookup"><span data-stu-id="d3786-117">Instantiates an implementation of the [**InkDivider**](inkdivider-class.md) interface and returns its handle.</span></span>                                                                                      |
| [<span data-ttu-id="d3786-118">**DeleteInkDivider**</span><span class="sxs-lookup"><span data-stu-id="d3786-118">**DeleteInkDivider**</span></span>](deleteinkdivider.md)                     | <span data-ttu-id="d3786-119">刪除 [**InkDivider**](inkdivider-class.md) 物件，並釋放相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="d3786-119">Deletes an [**InkDivider**](inkdivider-class.md) object and releases associated resources.</span></span>                                                                                                         |
| [<span data-ttu-id="d3786-120">**InvokeIDispatch**</span><span class="sxs-lookup"><span data-stu-id="d3786-120">**InvokeIDispatch**</span></span>](invokeidispatch.md)                       | <span data-ttu-id="d3786-121">叫用 IDispatch 介面的 helper 功能。</span><span class="sxs-lookup"><span data-stu-id="d3786-121">Invokes helper functionality for the IDispatch interface.</span></span>                                                                                                                                           |
| [<span data-ttu-id="d3786-122">**RecognizerCoNtextSet**</span><span class="sxs-lookup"><span data-stu-id="d3786-122">**RecognizerContextSet**</span></span>](recognizercontextset.md)             | <span data-ttu-id="d3786-123">測試 [**InkDivider**](inkdivider-class.md) 物件是否可以使用 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 類別來分析文字。</span><span class="sxs-lookup"><span data-stu-id="d3786-123">Tests whether the [**InkDivider**](inkdivider-class.md) object can use the [**InkRecognizerContext**](inkrecognizercontext-class.md) class to analyze words.</span></span>                                      |
| [<span data-ttu-id="d3786-124">**RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="d3786-124">**RemoveStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-removestrokes)                | <span data-ttu-id="d3786-125">從 [**InkDivider**](inkdivider-class.md)移除 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件。</span><span class="sxs-lookup"><span data-stu-id="d3786-125">Removes [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects from the [**InkDivider**](inkdivider-class.md).</span></span>                                                                                           |
| [<span data-ttu-id="d3786-126">**SetLineHeight**</span><span class="sxs-lookup"><span data-stu-id="d3786-126">**SetLineHeight**</span></span>](setlineheight.md)                           | <span data-ttu-id="d3786-127">在 [**InkDivider**](inkdivider-class.md)物件上設定 [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)屬性。</span><span class="sxs-lookup"><span data-stu-id="d3786-127">Sets the [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property on the [**InkDivider**](inkdivider-class.md) object.</span></span>                                                                                 |
| [<span data-ttu-id="d3786-128">**SetLineRecoCallback**</span><span class="sxs-lookup"><span data-stu-id="d3786-128">**SetLineRecoCallback**</span></span>](setlinerecocallback.md)               | <span data-ttu-id="d3786-129">設定要在行辨識期間使用的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="d3786-129">Sets a callback function to be used during line recognition.</span></span>                                                                                                                                        |



 

 

 
