---
description: 使用類似日期和時間語法的格式來定義日期時間間隔，方法是將字串分成數天、小時、分鐘、秒和毫秒的欄位。
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: 間隔格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989038"
---
# <a name="interval-format"></a><span data-ttu-id="b5c86-103">間隔格式</span><span class="sxs-lookup"><span data-stu-id="b5c86-103">Interval Format</span></span>

<span data-ttu-id="b5c86-104">WMI 會使用類似日期和時間語法的格式來定義日期時間間隔，方法是將字串分成數天、小時、分鐘、秒和微秒的欄位。</span><span class="sxs-lookup"><span data-stu-id="b5c86-104">WMI defines date-time intervals with a format similar to the date and time syntax by breaking the string into the fields for days, hours, minutes, seconds, and microseconds.</span></span>

<span data-ttu-id="b5c86-105">下列範例會顯示日期時間間隔的格式。</span><span class="sxs-lookup"><span data-stu-id="b5c86-105">The following example shows the format of a date-time interval.</span></span>

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

<span data-ttu-id="b5c86-106">下表列出日期時間間隔的欄位。</span><span class="sxs-lookup"><span data-stu-id="b5c86-106">The following table lists the fields of the date-time interval.</span></span>



| <span data-ttu-id="b5c86-107">欄位</span><span class="sxs-lookup"><span data-stu-id="b5c86-107">Field</span></span>    | <span data-ttu-id="b5c86-108">描述</span><span class="sxs-lookup"><span data-stu-id="b5c86-108">Description</span></span>                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c86-109">dddddddd</span><span class="sxs-lookup"><span data-stu-id="b5c86-109">dddddddd</span></span> | <span data-ttu-id="b5c86-110">代表數天 (00000000 到 99999999) 的八位數。</span><span class="sxs-lookup"><span data-stu-id="b5c86-110">Eight digits that represent a number of days (00000000 through 99999999).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="b5c86-111">HH</span><span class="sxs-lookup"><span data-stu-id="b5c86-111">HH</span></span>       | <span data-ttu-id="b5c86-112">一天中使用24小時制的兩位數小時 (00 到 23) 。</span><span class="sxs-lookup"><span data-stu-id="b5c86-112">Two-digit hour of the day that uses the 24-hour clock (00 through 23).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="b5c86-113">MM</span><span class="sxs-lookup"><span data-stu-id="b5c86-113">MM</span></span>       | <span data-ttu-id="b5c86-114">小時的兩位數分鐘 (00 到 59) 。</span><span class="sxs-lookup"><span data-stu-id="b5c86-114">Two-digit minute in the hour (00 through 59).</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="b5c86-115">SS</span><span class="sxs-lookup"><span data-stu-id="b5c86-115">SS</span></span>       | <span data-ttu-id="b5c86-116">分鐘 (00 到 59) 的兩位數秒數。</span><span class="sxs-lookup"><span data-stu-id="b5c86-116">Two-digit number of seconds in the minute (00 through 59).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="b5c86-117">mmmmmm</span><span class="sxs-lookup"><span data-stu-id="b5c86-117">mmmmmm</span></span>   | <span data-ttu-id="b5c86-118">第二個數字的毫秒數， (000000 到 999999) 。</span><span class="sxs-lookup"><span data-stu-id="b5c86-118">Six-digit number of microseconds in the second (000000 through 999999).</span></span> <span data-ttu-id="b5c86-119">使用此欄位時不需要您的實作為支援評估，但此欄位必須一律存在，以保留字元串的固定長度性質。</span><span class="sxs-lookup"><span data-stu-id="b5c86-119">Your implementation is not required to support evaluation using this field, but this field must always be present to preserve the fixed-length nature of the string.</span></span> |



 

<span data-ttu-id="b5c86-120">間隔一律具有尾端的 "： 000" 作為最後四個字元。</span><span class="sxs-lookup"><span data-stu-id="b5c86-120">Intervals always have a trailing ":000" as the last four characters.</span></span> <span data-ttu-id="b5c86-121">此外，與日期和時間不同的是，您無法使用星號來指出未使用的欄位。</span><span class="sxs-lookup"><span data-stu-id="b5c86-121">Further, unlike the date and time, you cannot use asterisks to indicate unused fields.</span></span> <span data-ttu-id="b5c86-122">此外，代表間隔的 [CIM \_ DATETIME](cim-datetime.md) 類型的所有屬性，都必須以 [子類型](standard-wmi-qualifiers.md) 標準辨識符號標示，並將限定詞設定為「間隔」。</span><span class="sxs-lookup"><span data-stu-id="b5c86-122">In addition, all properties of type [CIM\_DATETIME](cim-datetime.md) that represent intervals must be marked with the [SubType](standard-wmi-qualifiers.md) standard qualifier, with the qualifier set to "interval".</span></span>

<span data-ttu-id="b5c86-123">下列字串代表1天、12小時、0分鐘和32秒的間隔。</span><span class="sxs-lookup"><span data-stu-id="b5c86-123">The following string represents an interval of 1 day, 12 hours, 0 minutes, and 32 seconds.</span></span>

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a><span data-ttu-id="b5c86-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5c86-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5c86-125">日期和時間格式</span><span class="sxs-lookup"><span data-stu-id="b5c86-125">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="b5c86-126">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="b5c86-126">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="b5c86-127">CIM \_ DATETIME</span><span class="sxs-lookup"><span data-stu-id="b5c86-127">CIM\_DATETIME</span></span>](cim-datetime.md)
</dt> </dl>

 

 



