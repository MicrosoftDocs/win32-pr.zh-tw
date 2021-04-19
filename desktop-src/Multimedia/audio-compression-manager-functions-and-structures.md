---
title: 音訊壓縮管理員函式和結構
description: 音訊壓縮管理員函式和結構
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- 多媒體音訊、正常運作
- 音訊、等式函數
- 音訊壓縮管理員 (的功能) 、函式
- " (音訊壓縮管理員) 、函式、功能"
- 多媒體音訊、進行中的結構
- 音訊、進行中的結構
- 音訊壓縮管理員 (的) 、結構
- " (音效壓縮管理員) 、結構"
- 進行中結構
- 進行的函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969512"
---
# <a name="audio-compression-manager-functions-and-structures"></a><span data-ttu-id="70d82-113">音訊壓縮管理員函式和結構</span><span class="sxs-lookup"><span data-stu-id="70d82-113">Audio Compression Manager Functions and Structures</span></span>

<span data-ttu-id="70d82-114">執行的函式分成數個類別。</span><span class="sxs-lookup"><span data-stu-id="70d82-114">The ACM functions fall into several categories.</span></span> <span data-ttu-id="70d82-115">函數的命名慣例可讓您輕鬆地識別這些類別。</span><span class="sxs-lookup"><span data-stu-id="70d82-115">Naming conventions for the functions make it easy to identify these categories.</span></span> <span data-ttu-id="70d82-116">函式名稱 (有兩個例外狀況) 的形式為 *acmGroupFunction*，其中 *Group* 會指定 ([FormatTag]、[格式]、[]、[篩選]、[FilterTag] 或 [資料流程] ) *，且函* 式會描述函式所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="70d82-116">Function names (with two exceptions) are of the form *acmGroupFunction*, where *Group* designates the ACM category (such as "Driver," "Format," "FormatTag," "Filter," "FilterTag," or "Stream"), and *Function* describes the action performed by the function.</span></span>

<span data-ttu-id="70d82-117">篩選和格式群組中的函數非常類似。</span><span class="sxs-lookup"><span data-stu-id="70d82-117">The functions in the filter and format groups are very similar.</span></span> <span data-ttu-id="70d82-118">幾乎每個在篩選上作用的函式都有平行函式，可針對格式進行作用。</span><span class="sxs-lookup"><span data-stu-id="70d82-118">Almost every function that acts on filters has a parallel function that acts on formats.</span></span>

<span data-ttu-id="70d82-119">在 format 群組中，某些函式會使用波形-音訊格式標記 ([**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)) 結構的 **wFormatTag** 成員，而其他函式則需要完整的波形音訊格式 (完整的 **WAVEFORMATEX** 結構) 。</span><span class="sxs-lookup"><span data-stu-id="70d82-119">In the format group, some functions use waveform-audio format tags (the **wFormatTag** member of a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure) while others require full waveform-audio formats (the full **WAVEFORMATEX** structure).</span></span> <span data-ttu-id="70d82-120"> (如需 **WAVEFORMATEX** 結構的參考資訊，請參閱 [錯誤](error.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="70d82-120">(For reference information about the **WAVEFORMATEX** structure, see [Error](error.md).)</span></span>

<span data-ttu-id="70d82-121">在篩選群組中，某些函式會使用波形-音訊篩選標記 ([**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter)) 結構的 **dwFilterTag** 成員，而其他函式則需要完整的波形音訊篩選 (完整的 **WAVEFILTER** 結構) 。</span><span class="sxs-lookup"><span data-stu-id="70d82-121">In the filter group, some functions use waveform-audio filter tags (the **dwFilterTag** member of a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure), while others require full waveform-audio filters (the full **WAVEFILTER** structure).</span></span>

<span data-ttu-id="70d82-122">資料流程群組中的函式代表與轉換有關的許多步驟：開啟轉換實例、準備轉換、執行轉換、在轉換完成之後清除，以及關閉轉換實例。</span><span class="sxs-lookup"><span data-stu-id="70d82-122">The functions in the stream group represent the many steps involved in a conversion: opening a conversion instance, preparing for the conversion, performing the conversion, cleaning up after the conversion is complete, and closing the conversion instance.</span></span>

 

 