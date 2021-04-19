---
description: 地區設定 \_ SSHORTDATE
ms.assetid: 55333a53-1205-42eb-aa1a-c248c52a8a3f
title: LOCALE_SSHORTDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15077b4466fd74c02dd53bd7324aceba9233cc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996624"
---
# <a name="locale_sshortdate"></a><span data-ttu-id="e4b12-103">地區設定 \_ SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="e4b12-103">LOCALE\_SSHORTDATE</span></span>

<span data-ttu-id="e4b12-104">地區設定的簡短日期格式字串。</span><span class="sxs-lookup"><span data-stu-id="e4b12-104">Short date formatting string for the locale.</span></span> <span data-ttu-id="e4b12-105">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="e4b12-105">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="e4b12-106">此字串可以包含 [day、month、year 和 era 格式圖片](day--month--year--and-era-format-pictures.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="e4b12-106">The string can consist of a combination of [day, month, year, and era format pictures](day--month--year--and-era-format-pictures.md).</span></span> <span data-ttu-id="e4b12-107">例如，"M/d/yyyy" 表示2004年9月3日寫入9/3/2004。</span><span class="sxs-lookup"><span data-stu-id="e4b12-107">For example, "M/d/yyyy" indicates that September 3, 2004 is written 9/3/2004.</span></span>

<span data-ttu-id="e4b12-108">地區設定可以定義多個簡短的日期格式。</span><span class="sxs-lookup"><span data-stu-id="e4b12-108">Locales can define multiple short date formats.</span></span> <span data-ttu-id="e4b12-109">若要取得此地區設定的所有簡短日期格式，請使用 [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa)、 [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)或 [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)。</span><span class="sxs-lookup"><span data-stu-id="e4b12-109">To get all of the short date formats for this locale, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa), or [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span></span>

 

 



