---
description: 分割物件會使用 RecognizerCoNtext 來改善其辨識區段的分析，並產生手寫元素的辨識文字。
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: 使用辨識器內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026297"
---
# <a name="working-with-a-recognizer-context"></a><span data-ttu-id="b083c-103">使用辨識器內容</span><span class="sxs-lookup"><span data-stu-id="b083c-103">Working with a Recognizer Context</span></span>

<span data-ttu-id="b083c-104">[**分割**](inkdivider-class.md)物件會使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md)來改善其辨識區段的分析，並產生手寫元素的辨識文字。</span><span class="sxs-lookup"><span data-stu-id="b083c-104">The [**Divider**](inkdivider-class.md) object uses a [**RecognizerContext**](inkrecognizercontext-class.md) to improve its analysis of recognition segments and to generate recognition text for handwriting elements.</span></span>

<span data-ttu-id="b083c-105">您可以使用 [**分隔**](inkdivider-class.md)物件的 [**RecognizerCoNtext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)屬性，或在 managed 程式碼) 的 ([分割](/previous-versions/ms839465(v=msdn.10))函式的呼叫中提供辨識器內容，來設定辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="b083c-105">You can set the recognizer context by using the [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property of the [**Divider**](inkdivider-class.md) object or by supplying the recognizer context in the call to the [Divider](/previous-versions/ms839465(v=msdn.10)) constructor (in managed code).</span></span> <span data-ttu-id="b083c-106">如果非手寫辨識器的辨識器內容，或不支援「免費輸入」功能的辨識器內容指派給 **RecognizerCoNtext** 屬性，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b083c-106">If a recognizer context for a non-handwriting recognizer or for a recognizer that does not support the free input capability is assigned to the **RecognizerContext** property, then an exception is thrown.</span></span>

<span data-ttu-id="b083c-107">如果未安裝辨識器，或未將辨識器內容指派給 [**分割**](inkdivider-class.md) 物件，則 **分隔** 物件不會使用辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="b083c-107">If recognizers are not installed or a recognizer context is not assigned to the [**Divider**](inkdivider-class.md) object, the **Divider** object does not use a recognizer context.</span></span> <span data-ttu-id="b083c-108">在此情況下，版面配置分析功能會執行區段分割，而且沒有任何文字與 [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="b083c-108">In this case, the layout analysis feature performs the segment division, and no text is associated with the [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

> [!Note]  
> <span data-ttu-id="b083c-109">將筆劃指派給 [**分隔**](inkdivider-class.md)物件之後，就無法變更 [**RecognizerCoNtext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)屬性。</span><span class="sxs-lookup"><span data-stu-id="b083c-109">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property cannot be changed after strokes have been assigned to the [**Divider**](inkdivider-class.md) object.</span></span> <span data-ttu-id="b083c-110">**分隔** 物件會使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的預設屬性值。</span><span class="sxs-lookup"><span data-stu-id="b083c-110">The **Divider** object uses the default property values of the [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="b083c-111">[**分割**](inkdivider-class.md)物件會在版面配置分析期間，將辨識器內容套用至手寫元素。</span><span class="sxs-lookup"><span data-stu-id="b083c-111">The [**Divider**](inkdivider-class.md) object applies the recognizer context to handwritten elements during layout analysis.</span></span> <span data-ttu-id="b083c-112">**分割** 物件會忽略您直接指派給辨識器內容的任何筆觸。</span><span class="sxs-lookup"><span data-stu-id="b083c-112">Any strokes you assign directly to the recognizer context are ignored by the **Divider** object.</span></span> <span data-ttu-id="b083c-113">如需文字辨識的詳細資訊，請參閱 [關於手寫辨識](about-handwriting-recognition.md)。</span><span class="sxs-lookup"><span data-stu-id="b083c-113">For more information about text recognition, see [About Handwriting Recognition](about-handwriting-recognition.md).</span></span>

 

 
