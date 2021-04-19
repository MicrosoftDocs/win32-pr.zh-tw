---
description: 這個屬性會測量進度指標列的填滿程度。
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: 進度控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979398"
---
# <a name="progress-control-attribute"></a><span data-ttu-id="39f02-103">進度控制項屬性</span><span class="sxs-lookup"><span data-stu-id="39f02-103">Progress Control Attribute</span></span>

<span data-ttu-id="39f02-104">這個屬性會測量進度指標列的填滿程度。</span><span class="sxs-lookup"><span data-stu-id="39f02-104">This attribute measures how far the progress indicator bar is filled.</span></span> <span data-ttu-id="39f02-105">記錄包含兩個整數和一個字串。</span><span class="sxs-lookup"><span data-stu-id="39f02-105">The record contains two integers and a string.</span></span> <span data-ttu-id="39f02-106">第一個數位是進度，第二個數字是 (進度) 最大可能數目的範圍。</span><span class="sxs-lookup"><span data-stu-id="39f02-106">The first number is the progress, the second number is the range (the maximal possible number for the progress).</span></span> <span data-ttu-id="39f02-107">設定時，可以輸入整數位段或字串（包含整數）的整數。</span><span class="sxs-lookup"><span data-stu-id="39f02-107">On setting, the integers can be entered as integer fields or strings containing the integers.</span></span> <span data-ttu-id="39f02-108">如果遺漏第二個數字，則會假設為預設的 (1024) 。</span><span class="sxs-lookup"><span data-stu-id="39f02-108">If the second number is missing it is assumed to be the default (1024).</span></span> <span data-ttu-id="39f02-109">如果進度大於範圍，則會將它變更為範圍。</span><span class="sxs-lookup"><span data-stu-id="39f02-109">If the progress is larger than the range then it is changed to be the range.</span></span> <span data-ttu-id="39f02-110">第三個欄位是字串，即顯示其進度的動作名稱。</span><span class="sxs-lookup"><span data-stu-id="39f02-110">The third field is a string, the name of the action whose progress is displayed.</span></span>

<span data-ttu-id="39f02-111">如需相關資訊，請參閱 [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)，以及 [將自訂動作新增至 ProgressBar](adding-custom-actions-to-the-progressbar.md)。</span><span class="sxs-lookup"><span data-stu-id="39f02-111">For related information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md), and [Adding Custom Actions to the ProgressBar](adding-custom-actions-to-the-progressbar.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="39f02-112">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="39f02-112">Valid Controls</span></span>

[<span data-ttu-id="39f02-113">進度列</span><span class="sxs-lookup"><span data-stu-id="39f02-113">ProgressBar</span></span>](progressbar-control.md)

## <a name="associated-bit-flags"></a><span data-ttu-id="39f02-114">相關聯的位旗標</span><span class="sxs-lookup"><span data-stu-id="39f02-114">Associated Bit Flags</span></span>

<span data-ttu-id="39f02-115">這個屬性不會使用位旗標。</span><span class="sxs-lookup"><span data-stu-id="39f02-115">This attribute does not use bit flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="39f02-116">備註</span><span class="sxs-lookup"><span data-stu-id="39f02-116">Remarks</span></span>

<span data-ttu-id="39f02-117">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="39f02-117">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



