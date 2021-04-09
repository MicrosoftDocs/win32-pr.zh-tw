---
description: 地區設定 \_ SGROUPING
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945503"
---
# <a name="locale_sgrouping"></a><span data-ttu-id="39332-103">地區設定 \_ SGROUPING</span><span class="sxs-lookup"><span data-stu-id="39332-103">LOCALE\_SGROUPING</span></span>

<span data-ttu-id="39332-104">小數點左邊每個位數群組的大小。</span><span class="sxs-lookup"><span data-stu-id="39332-104">Sizes for each group of digits to the left of the decimal.</span></span> <span data-ttu-id="39332-105">此字串允許的最大字元數為十個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="39332-105">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="39332-106">每個群組都需要明確的大小，且大小會以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="39332-106">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="39332-107">如果最後一個值為0，則會重複上述值。</span><span class="sxs-lookup"><span data-stu-id="39332-107">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="39332-108">例如，若要將數以千計分組，請指定 3; 0。</span><span class="sxs-lookup"><span data-stu-id="39332-108">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="39332-109">印度地區設定群組的前一千個群組，然後分組為數百。</span><span class="sxs-lookup"><span data-stu-id="39332-109">Indic locales group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="39332-110">例如，12、34、56789是以3表示，2; 0。</span><span class="sxs-lookup"><span data-stu-id="39332-110">For example, 12,34,56,789 is represented by 3;2;0.</span></span>

<span data-ttu-id="39332-111">其他範例：</span><span class="sxs-lookup"><span data-stu-id="39332-111">Further examples:</span></span>



| <span data-ttu-id="39332-112">規格</span><span class="sxs-lookup"><span data-stu-id="39332-112">Specification</span></span> | <span data-ttu-id="39332-113">產生的字串</span><span class="sxs-lookup"><span data-stu-id="39332-113">Resulting string</span></span>   |
|---------------|--------------------|
| <span data-ttu-id="39332-114">3; 0</span><span class="sxs-lookup"><span data-stu-id="39332-114">3;0</span></span>           | <span data-ttu-id="39332-115">3000000000000</span><span class="sxs-lookup"><span data-stu-id="39332-115">3,000,000,000,000</span></span>  |
| <span data-ttu-id="39332-116">3; 2; 0</span><span class="sxs-lookup"><span data-stu-id="39332-116">3;2;0</span></span>         | <span data-ttu-id="39332-117">30、00、00、00、00000</span><span class="sxs-lookup"><span data-stu-id="39332-117">30,00,00,00,00,000</span></span> |
| <span data-ttu-id="39332-118">3</span><span class="sxs-lookup"><span data-stu-id="39332-118">3</span></span>             | <span data-ttu-id="39332-119">3000000000000</span><span class="sxs-lookup"><span data-stu-id="39332-119">3000000000,000</span></span>     |
| <span data-ttu-id="39332-120">3; 2</span><span class="sxs-lookup"><span data-stu-id="39332-120">3;2</span></span>           | <span data-ttu-id="39332-121">30000000、00000</span><span class="sxs-lookup"><span data-stu-id="39332-121">30000000,00,000</span></span>    |



 

 

 



