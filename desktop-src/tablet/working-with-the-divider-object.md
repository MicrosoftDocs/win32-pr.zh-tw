---
description: 分隔物件提供對 Tablet PC 版面配置分析功能的存取。
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: 使用分隔物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd158f85d368d764bce17e8b481ebe625a4d6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970981"
---
# <a name="working-with-the-divider-object"></a><span data-ttu-id="a0789-103">使用分隔物件</span><span class="sxs-lookup"><span data-stu-id="a0789-103">Working with the Divider Object</span></span>

<span data-ttu-id="a0789-104">[分隔](/previous-versions/ms583616(v=vs.100))物件提供對 Tablet PC 版面配置分析功能的存取。</span><span class="sxs-lookup"><span data-stu-id="a0789-104">The [Divider](/previous-versions/ms583616(v=vs.100)) object provides access to the Tablet PC layout analysis features.</span></span>

<span data-ttu-id="a0789-105">在 managed 程式碼中，您可以呼叫其中一個[分隔](/previous-versions/ms839465(v=msdn.10))器函式來具現化[分割](/previous-versions/ms583616(v=vs.100))物件。</span><span class="sxs-lookup"><span data-stu-id="a0789-105">In managed code, the [Divider](/previous-versions/ms583616(v=vs.100)) object can be instantiated by calling one of the [Divider](/previous-versions/ms839465(v=msdn.10)) constructors.</span></span> <span data-ttu-id="a0789-106">在自動化中，這稱為 [**InkDivider**](inkdivider-class.md) 物件，可透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="a0789-106">In Automation, this is called the [**InkDivider**](inkdivider-class.md) object, and it can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="a0789-107">您可以藉由呼叫[分隔](/previous-versions/ms583616(v=vs.100))物件的[除法](/previous-versions/ms839461(v=msdn.10))方法，取得目前分析結果的快照。</span><span class="sxs-lookup"><span data-stu-id="a0789-107">You can obtain a snapshot of the current analysis result by calling the [Divide](/previous-versions/ms839461(v=msdn.10)) method of the [Divider](/previous-versions/ms583616(v=vs.100)) object.</span></span> <span data-ttu-id="a0789-108">分析結果會在 [DivisionResult](/previous-versions/ms839371(v=msdn.10)) 物件中傳回。</span><span class="sxs-lookup"><span data-stu-id="a0789-108">The analysis result is returned in a [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object.</span></span> <span data-ttu-id="a0789-109">每次您呼叫除法方法時，分界線物件就會建立 DivisionResult 物件。</span><span class="sxs-lookup"><span data-stu-id="a0789-109">Each time you call the Divide method, the Divider object creates a DivisionResult object.</span></span> <span data-ttu-id="a0789-110">如需 DivisionResult 物件的詳細資訊，請參閱 [使用 DivisionResult 物件](working-with-the-divisionresult-object.md)。</span><span class="sxs-lookup"><span data-stu-id="a0789-110">For more information about the DivisionResult object, see [Working with the DivisionResult Object](working-with-the-divisionresult-object.md).</span></span>

<span data-ttu-id="a0789-111">[分割](/previous-versions/ms583616(v=vs.100))物件所分析的[筆劃](/previous-versions/ms552701(v=vs.100))集合會包含在分隔物件的 [[筆觸](/previous-versions/ms839422(v=msdn.10))] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="a0789-111">The [Strokes](/previous-versions/ms552701(v=vs.100)) collection that the [Divider](/previous-versions/ms583616(v=vs.100)) object analyzes is contained in the [Strokes](/previous-versions/ms839422(v=msdn.10)) property of the Divider object.</span></span> <span data-ttu-id="a0789-112">當您在集合中加入或刪除時，分隔物件會動態分析筆劃集合。</span><span class="sxs-lookup"><span data-stu-id="a0789-112">The Divider object dynamically analyzes the Strokes collection as you add to or delete from the collection.</span></span> <span data-ttu-id="a0789-113">如需分割物件之 [筆觸] 屬性的詳細資訊，請參閱 [使用筆劃集合](working-with-a-strokes-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="a0789-113">For more information about the Strokes property of the Divider object, see [Working with a Strokes Collection](working-with-a-strokes-collection.md).</span></span>

<span data-ttu-id="a0789-114">[分割](/previous-versions/ms583616(v=vs.100))物件會使用辨識器內容來改善其辨識區段的分析，並產生手寫元素的辨識文字。</span><span class="sxs-lookup"><span data-stu-id="a0789-114">The [Divider](/previous-versions/ms583616(v=vs.100)) object uses a recognizer context to improve its analysis of recognition segments and to generate recognition text for handwriting elements.</span></span> <span data-ttu-id="a0789-115">您可以使用分隔物件的 [RecognizerCoNtext](/previous-versions/ms839415(v=msdn.10)) 屬性來設定辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="a0789-115">You can set the recognizer context by using the [RecognizerContext](/previous-versions/ms839415(v=msdn.10)) property of the Divider object.</span></span> <span data-ttu-id="a0789-116">將筆劃指派給分隔物件之後，就無法變更 RecognizerCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="a0789-116">The RecognizerContext property cannot be changed after strokes have been assigned to the Divider object.</span></span> <span data-ttu-id="a0789-117">如需分割物件之 RecognizerCoNtext 屬性的詳細資訊，請參閱 [使用辨識器內容](working-with-a-recognizer-context.md)。</span><span class="sxs-lookup"><span data-stu-id="a0789-117">For more information about the RecognizerContext property of the Divider object, see [Working with a Recognizer Context](working-with-a-recognizer-context.md).</span></span>

> [!Caution]  
> <span data-ttu-id="a0789-118">在 managed 程式碼中，您必須在此物件上呼叫 [Dispose](/previous-versions/ms839450(v=msdn.10)) 方法，才能使其超出範圍。</span><span class="sxs-lookup"><span data-stu-id="a0789-118">In managed code, you must call the [Dispose](/previous-versions/ms839450(v=msdn.10)) method on this object before it goes out of scope.</span></span> <span data-ttu-id="a0789-119">這個物件會維護非受控資源。</span><span class="sxs-lookup"><span data-stu-id="a0789-119">This object maintains non-managed resources.</span></span> <span data-ttu-id="a0789-120">依賴此物件的完成可能會導致應用程式中的記憶體流失和例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a0789-120">Relying on finalization for this object can cause memory leaks and exceptions within your application.</span></span>

 

 

 
