---
description: 除了辨識文字之外，辨識器還可以辨識相關物件的類別。
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: 物件辨識器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944783"
---
# <a name="object-recognizers"></a><span data-ttu-id="a7c3a-103">物件辨識器</span><span class="sxs-lookup"><span data-stu-id="a7c3a-103">Object Recognizers</span></span>

<span data-ttu-id="a7c3a-104">除了辨識文字之外，辨識器還可以辨識相關物件的類別。</span><span class="sxs-lookup"><span data-stu-id="a7c3a-104">In addition to recognizing text, recognizers can recognize a class of related objects.</span></span> <span data-ttu-id="a7c3a-105">物件辨識器會根據其用途辨識一般圖形。</span><span class="sxs-lookup"><span data-stu-id="a7c3a-105">Object recognizers recognize general shapes, according to their purpose.</span></span> <span data-ttu-id="a7c3a-106">物件辨識器可用來辨識：</span><span class="sxs-lookup"><span data-stu-id="a7c3a-106">Object recognizers are used to recognize:</span></span>

-   <span data-ttu-id="a7c3a-107">音符</span><span class="sxs-lookup"><span data-stu-id="a7c3a-107">Musical notes</span></span>
-   <span data-ttu-id="a7c3a-108">幾何圖形</span><span class="sxs-lookup"><span data-stu-id="a7c3a-108">Geometric shapes</span></span>
-   <span data-ttu-id="a7c3a-109">數學方公式</span><span class="sxs-lookup"><span data-stu-id="a7c3a-109">Math equations</span></span>
-   <span data-ttu-id="a7c3a-110">流程圖元素</span><span class="sxs-lookup"><span data-stu-id="a7c3a-110">Flow chart elements</span></span>

<span data-ttu-id="a7c3a-111">通常，這類辨識器可辨識的物件會在二維空間或功能的關聯性中。</span><span class="sxs-lookup"><span data-stu-id="a7c3a-111">Usually, the objects that are recognized by such a recognizer are in a two-dimensional spatial or functional relationship with each other.</span></span> <span data-ttu-id="a7c3a-112">例如，在數學方程式的複雜關聯性中，辨識器可以針對明確整數的上限傳回不同的結果，而非分數的分子。</span><span class="sxs-lookup"><span data-stu-id="a7c3a-112">For example, within the complex relationships in a math equation, a recognizer can return different results for an upper limit on a definite integral as opposed to a numerator in a fraction.</span></span>

<span data-ttu-id="a7c3a-113">因為這些關聯性的一般本質，所以很難定義一組可針對每個物件辨識器運作的介面。</span><span class="sxs-lookup"><span data-stu-id="a7c3a-113">Because of the very general nature of these relationships, it is extremely difficult to define the set of interfaces that will work for every object recognizer.</span></span>

<span data-ttu-id="a7c3a-114">Tablet PC 技術為 Managed 程式庫和自動化介面中的物件辨識器提供了基本的架構。</span><span class="sxs-lookup"><span data-stu-id="a7c3a-114">The Tablet PC Technology provides a basic framework for object recognizers in the Managed Library and Automation interfaces.</span></span> <span data-ttu-id="a7c3a-115">不過，您必須開發自訂介面，以說明每個物件辨識器可辨識之物件之間的複雜空間關聯性。</span><span class="sxs-lookup"><span data-stu-id="a7c3a-115">However, you must develop custom interfaces that describe complex spatial relationships between recognized objects for each object recognizer.</span></span> <span data-ttu-id="a7c3a-116">具體而言，在物件辨識器中，平臺會提供基本的 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件，以便將 [**筆墨**](inkdisp-class.md) 物件與辨識器內容建立關聯，以及呼叫辨識器來執行辨識。</span><span class="sxs-lookup"><span data-stu-id="a7c3a-116">Specifically, for object recognizers, the platform provides the basic [**RecognizerContext**](inkrecognizercontext-class.md) object for associating the [**Ink**](inkdisp-class.md) object with the recognizer context and for calling the recognizer to perform the recognition.</span></span>

 

 



