---
description: 合併模組的預設語言是套用語言轉換之前，模組的 ModuleSignature 資料表中所列的語言。 這也是 [範本摘要] 屬性中所列的第一種語言。
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: 選擇多重語言合併模組的預設語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848940"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a><span data-ttu-id="f4484-104">選擇多重語言合併模組的預設語言</span><span class="sxs-lookup"><span data-stu-id="f4484-104">Choosing the Default Language of a Multiple Language Merge Module</span></span>

<span data-ttu-id="f4484-105">合併模組的預設語言是套用語言轉換之前，模組的 [ModuleSignature 資料表](modulesignature-table.md) 中所列的語言。</span><span class="sxs-lookup"><span data-stu-id="f4484-105">The default language for a merge module is the language that is listed in the [ModuleSignature Table](modulesignature-table.md) of the module before language transforms are applied.</span></span> <span data-ttu-id="f4484-106">這也是 [ [**範本摘要**](template-summary.md) ] 屬性中所列的第一種語言。</span><span class="sxs-lookup"><span data-stu-id="f4484-106">This is also the first language that is listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="f4484-107">模組的預設語言應該是您所支援的其中一種最特定語言，因為預設語言會先進行檢查，如果它符合要求的語言，則會使用它，即使另一個語言更相符也是一樣。</span><span class="sxs-lookup"><span data-stu-id="f4484-107">The default language for the module should be one of the most specific languages that you support, because the default language is always checked first, and if it satisfies the requested language, it is used even if another language is a better match.</span></span> <span data-ttu-id="f4484-108">例如，如果模組支援1033和0，則1033應該是預設語言。</span><span class="sxs-lookup"><span data-stu-id="f4484-108">For example, if a module supports 1033 and 0, 1033 should be the default language.</span></span> <span data-ttu-id="f4484-109">如果0是預設語言，它一定會滿足任何要求，而且永遠不會使用1033轉換，即使1033是所要求的正確語言。</span><span class="sxs-lookup"><span data-stu-id="f4484-109">If 0 were the default language, it would always satisfy any request, and the 1033 transform would never be used, even if 1033 is the exact language requested.</span></span>

 

 



