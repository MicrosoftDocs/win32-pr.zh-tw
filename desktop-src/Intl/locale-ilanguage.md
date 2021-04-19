---
description: 地區設定 \_ ILANGUAGE
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970362"
---
# <a name="locale_ilanguage"></a><span data-ttu-id="fe8e9-103">地區設定 \_ ILANGUAGE</span><span class="sxs-lookup"><span data-stu-id="fe8e9-103">LOCALE\_ILANGUAGE</span></span>

<span data-ttu-id="fe8e9-104">具有十六進位值的[語言識別項](language-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="fe8e9-104">[Language identifier](language-identifiers.md) with a hexadecimal value.</span></span> <span data-ttu-id="fe8e9-105">例如，英文 (美國) 的值為0409，表示0x0409 十六進位，相當於 1033 decimal。</span><span class="sxs-lookup"><span data-stu-id="fe8e9-105">For example, English (United States) has the value 0409, which indicates 0x0409 hexadecimal, and is equivalent to 1033 decimal.</span></span> <span data-ttu-id="fe8e9-106">此字串允許的最大字元數為五個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="fe8e9-106">The maximum number of characters allowed for this string is five, including a terminating null character.</span></span>

<span data-ttu-id="fe8e9-107">**Windows Vista 和更新版本：** 使用這個常數可能會導致 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 傳回不正確地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe8e9-107">**Windows Vista and later:** Use of this constant can cause [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) to return an invalid locale identifier.</span></span> <span data-ttu-id="fe8e9-108">呼叫此函式時，您的應用程式應該使用 [LOCALE \_ SNAME](locale-sname.md) 常數。</span><span class="sxs-lookup"><span data-stu-id="fe8e9-108">Your application should use the [LOCALE\_SNAME](locale-sname.md) constant when calling this function.</span></span>

 

 



