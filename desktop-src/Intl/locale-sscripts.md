---
description: 地區設定 \_ SSCRIPTS
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970841"
---
# <a name="locale_sscripts"></a><span data-ttu-id="307b5-103">地區設定 \_ SSCRIPTS</span><span class="sxs-lookup"><span data-stu-id="307b5-103">LOCALE\_SSCRIPTS</span></span>

<span data-ttu-id="307b5-104">**Windows Vista 和更新版本：** 字串，代表腳本清單（使用 [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)中使用的4個字元標記法）。</span><span class="sxs-lookup"><span data-stu-id="307b5-104">**Windows Vista and later:** A string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="307b5-105">每個腳本名稱都是由四個拉丁字元所組成，且清單會依字母順序排列，並以每個名稱（包括最後）和分號。</span><span class="sxs-lookup"><span data-stu-id="307b5-105">Each script name consists of four Latin characters and the list is arranged in alphabetical order with each name, including the last, followed by a semicolon.</span></span>

<span data-ttu-id="307b5-106">您可以呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) ，並將 *LCType* 設定為 LOCALE \_ SSCRIPTS，作為策略的一部分，以降低 (IDNs) 的國際化功能變數名稱相關的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="307b5-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) can be called with *LCType* set to LOCALE\_SSCRIPTS as part of a strategy to mitigate security issues related to Internationalized Domain Names (IDNs).</span></span> <span data-ttu-id="307b5-107">以下是一些範例值：</span><span class="sxs-lookup"><span data-stu-id="307b5-107">Here are some example values:</span></span>



| <span data-ttu-id="307b5-108">Locale</span><span class="sxs-lookup"><span data-stu-id="307b5-108">Locale</span></span>                  | <span data-ttu-id="307b5-109">地區設定/語言名稱</span><span class="sxs-lookup"><span data-stu-id="307b5-109">Locale/language name</span></span> | <span data-ttu-id="307b5-110">值</span><span class="sxs-lookup"><span data-stu-id="307b5-110">Value</span></span>                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b5-111">英文 (美國)</span><span class="sxs-lookup"><span data-stu-id="307b5-111">English (United States)</span></span> | <span data-ttu-id="307b5-112">zh-TW</span><span class="sxs-lookup"><span data-stu-id="307b5-112">en-US</span></span>                | <span data-ttu-id="307b5-113">Latn;</span><span class="sxs-lookup"><span data-stu-id="307b5-113">Latn;</span></span>                                                                                                  |
| <span data-ttu-id="307b5-114">印度文 (印度)</span><span class="sxs-lookup"><span data-stu-id="307b5-114">Hindi (India)</span></span>           | <span data-ttu-id="307b5-115">hi-IN</span><span class="sxs-lookup"><span data-stu-id="307b5-115">hi-IN</span></span>                | <span data-ttu-id="307b5-116">Deva;</span><span class="sxs-lookup"><span data-stu-id="307b5-116">Deva;</span></span>                                                                                                  |
| <span data-ttu-id="307b5-117">日文 (日本)</span><span class="sxs-lookup"><span data-stu-id="307b5-117">Japanese (Japan)</span></span>        | <span data-ttu-id="307b5-118">ja-JP</span><span class="sxs-lookup"><span data-stu-id="307b5-118">ja-JP</span></span>                | <span data-ttu-id="307b5-119">**Windows 7 和更新版本：** Hani;Hira;Jpan;區分</span><span class="sxs-lookup"><span data-stu-id="307b5-119">**Windows 7 and later:** Hani;Hira;Jpan;Kana;</span></span><br/> <span data-ttu-id="307b5-120">**Windows Vista：** Hani;Hira;區分</span><span class="sxs-lookup"><span data-stu-id="307b5-120">**Windows Vista:** Hani;Hira;Kana;</span></span><br/> |



 

<span data-ttu-id="307b5-121">複合腳本值不包含拉丁腳本，除非它是用於特定地區設定之書寫系統的必要部分。</span><span class="sxs-lookup"><span data-stu-id="307b5-121">A compound script value does not include the Latin script unless it is an essential part of the writing system used for the particular locale.</span></span> <span data-ttu-id="307b5-122">拉丁字元通常用於不是原生的地區設定內容，例如外部商務名稱。</span><span class="sxs-lookup"><span data-stu-id="307b5-122">Latin characters are often used in the context of locales for which they are not native, for example, for a foreign business name.</span></span> <span data-ttu-id="307b5-123">在上述範例中，印度文的印度文中，唯一的腳本值為 "Deva" ("梵文" ) ，不過拉丁字元也可以出現在印度文文字中。</span><span class="sxs-lookup"><span data-stu-id="307b5-123">In the example above for Hindi in India, the only script value is "Deva" (for "Devanagari"), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="307b5-124">[VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)函式具有特殊旗標，可解決此案例。</span><span class="sxs-lookup"><span data-stu-id="307b5-124">The [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) function has a special flag to address this case.</span></span>

 

 




