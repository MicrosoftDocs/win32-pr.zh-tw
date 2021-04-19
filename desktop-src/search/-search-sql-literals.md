---
description: 常值是代表查詢語句中值的字元字串。 您可以使用常值來比較資料行的值，或指定搜尋詞彙。 Windows Search 支援下列類型的常值。
ms.assetid: cc526174-3c91-402d-b7d0-69fc9a61c3f9
title: 常值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e066f62a39bc46ec2ff7bf44c187d33f3832ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973228"
---
# <a name="literals"></a><span data-ttu-id="16109-105">常值</span><span class="sxs-lookup"><span data-stu-id="16109-105">Literals</span></span>

<span data-ttu-id="16109-106">常值是代表查詢語句中值的字元字串。</span><span class="sxs-lookup"><span data-stu-id="16109-106">A literal is a string of characters that represents a value in a query statement.</span></span> <span data-ttu-id="16109-107">您可以使用常值來比較資料行的值，或指定搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="16109-107">You use literals to compare column values or to specify search terms.</span></span> <span data-ttu-id="16109-108">Windows Search 支援下列類型的常值。</span><span class="sxs-lookup"><span data-stu-id="16109-108">Windows Search supports the following types of literals.</span></span>


-   <span data-ttu-id="16109-109">**字串常** 值可以是任何長度，而且可以包含 ANSI 或 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="16109-109">**String literals** can be any length and can contain either ANSI or Unicode characters.</span></span> <span data-ttu-id="16109-110">您必須以單引號括住字串常值 ( ' ) 。</span><span class="sxs-lookup"><span data-stu-id="16109-110">You must enclose string literals in single quotation marks(').</span></span> <span data-ttu-id="16109-111">若要在字串常值內加入單引號，請使用兩個單引號 ( ' ' ) 。</span><span class="sxs-lookup"><span data-stu-id="16109-111">To include a single quotation mark inside a string literal, use two single quotation marks ('').</span></span> <span data-ttu-id="16109-112">將空字串表示為兩個連續的單引號 ( ' ' ) 。</span><span class="sxs-lookup"><span data-stu-id="16109-112">Represent an empty string as two consecutive single quotation marks ('').</span></span>
-   <span data-ttu-id="16109-113">**數值常** 值可以包含數位0-9、句號，以及字母 E (或 E) 。</span><span class="sxs-lookup"><span data-stu-id="16109-113">**Numeric literals** can contain the digits 0-9, a period, and the letter E (or e).</span></span> <span data-ttu-id="16109-114">數值常值代表數位，包括正數和負整數、十進位數和貨幣值。</span><span class="sxs-lookup"><span data-stu-id="16109-114">Numeric literals represent numbers, including positive and negative integers, decimal numbers, and currency values.</span></span> <span data-ttu-id="16109-115">您可以使用科學記號標記法來定義數值常值 (例如 2.3 E-05) 。</span><span class="sxs-lookup"><span data-stu-id="16109-115">Numeric literals can be defined by using scientific notation (for example, 2.3E-05).</span></span> <span data-ttu-id="16109-116">請勿將數值常值括在單引號中，否則會被視為字串常值，並使用字串比較技巧進行比較。</span><span class="sxs-lookup"><span data-stu-id="16109-116">Do not enclose a numeric literal in single quotation marks, or it will be interpreted as a string literal and compared using string comparison techniques.</span></span> <span data-ttu-id="16109-117">貨幣值不能包含貨幣符號。</span><span class="sxs-lookup"><span data-stu-id="16109-117">Currency values cannot contain currency symbols.</span></span>
-   <span data-ttu-id="16109-118">**十六進位常** 值可以包含數位0-9 和字母 a-f 和 a-f。</span><span class="sxs-lookup"><span data-stu-id="16109-118">**Hexadecimal literals** can contain the digits 0-9 and the letters A-F and a-f.</span></span> <span data-ttu-id="16109-119">十六進位常值表示以十六進位標記法指定的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="16109-119">A hexadecimal literal represents an unsigned integer specified in hexadecimal notation.</span></span> <span data-ttu-id="16109-120">十六進位常值的開頭必須是0x。</span><span class="sxs-lookup"><span data-stu-id="16109-120">Hexadecimal literals must begin with 0x.</span></span>
    > [!Note]  
    > <span data-ttu-id="16109-121">SQL-92 標準要求以單引號括住十六進位常值;不過，Windows Search 不支援該標記法。</span><span class="sxs-lookup"><span data-stu-id="16109-121">The SQL-92 standard requires that hexadecimal literals be enclosed in single quotation marks; however, Windows Search does not support that notation.</span></span>

     

-   <span data-ttu-id="16109-122">**布林常** 值代表邏輯值，而且可以是 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="16109-122">**Boolean literals** represent logical values, and can be either **TRUE** or **FALSE**.</span></span> <span data-ttu-id="16109-123">請勿將布林值常值括在單引號中，或將它解釋為字串常值。</span><span class="sxs-lookup"><span data-stu-id="16109-123">Do not enclose a Boolean literal in single quotation marks, or it is interpreted as a string literal.</span></span>
-   <span data-ttu-id="16109-124">**日期常** 值代表特定日期、時間戳記或相對時間，並以單引號括住。</span><span class="sxs-lookup"><span data-stu-id="16109-124">**Date literals** represent specific dates, time stamps, or relative times, and are enclosed in single quotation marks.</span></span> <span data-ttu-id="16109-125">您必須將日期以年/月/日時數：分：秒或年-月-日時數：分鐘：秒，其中 month、day 和 year 是數位。</span><span class="sxs-lookup"><span data-stu-id="16109-125">You must put dates in the form year/month/day hours:minutes:seconds or year-month-day hours:minutes:seconds, where the month, day, and year are numbers.</span></span> <span data-ttu-id="16109-126">以四位數值指定年份，例如2004。</span><span class="sxs-lookup"><span data-stu-id="16109-126">Specify the year with a four-digit value, for example, 2004.</span></span> <span data-ttu-id="16109-127">時間值的格式必須為小時：分鐘：秒。</span><span class="sxs-lookup"><span data-stu-id="16109-127">Time values must be in the form hours:minutes:seconds.</span></span> <span data-ttu-id="16109-128">相對時間語法是以 [DATEADD 函數](-search-sql-dateadd.md)為基礎。</span><span class="sxs-lookup"><span data-stu-id="16109-128">Relative time syntax is based on the [DATEADD Function](-search-sql-dateadd.md).</span></span>

 

 



