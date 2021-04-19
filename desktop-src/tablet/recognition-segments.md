---
description: 辨識區段是辨識器在內部用來產生特定筆墨物件之辨識結果的基本筆墨單位。
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: 辨識區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997944"
---
# <a name="recognition-segments"></a><span data-ttu-id="40e6f-103">辨識區段</span><span class="sxs-lookup"><span data-stu-id="40e6f-103">Recognition Segments</span></span>

<span data-ttu-id="40e6f-104">辨識區段是辨識器在內部用來產生特定筆墨物件之辨識結果的基本筆墨單位。</span><span class="sxs-lookup"><span data-stu-id="40e6f-104">A recognition segment is the basic ink unit that a recognizer uses internally to produce a recognition result for a particular Ink object.</span></span> <span data-ttu-id="40e6f-105">辨識區段是筆墨筆劃的集合。</span><span class="sxs-lookup"><span data-stu-id="40e6f-105">A recognition segment is a collection of ink strokes.</span></span> <span data-ttu-id="40e6f-106">例如，辨識器能夠辨識英文的手寫手寫，可能會使用單字作為基本辨識區段。</span><span class="sxs-lookup"><span data-stu-id="40e6f-106">For example, a recognizer that is capable of recognizing English cursive handwriting might use a word as the basic recognition segment.</span></span>

<span data-ttu-id="40e6f-107">其他辨識器可能會使用複合單字的一部分作為基本區段。</span><span class="sxs-lookup"><span data-stu-id="40e6f-107">Other recognizers may use parts of composite words as basic segments.</span></span> <span data-ttu-id="40e6f-108">例如，在西班牙文中，簡短的單字通常會結合以提供較長的複合字組。</span><span class="sxs-lookup"><span data-stu-id="40e6f-108">For example, in Spanish, short words are commonly combined to provide longer composite words.</span></span> <span data-ttu-id="40e6f-109">"Damelo" 是由三個字組 "da me lo" 組成的西班牙文， (給我) ，但它是以單一單字寫成。</span><span class="sxs-lookup"><span data-stu-id="40e6f-109">"Damelo" is a Spanish word that is composed of three words "da me lo" (give me that), but it is written as a single word.</span></span> <span data-ttu-id="40e6f-110">西班牙文辨識器可以將每個部分字組辨識為區段。</span><span class="sxs-lookup"><span data-stu-id="40e6f-110">A Spanish recognizer could recognize each subword as a segment.</span></span>

<span data-ttu-id="40e6f-111">辨識器可能會發現數種將筆墨範例分成辨識區段的方式。</span><span class="sxs-lookup"><span data-stu-id="40e6f-111">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="40e6f-112">由於辨識使用者的預期輸入需要混淆，因此辨識器可能會傳回許多替代相符專案。</span><span class="sxs-lookup"><span data-stu-id="40e6f-112">Because ambiguity is involved in recognizing the user's intended input, the recognizer can return many alternate matches.</span></span>

<span data-ttu-id="40e6f-113">如需替代項的詳細資訊，請參閱 [替代](alternates.md)。</span><span class="sxs-lookup"><span data-stu-id="40e6f-113">For more information about alternates, see [Alternates](alternates.md).</span></span>

 

 



