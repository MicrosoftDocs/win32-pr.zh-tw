---
description: 將模組合併至安裝資料庫時，有兩種重要的語言。
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: 以特定語言開啟 Multiple-Language 合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026356"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a><span data-ttu-id="47ed5-103">以特定語言開啟 Multiple-Language 合併模組</span><span class="sxs-lookup"><span data-stu-id="47ed5-103">Opening a Multiple-Language Merge Module in a Specific Language</span></span>

<span data-ttu-id="47ed5-104">將模組合併至安裝資料庫時，有兩種重要的語言。</span><span class="sxs-lookup"><span data-stu-id="47ed5-104">When merging a module into an installation database, there are two important languages.</span></span> <span data-ttu-id="47ed5-105">第一個是 [**ProductLanguage**](productlanguage.md) 在 [屬性資料表](property-table.md)中所指定之目標安裝套件的語言。</span><span class="sxs-lookup"><span data-stu-id="47ed5-105">The first is the language of the target installation package specified by [**ProductLanguage**](productlanguage.md) in the [Property Table](property-table.md).</span></span> <span data-ttu-id="47ed5-106">第二個是 [ModuleSignature 資料表](modulesignature-table.md)的 language 資料行中所顯示之 merge 模組的語言。</span><span class="sxs-lookup"><span data-stu-id="47ed5-106">The second is the language of the merge module that appears in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="47ed5-107">當封裝開啟進行合併時，合併工具可以將安裝封裝的語言傳遞給模組。</span><span class="sxs-lookup"><span data-stu-id="47ed5-107">The language of the installation package can be passed to the module by the merge tool when the package is opened for a merge.</span></span> <span data-ttu-id="47ed5-108">不過，有時候可能需要忽略目標的語言，並要求以另一種語言來開啟該模組，例如，從模組安裝英文和德文資源的英文套件。</span><span class="sxs-lookup"><span data-stu-id="47ed5-108">However, sometimes it may be necessary to disregard the language of the target, and request that the module be opened in another language, for example, an English package installing both the English and German resources from the module.</span></span>

<span data-ttu-id="47ed5-109">使用語言要求開啟模組時，合併工具會針對 [ModuleSignature 資料表](modulesignature-table.md)的 language 資料行中所指定的語言，檢查要求的語言。</span><span class="sxs-lookup"><span data-stu-id="47ed5-109">When opening a module with a language request, the merge tool checks the requested language against the languages that are specified in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="47ed5-110">下列程式是用來決定要使用的語言。</span><span class="sxs-lookup"><span data-stu-id="47ed5-110">The following process is used to determine which language to use.</span></span>

<span data-ttu-id="47ed5-111">**判斷要使用的語言**</span><span class="sxs-lookup"><span data-stu-id="47ed5-111">**To determine which language to use**</span></span>

1.  <span data-ttu-id="47ed5-112">如果 [ModuleSignature 資料表](modulesignature-table.md) 中的語言等於或高於要求的語言，則會開啟模組。</span><span class="sxs-lookup"><span data-stu-id="47ed5-112">If the language in the [ModuleSignature Table](modulesignature-table.md) is equal or more general than the requested language, the module opens.</span></span>
2.  <span data-ttu-id="47ed5-113">如果模組支援所要求的正確語言，則會使用該語言。</span><span class="sxs-lookup"><span data-stu-id="47ed5-113">If the module supports the exact language requested, that language is used.</span></span>
3.  <span data-ttu-id="47ed5-114">如果模組支援使用語言群組的語言群組，例如，如果已要求1033但在步驟2中找不到，則檢查9。</span><span class="sxs-lookup"><span data-stu-id="47ed5-114">If the module supports the language group of the language requested that language group is used, for example, check 9 if 1033 was requested but not found in step 2.</span></span>
4.  <span data-ttu-id="47ed5-115">檢查是否有語言轉換將模組變更為中性。</span><span class="sxs-lookup"><span data-stu-id="47ed5-115">Check if there is a language transform that changes the module to neutral.</span></span>
5.  <span data-ttu-id="47ed5-116">如果上述步驟都沒有成功，則模組不支援要求的語言，因此合併會失敗。</span><span class="sxs-lookup"><span data-stu-id="47ed5-116">If none of the previous steps succeed, the module does not support the requested language and the merge fails.</span></span>

 

 



