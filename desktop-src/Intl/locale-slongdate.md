---
description: 地區設定 \_ SLONGDATE
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b24d81318f471b33a4ab644a059607e5ac490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113569"
---
# <a name="locale_slongdate"></a><span data-ttu-id="d5f64-103">地區設定 \_ SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="d5f64-103">LOCALE\_SLONGDATE</span></span>

<span data-ttu-id="d5f64-104">地區設定的完整日期格式字串。</span><span class="sxs-lookup"><span data-stu-id="d5f64-104">Long date formatting string for the locale.</span></span> <span data-ttu-id="d5f64-105">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="d5f64-105">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="d5f64-106">字串可以包含 [day、month、year 和紀元格式的圖片](day--month--year--and-era-format-pictures.md) ，以及以單引號括住的任何字元字串。</span><span class="sxs-lookup"><span data-stu-id="d5f64-106">The string can consist of a combination of [day, month, year, and era format pictures](day--month--year--and-era-format-pictures.md) and any string of characters enclosed in single quotes.</span></span> <span data-ttu-id="d5f64-107">以單引號括住的字元會維持指定的狀態。</span><span class="sxs-lookup"><span data-stu-id="d5f64-107">Characters in single quotes remain as specified.</span></span> <span data-ttu-id="d5f64-108">例如，西班牙文 (西班牙) 的完整日期為 "dddd，dd ' de ' MMMM ' de ' yyyy"。</span><span class="sxs-lookup"><span data-stu-id="d5f64-108">For example, the Spanish (Spain) long date is "dddd, dd' de 'MMMM' de 'yyyy".</span></span> <span data-ttu-id="d5f64-109">地區設定可以定義多個完整的日期格式。</span><span class="sxs-lookup"><span data-stu-id="d5f64-109">Locales can define multiple long date formats.</span></span>

<span data-ttu-id="d5f64-110">若要取得地區設定的所有完整日期格式，請使用 [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa)、 [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)或 [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)。</span><span class="sxs-lookup"><span data-stu-id="d5f64-110">To get all of the long date formats for a locale, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa), or [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span></span>

 

 



