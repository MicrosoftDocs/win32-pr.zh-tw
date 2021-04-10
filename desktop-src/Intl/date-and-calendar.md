---
description: 每個地區設定都有預設的行事曆類型 (資料類型 CALTYPE) 與其相關聯。 地區設定也可以有替代的行事曆類型。 如需行事曆類型的詳細資訊，請參閱行事曆類型資訊。
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: 日期和行事曆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851820"
---
# <a name="date-and-calendar"></a><span data-ttu-id="99143-105">日期和行事曆</span><span class="sxs-lookup"><span data-stu-id="99143-105">Date and Calendar</span></span>

<span data-ttu-id="99143-106">每個 [地區](locales-and-languages.md) 設定都有預設的行事曆類型 (資料類型 CALTYPE) 與其相關聯。</span><span class="sxs-lookup"><span data-stu-id="99143-106">Each [locale](locales-and-languages.md) has a default calendar type (data type CALTYPE) associated with it.</span></span> <span data-ttu-id="99143-107">地區設定也可以有替代的行事曆類型。</span><span class="sxs-lookup"><span data-stu-id="99143-107">A locale can also have an alternate calendar type.</span></span> <span data-ttu-id="99143-108">如需行事曆類型的詳細資訊，請參閱行事 [曆類型資訊](calendar-type-information.md)。</span><span class="sxs-lookup"><span data-stu-id="99143-108">For details of calendar types, see [Calendar Type Information](calendar-type-information.md).</span></span>

> [!Note]  
> <span data-ttu-id="99143-109">若要針對地區設定使用替代的行事曆類型，您的應用程式必須將 [地區設定 \_ IOPTIONALCALENDAR](locale-ioptionalcalendar.md) 常數設定為地區設定的替代行事曆類型。</span><span class="sxs-lookup"><span data-stu-id="99143-109">To use an alternate calendar type for a locale, your application must set the [LOCALE\_IOPTIONALCALENDAR](locale-ioptionalcalendar.md) constant to the alternate calendar type for the locale.</span></span>

 

<span data-ttu-id="99143-110">大部分的地區設定都使用標準西曆和設定的日期格式數目。</span><span class="sxs-lookup"><span data-stu-id="99143-110">Most locales use the standard Gregorian calendar and a set number of date formats.</span></span> <span data-ttu-id="99143-111">您可以使用 [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) 或 [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) 函數來顯示日期格式的這些預設選項。</span><span class="sxs-lookup"><span data-stu-id="99143-111">These default choices for date formats are available for display by using the [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) or [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) function.</span></span>

<span data-ttu-id="99143-112">某些地區設定在建立格式選項的完整清單時，需要特殊的考慮。</span><span class="sxs-lookup"><span data-stu-id="99143-112">Some locales require special considerations when creating a complete list of format choices.</span></span> <span data-ttu-id="99143-113">其中某些地區設定需要將文字字串插入日期格式字串中，而有些則需要以完全不同的方法來計算值。</span><span class="sxs-lookup"><span data-stu-id="99143-113">Some of these locales require text strings to be inserted in the date format string, while others require a completely different method of computation of the values.</span></span> <span data-ttu-id="99143-114">應用程式會藉由新增特定地區設定資訊類型和行事曆類型來解決這些特殊需求。</span><span class="sxs-lookup"><span data-stu-id="99143-114">An application addresses these special requirements by the addition of certain locale information types and calendar types.</span></span>

<span data-ttu-id="99143-115">如需在應用程式中執行日期和行事曆的詳細資訊，請參閱抓取 [時間和日期資訊](retrieving-time-and-date-information.md)。</span><span class="sxs-lookup"><span data-stu-id="99143-115">For details about implementing dates and calendars in your applications, see [Retrieving Time and Date Information](retrieving-time-and-date-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99143-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="99143-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99143-117">關於國家語言支援</span><span class="sxs-lookup"><span data-stu-id="99143-117">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="99143-118">行事曆類型資訊</span><span class="sxs-lookup"><span data-stu-id="99143-118">Calendar Type Information</span></span>](calendar-type-information.md)
</dt> <dt>

[<span data-ttu-id="99143-119">正在抓取時間和日期資訊</span><span class="sxs-lookup"><span data-stu-id="99143-119">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="99143-120">**EnumDateFormatsEx**</span><span class="sxs-lookup"><span data-stu-id="99143-120">**EnumDateFormatsEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[<span data-ttu-id="99143-121">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="99143-121">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



