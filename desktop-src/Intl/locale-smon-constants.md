---
description: 地區設定 \_ SMON \* 常數
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: LOCALE_SMON * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969264"
---
# <a name="locale_smon-constants"></a><span data-ttu-id="e745d-103">地區設定 \_ SMON \* 常數</span><span class="sxs-lookup"><span data-stu-id="e745d-103">LOCALE\_SMON\* Constants</span></span>

<span data-ttu-id="e745d-104">本主題定義 \_ \* NLS 用來表示貨幣值的地區設定 SMON 常數。</span><span class="sxs-lookup"><span data-stu-id="e745d-104">This topic defines the LOCALE\_SMON\* constants used by NLS in representing monetary values.</span></span>



| <span data-ttu-id="e745d-105">值</span><span class="sxs-lookup"><span data-stu-id="e745d-105">Value</span></span>                   | <span data-ttu-id="e745d-106">意義</span><span class="sxs-lookup"><span data-stu-id="e745d-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e745d-107">地區設定 \_ SMONDECIMALSEP</span><span class="sxs-lookup"><span data-stu-id="e745d-107">LOCALE\_SMONDECIMALSEP</span></span>  | <span data-ttu-id="e745d-108">字元 (s) 用來作為貨幣小數分隔符號。</span><span class="sxs-lookup"><span data-stu-id="e745d-108">Character(s) used as the monetary decimal separator.</span></span> <span data-ttu-id="e745d-109">此字串允許的最大字元數為四個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="e745d-109">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="e745d-110">例如，如果貨幣金額顯示為 "$3.40"，就像「三元和40美分」會顯示在美國，而貨幣小數分隔符號則是 "."。</span><span class="sxs-lookup"><span data-stu-id="e745d-110">For example, if a monetary amount is displayed as "$3.40", just as "three dollars and forty cents" is displayed in the United States, then the monetary decimal separator is ".".</span></span>                                                                                                                                             |
| <span data-ttu-id="e745d-111">地區設定 \_ SMONGROUPING</span><span class="sxs-lookup"><span data-stu-id="e745d-111">LOCALE\_SMONGROUPING</span></span>    | <span data-ttu-id="e745d-112">小數點左邊每個貨幣位數群組的大小。</span><span class="sxs-lookup"><span data-stu-id="e745d-112">Sizes for each group of monetary digits to the left of the decimal.</span></span> <span data-ttu-id="e745d-113">此字串允許的最大字元數為十個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="e745d-113">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="e745d-114">每個群組都需要明確的大小，且大小會以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="e745d-114">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="e745d-115">如果最後一個值為0，則會重複上述值。</span><span class="sxs-lookup"><span data-stu-id="e745d-115">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="e745d-116">例如，若要將數以千計分組，請指定 3; 0。</span><span class="sxs-lookup"><span data-stu-id="e745d-116">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="e745d-117">印度文語言會將前一千分組，然後分組為數百。</span><span class="sxs-lookup"><span data-stu-id="e745d-117">Indic languages group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="e745d-118">例如12、34、56789是以3表示，2; 0。</span><span class="sxs-lookup"><span data-stu-id="e745d-118">For example 12,34,56,789 is represented by 3;2;0.</span></span> |
| <span data-ttu-id="e745d-119">地區設定 \_ SMONTHOUSANDSEP</span><span class="sxs-lookup"><span data-stu-id="e745d-119">LOCALE\_SMONTHOUSANDSEP</span></span> | <span data-ttu-id="e745d-120">字元 (s) 用來作為小數點左邊數位群組之間的貨幣分隔符號。</span><span class="sxs-lookup"><span data-stu-id="e745d-120">Character(s) used as the monetary separator between groups of digits to the left of the decimal.</span></span> <span data-ttu-id="e745d-121">此字串允許的最大字元數為四個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="e745d-121">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="e745d-122">一般而言，這些群組代表上千個。</span><span class="sxs-lookup"><span data-stu-id="e745d-122">Typically, the groups represent thousands.</span></span> <span data-ttu-id="e745d-123">不過，根據針對地區設定 SMONGROUPING 所指定的值 \_ ，它們可以代表其他內容。</span><span class="sxs-lookup"><span data-stu-id="e745d-123">However, depending on the value specified for LOCALE\_SMONGROUPING, they can represent something else.</span></span>                                                                                                                                 |



 

 

 



