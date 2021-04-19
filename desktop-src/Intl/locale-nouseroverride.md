---
description: 地區設定 \_ NOUSEROVERRIDE
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977937"
---
# <a name="locale_nouseroverride"></a><span data-ttu-id="f57df-103">地區設定 \_ NOUSEROVERRIDE</span><span class="sxs-lookup"><span data-stu-id="f57df-103">LOCALE\_NOUSEROVERRIDE</span></span>

> [!Caution]  
> <span data-ttu-id="f57df-104">由於地區設定 \_ NOUSEROVERRIDE 會停用使用者喜好設定，因此強烈建議您不要使用。</span><span class="sxs-lookup"><span data-stu-id="f57df-104">Since LOCALE\_NOUSEROVERRIDE disables user preferences, its use is strongly discouraged.</span></span> <span data-ttu-id="f57df-105">由於 [自訂地區](custom-locales.md)設定、服務更新、不同的作業系統版本和其他案例可能會以非預期的方式變更資料，因此這個常數不保證資料的穩定性。</span><span class="sxs-lookup"><span data-stu-id="f57df-105">This constant does not guarantee data stability since [custom locales](custom-locales.md), service updates, different operating system versions, and other scenarios can change data in unexpected ways.</span></span> <span data-ttu-id="f57df-106">如需詳細資訊，請參閱 [使用永久性地區設定資料](using-persistent-locale-data.md)。</span><span class="sxs-lookup"><span data-stu-id="f57df-106">For more information, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

<span data-ttu-id="f57df-107">沒有使用者覆寫。</span><span class="sxs-lookup"><span data-stu-id="f57df-107">No user override.</span></span> <span data-ttu-id="f57df-108">例如，在多個函式（例如 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 和 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)）中，這個常數會導致函式略過任何使用者覆寫，並針對函式呼叫中指定的任何其他常數使用系統預設值。</span><span class="sxs-lookup"><span data-stu-id="f57df-108">In several functions, for example, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) and [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), this constant causes the function to bypass any user override and use the system default value for any other constant specified in the function call.</span></span> <span data-ttu-id="f57df-109">即使識別碼指出目前的地區設定，以及使用者已使用主控台變更部分值，或應用程式已使用 [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa)變更這些值，也會從地區設定資料庫取出資訊。</span><span class="sxs-lookup"><span data-stu-id="f57df-109">The information is retrieved from the locale database, even if the identifier indicates the current locale and the user has changed some of the values using the Control Panel, or if an application has changed these values by using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="f57df-110">如果未指定這個常數，則使用者從主控台設定的任何值，或應用程式已使用 [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) 設定的任何值，優先于目前系統預設地區設定的資料庫設定。</span><span class="sxs-lookup"><span data-stu-id="f57df-110">If this constant is not specified, any values that the user has configured from the Control Panel or that an application has configured using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) take precedence over the database settings for the current system default locale.</span></span>

 

 



