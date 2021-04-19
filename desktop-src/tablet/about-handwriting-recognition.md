---
description: Tablet PC 包含的技術可辨識最常用於手寫形式的筆墨輸入。
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: 關於手寫辨識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985147"
---
# <a name="about-handwriting-recognition"></a><span data-ttu-id="6f964-103">關於手寫辨識</span><span class="sxs-lookup"><span data-stu-id="6f964-103">About Handwriting Recognition</span></span>

<span data-ttu-id="6f964-104">Tablet PC 包含的技術可辨識最常用於手寫形式的筆墨輸入。</span><span class="sxs-lookup"><span data-stu-id="6f964-104">Tablet PC includes technology for recognizing ink input that is most commonly in the form of handwriting.</span></span> <span data-ttu-id="6f964-105">提供辨識的軟體模組稱為辨識器。</span><span class="sxs-lookup"><span data-stu-id="6f964-105">The software module that provides the recognition is called a recognizer.</span></span> <span data-ttu-id="6f964-106">辨識器會辨識一種語言、一組相關的語言，或相關物件（例如，音樂筆記、系統手勢或幾何圖形）的類別。</span><span class="sxs-lookup"><span data-stu-id="6f964-106">A recognizer recognizes one language, a group of related languages, or a class of related objects such as musical notes, system gestures, or geometric shapes.</span></span> <span data-ttu-id="6f964-107">您可以動態地將辨識器新增至 ink 服務系統。</span><span class="sxs-lookup"><span data-stu-id="6f964-107">You can dynamically add recognizers to the ink services system.</span></span>

## <a name="recognition-steps"></a><span data-ttu-id="6f964-108">辨識步驟</span><span class="sxs-lookup"><span data-stu-id="6f964-108">Recognition Steps</span></span>

<span data-ttu-id="6f964-109">辨識會透過使用辨識器內容來處理。</span><span class="sxs-lookup"><span data-stu-id="6f964-109">Recognition is handled through the use of a recognizer context.</span></span> <span data-ttu-id="6f964-110">辨識包含四個基本步驟：</span><span class="sxs-lookup"><span data-stu-id="6f964-110">Recognition consists of four basic steps:</span></span>

1.  <span data-ttu-id="6f964-111">設定辨識條件約束的依據：</span><span class="sxs-lookup"><span data-stu-id="6f964-111">Setting up the recognition constraints by:</span></span>
    -   <span data-ttu-id="6f964-112">選取 (幾何條件約束) 的辨識器和輸入模式。</span><span class="sxs-lookup"><span data-stu-id="6f964-112">Selecting the recognizer and input mode (geometric constraints).</span></span>
    -   <span data-ttu-id="6f964-113">設定語言條件約束。</span><span class="sxs-lookup"><span data-stu-id="6f964-113">Setting the language constraints.</span></span> <span data-ttu-id="6f964-114">例如，您可以將輸入限制為英數位元，也可以傳遞架構來協助辨識器。</span><span class="sxs-lookup"><span data-stu-id="6f964-114">For example, you can restrict input to alphanumeric characters or you can pass schemas to assist the recognizer.</span></span>
2.  <span data-ttu-id="6f964-115">將筆墨傳送到辨識器。</span><span class="sxs-lookup"><span data-stu-id="6f964-115">Sending ink to the recognizer.</span></span>
3.  <span data-ttu-id="6f964-116">處理輸入 (辨識) 。</span><span class="sxs-lookup"><span data-stu-id="6f964-116">Processing the input (recognizing).</span></span>
4.  <span data-ttu-id="6f964-117">傳回識別的結果。</span><span class="sxs-lookup"><span data-stu-id="6f964-117">Returning the results of the recognition.</span></span>

<span data-ttu-id="6f964-118">步驟2和3可能會在迴圈中重複，或在嘗試辨識之前，將所有筆墨筆劃新增至筆墨。</span><span class="sxs-lookup"><span data-stu-id="6f964-118">Steps 2 and 3 may be repeated in a loop, or all of the ink strokes may be added to the ink before recognition is attempted.</span></span>

## <a name="samples-and-related-topics"></a><span data-ttu-id="6f964-119">範例和相關主題</span><span class="sxs-lookup"><span data-stu-id="6f964-119">Samples and Related Topics</span></span>

<span data-ttu-id="6f964-120">[Advanced 辨識範例](advanced-recognition-sample.md) 示範如何搭配使用辨識器與 [**ink**](inkdisp-class.md) 物件來執行筆跡辨識。</span><span class="sxs-lookup"><span data-stu-id="6f964-120">[Advanced Recognition Sample](advanced-recognition-sample.md) demonstrates how to use recognizers with [**Ink**](inkdisp-class.md) objects to perform ink recognition.</span></span>

<span data-ttu-id="6f964-121">辨識[器 Dll 範例範本](recognizer-dll-sample-template.md)包含用來建立辨識器 dll 的範本。</span><span class="sxs-lookup"><span data-stu-id="6f964-121">[Recognizer DLL Sample Template](recognizer-dll-sample-template.md) contains a template for creating a recognizer DLL.</span></span> <span data-ttu-id="6f964-122">範本包含用來註冊和取消註冊伺服器的功能，以及主要辨識器函式的骨架。</span><span class="sxs-lookup"><span data-stu-id="6f964-122">The template contains functions for registering and unregistering the server, as well as skeletons for primary recognizer functions.</span></span>

<span data-ttu-id="6f964-123">下列各節說明 Tablet PC 辨識技術背後的基本概念。</span><span class="sxs-lookup"><span data-stu-id="6f964-123">The following sections describe the basic concepts behind the Tablet PC recognition technology.</span></span> <span data-ttu-id="6f964-124">如需建立自訂辨識器的詳細資訊，請參閱 [建立辨識器](creating-a-recognizer.md)。</span><span class="sxs-lookup"><span data-stu-id="6f964-124">For detailed information about creating custom recognizers, see [Creating a Recognizer](creating-a-recognizer.md).</span></span>

-   [<span data-ttu-id="6f964-125">文字辨識器</span><span class="sxs-lookup"><span data-stu-id="6f964-125">Text Recognizers</span></span>](text-recognizers.md)
-   [<span data-ttu-id="6f964-126">物件辨識器</span><span class="sxs-lookup"><span data-stu-id="6f964-126">Object Recognizers</span></span>](object-recognizers.md)
-   [<span data-ttu-id="6f964-127">使用辨識器集合</span><span class="sxs-lookup"><span data-stu-id="6f964-127">Using the Recognizers Collection</span></span>](using-the-recognizers-collection.md)
-   [<span data-ttu-id="6f964-128">辨識器內容</span><span class="sxs-lookup"><span data-stu-id="6f964-128">Recognizer Context</span></span>](recognizer-context.md)
-   [<span data-ttu-id="6f964-129">辨識區段</span><span class="sxs-lookup"><span data-stu-id="6f964-129">Recognition Segments</span></span>](recognition-segments.md)
-   [<span data-ttu-id="6f964-130">角度文字的辨識</span><span class="sxs-lookup"><span data-stu-id="6f964-130">Recognition of Angled Text</span></span>](recognition-of-angled-text.md)
-   [<span data-ttu-id="6f964-131">辨識器筆觸重新排序支援</span><span class="sxs-lookup"><span data-stu-id="6f964-131">Recognizer Stroke Reordering Support</span></span>](recognizer-stroke-reordering-support.md)
-   [<span data-ttu-id="6f964-132">字典和 Factoids</span><span class="sxs-lookup"><span data-stu-id="6f964-132">Dictionaries and Factoids</span></span>](dictionaries-and-factoids.md)
-   <span data-ttu-id="6f964-133">[關於辨識的信賴財產 \[\]](confidence-property--about-recognition.md)</span><span class="sxs-lookup"><span data-stu-id="6f964-133">[Confidence Property \[About Recognition\]](confidence-property--about-recognition.md)</span></span>
-   [<span data-ttu-id="6f964-134">替代項目</span><span class="sxs-lookup"><span data-stu-id="6f964-134">Alternates</span></span>](alternates.md)
-   [<span data-ttu-id="6f964-135">筆跡區段和替代項</span><span class="sxs-lookup"><span data-stu-id="6f964-135">Ink Segments and Alternates</span></span>](ink-segments-and-alternates.md)

 

 



