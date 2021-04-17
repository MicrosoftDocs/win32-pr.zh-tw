---
description: 為了搭配 Windows Vista 和 Windows XP Tablet PC Edition 使用而建立的辨識器會使用一組結構，其中每個結構都稱為 >lattice，可將辨識結果傳遞回 Tablet PC 平臺程式庫。
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: 辨識器 >lattice 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bbfe71674571ae0554509dfa8477569ef8b44d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566202"
---
# <a name="recognizer-lattice-structure"></a><span data-ttu-id="9bd3e-103">辨識器 >lattice 結構</span><span class="sxs-lookup"><span data-stu-id="9bd3e-103">Recognizer Lattice Structure</span></span>

<span data-ttu-id="9bd3e-104">為了搭配 Windows Vista 和 Windows XP Tablet PC Edition 使用而建立的辨識器會使用一組結構，其中每個結構都稱為 >lattice，可將辨識結果傳遞回 Tablet PC 平臺程式庫。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-104">Recognizers created for use with Windows Vista and Windows XP Tablet PC Edition use a set of structures, each of which is called a lattice, to pass recognition results back to Tablet PC platform libraries.</span></span> <span data-ttu-id="9bd3e-105">Tablet PC 平臺接著會將這些結構中的資訊複製到 [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) 物件、 [**IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) 集合和 [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) 物件中。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-105">The Tablet PC platform then copies the information in these structures into the [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object, the [**IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) collection, and the [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object.</span></span>

<span data-ttu-id="9bd3e-106">當平臺呼叫 [HRECOCONTEXT](hrecocontext-handle.md)控制碼上的 [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)函式時，辨識器應該會傳回 >lattice 的指標。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-106">A pointer to the lattice should be returned by the recognizer when the platform calls the [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) function on the [HRECOCONTEXT](hrecocontext-handle.md) handle.</span></span>

<span data-ttu-id="9bd3e-107">本節將詳細說明 >lattice 結構。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-107">This section describes the lattice structure in detail.</span></span> <span data-ttu-id="9bd3e-108">如需辨識器和相關概念的總覽，請參閱 [關於手寫辨識](about-handwriting-recognition.md)。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-108">For an overview of recognizers and related concepts, see [About Handwriting Recognition](about-handwriting-recognition.md).</span></span>

## <a name="the-need-for-a-lattice"></a><span data-ttu-id="9bd3e-109">>lattice 的需求</span><span class="sxs-lookup"><span data-stu-id="9bd3e-109">The Need for a Lattice</span></span>

<span data-ttu-id="9bd3e-110">辨識器可能會有數種方式可將一組筆墨筆觸分成辨識區段。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-110">A recognizer may find several ways to break a set of ink strokes into recognition segments.</span></span> <span data-ttu-id="9bd3e-111">辨識器用來作為辨識區段的內容，取決於辨識器的類型。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-111">What the recognizer uses as a recognition segment depends upon the type of recognizer.</span></span> <span data-ttu-id="9bd3e-112">英文語言辨識器通常會使用單字作為辨識區段。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-112">English language recognizers typically use words as the recognition segment.</span></span> <span data-ttu-id="9bd3e-113">其他辨識器可能會使用字元、圖形或手勢作為辨識區段。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-113">Other recognizers might use characters, shapes, or gestures as the recognition segment.</span></span> <span data-ttu-id="9bd3e-114">>lattice 結構的彈性可讓您以邏輯方式管理大量的辨識結果，這些結果可結合在複雜的關聯性中。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-114">The flexibility of the lattice structures allows for logical management of the large number of recognition results that can be combined in complex relationships.</span></span>

<span data-ttu-id="9bd3e-115">就內部而言，辨識器會使用 >lattice 來保存指定筆墨的基本識別單位。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-115">Internally, recognizers use a lattice to hold basic recognition units for a given piece of ink.</span></span> <span data-ttu-id="9bd3e-116">>lattice 也會保留合併結果的分數或信賴等級。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-116">The lattice also holds the score, or confidence level, of the combined result.</span></span> <span data-ttu-id="9bd3e-117">此外，>lattice 會將區段對應儲存至原始筆墨筆劃。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-117">In addition, the lattice stores the mapping of segments to the original ink strokes.</span></span>

<span data-ttu-id="9bd3e-118">>lattice 結構定義于 RecTypes .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-118">The lattice structures are defined in the RecTypes.h header file.</span></span> <span data-ttu-id="9bd3e-119">>lattice 結構包含下列結構：</span><span class="sxs-lookup"><span data-stu-id="9bd3e-119">The lattice structures include the following structures:</span></span>

-   [<span data-ttu-id="9bd3e-120">**辨識 \_ >LATTICE**</span><span class="sxs-lookup"><span data-stu-id="9bd3e-120">**RECO\_LATTICE**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [<span data-ttu-id="9bd3e-121">**辨識 \_ >LATTICE 資料 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="9bd3e-121">**RECO\_LATTICE\_COLUMN**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [<span data-ttu-id="9bd3e-122">**辨識 \_ >LATTICE \_ 元素**</span><span class="sxs-lookup"><span data-stu-id="9bd3e-122">**RECO\_LATTICE\_ELEMENT**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [<span data-ttu-id="9bd3e-123">**辨識 \_ >LATTICE \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="9bd3e-123">**RECO\_LATTICE\_PROPERTIES**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [<span data-ttu-id="9bd3e-124">**辨識 \_ >LATTICE \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="9bd3e-124">**RECO\_LATTICE\_PROPERTY**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a><span data-ttu-id="9bd3e-125">>lattice 元件</span><span class="sxs-lookup"><span data-stu-id="9bd3e-125">Lattice Components</span></span>

<span data-ttu-id="9bd3e-126">下列範例會使用「一起」一字的筆觸，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-126">The following examples use the strokes for the word "together" as shown in the following image.</span></span> <span data-ttu-id="9bd3e-127">在範例中，會將區段評估為一或多個單字。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-127">In the examples, the segments are evaluated as one or more words.</span></span> <span data-ttu-id="9bd3e-128">數位代表要評估之區段中的個別筆劃。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-128">The numbers represent the individual strokes in the segment being evaluated.</span></span> <span data-ttu-id="9bd3e-129">請注意，每個 "t" 字元都包含兩個筆劃。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-129">Note that each of the "t" characters contains two strokes.</span></span>

!["合" 單字的筆劃](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

<span data-ttu-id="9bd3e-131">>lattice 是由一或多個資料行所組成，每個區段各一個資料行。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-131">A lattice is composed of one or more columns, one for each segment.</span></span> <span data-ttu-id="9bd3e-132">每個資料行依次包含一或多個元素。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-132">Each column in turn contains one or more elements.</span></span> <span data-ttu-id="9bd3e-133">專案會保留不同的辨識替代專案。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-133">An element holds a discrete recognition alternate.</span></span> <span data-ttu-id="9bd3e-134">如需資料行的詳細資訊，請參閱 [**辨識 \_ >lattice 資料 \_ 行**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) 結構。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-134">For more information about columns, see the [**RECO\_LATTICE\_COLUMN**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) structure.</span></span> <span data-ttu-id="9bd3e-135">如需元素的詳細資訊，請參閱 [**辨識 \_ >lattice \_ 元素**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element) 結構。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-135">For more information about elements, see the [**RECO\_LATTICE\_ELEMENT**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element) structure.</span></span>

<span data-ttu-id="9bd3e-136">評估上一個範例中所示的筆墨範例時，辨識器可能會傳回單一區段。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-136">The recognizer might return a single segment when evaluating the ink sample shown in the previous example.</span></span> <span data-ttu-id="9bd3e-137">在此情況下，>lattice 包含具有單一元素的單一資料行。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-137">In this case the lattice contains a single column with a single element.</span></span>

<span data-ttu-id="9bd3e-138">更複雜的範例會在辨識器評估筆墨樣本時自行呈現，並產生每個區段的多個區段和多個替代項。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-138">A more complex example presents itself when the recognizer evaluates the ink sample and comes up with multiple segments and multiple alternates for each segment.</span></span>

<span data-ttu-id="9bd3e-139">辨識替代項的數目可能會錯開，即使是小型筆墨範例也是如此。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-139">The number of recognition alternates may be staggering, even for a small ink sample.</span></span> <span data-ttu-id="9bd3e-140">例如，"t o g e t h e r" 可能產生下列結果：</span><span class="sxs-lookup"><span data-stu-id="9bd3e-140">For example, "t o g e t h e r" can yield the following results:</span></span>

-   <span data-ttu-id="9bd3e-141">「取得她」 (再加上每個字的替代專案) </span><span class="sxs-lookup"><span data-stu-id="9bd3e-141">"to get her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="9bd3e-142">「收集」 (再加上每個字組的替代項) </span><span class="sxs-lookup"><span data-stu-id="9bd3e-142">"to gather" (plus alternates for each word)</span></span>
-   <span data-ttu-id="9bd3e-143">「給她」 (再加上每個字的替換) </span><span class="sxs-lookup"><span data-stu-id="9bd3e-143">"to got her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="9bd3e-144">「一起」 (加上單字的替代項) </span><span class="sxs-lookup"><span data-stu-id="9bd3e-144">"together" (plus alternates for the word)</span></span>

<span data-ttu-id="9bd3e-145">在此情況下，辨識器可能會建立下列 >lattice 結構。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-145">In this case, a recognizer might create the following lattice structure.</span></span>

![「一起」一字的 >lattice 結構](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> <span data-ttu-id="9bd3e-147">每個資料行都有相同的筆劃順序，因為它們全都參考相同的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。</span><span class="sxs-lookup"><span data-stu-id="9bd3e-147">Each column shares the same stroke order because they all refer to the same [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

 

 

 
