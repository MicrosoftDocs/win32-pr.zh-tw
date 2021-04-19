---
description: 替代項是辨識區段的可能字組相符項。 辨識器會產生替代專案，並以字典或模擬的筆墨或音訊輸入可接受的相符專案作為基礎。
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: 替代項目
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350c9ac97f0af1451a0ded6445cf658dad4ee4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970350"
---
# <a name="alternates"></a><span data-ttu-id="e6750-104">替代項目</span><span class="sxs-lookup"><span data-stu-id="e6750-104">Alternates</span></span>

<span data-ttu-id="e6750-105">替代項是辨識區段的可能字組相符項。</span><span class="sxs-lookup"><span data-stu-id="e6750-105">An alternate is a potential word match for a recognition segment.</span></span> <span data-ttu-id="e6750-106">辨識器會產生替代專案，並以字典或模擬的筆墨或音訊輸入可接受的相符專案作為基礎。</span><span class="sxs-lookup"><span data-stu-id="e6750-106">A recognizer generates alternates and bases them on acceptable matches of the ink or audio input against a dictionary or factoid.</span></span>

> [!Note]  
> <span data-ttu-id="e6750-107">信賴評估目前僅適用于 Microsoft 英文 (美國) 和手勢辨識器。</span><span class="sxs-lookup"><span data-stu-id="e6750-107">Confidence evaluation is currently available only for the Microsoft English (United States) and gesture recognizers.</span></span>

 

<span data-ttu-id="e6750-108">有時筆墨在區段之間可能會有不明確的區別。</span><span class="sxs-lookup"><span data-stu-id="e6750-108">Sometimes the ink may have ambiguous distinctions between segments.</span></span> <span data-ttu-id="e6750-109">辨識器會比較這些區段與辨識器字典，以判斷可能的相符專案。</span><span class="sxs-lookup"><span data-stu-id="e6750-109">The recognizer compares these segments to a recognizer dictionary to determine possible matches.</span></span> <span data-ttu-id="e6750-110">當辨識器比較區段時，會維持一份可能的替代相符專案清單，並將信賴等級指派給每一個專案，以挑選最重要的選擇。</span><span class="sxs-lookup"><span data-stu-id="e6750-110">When the recognizer compares the segments, it maintains a list of possible alternate matches and assigns a confidence level to each one, picking a top choice.</span></span>

> [!Note]  
> <span data-ttu-id="e6750-111">辨識器無法針對小於辨識區段的筆墨提供替代部分。</span><span class="sxs-lookup"><span data-stu-id="e6750-111">The recognizer cannot provide alternates for a portion of ink that is smaller than a recognition segment.</span></span>

 

 

 



